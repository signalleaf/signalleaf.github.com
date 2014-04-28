---
layout: post
title: "Correcting Episode Tracking For Mobile And Other Devices"
date: 2014-04-28 12:43
comments: true
categories: [SignalLeaf, Tracking, Features]
---

A while back, one of the SignalLeaf users notified me of a
problem with their episode download stats. In a podcast that
has near 50 episodes with around 1,200 listens per episode
on average, one of the episodes spiked up to more than
22,000 listens... at least, the episode report said it did.
That didn't seem right to the podcaster, and certainly didn't
seem right to me. And it turns out it wasn't right... at least,
it wasn't the expected results even if it was technically
correct.

<img src="/images/blog_posts/true-or-false-confused.jpg" class="center">

<!-- more -->

It got worse, though. More podcasters reported similar problems,
over time. I thought the first big report was strange, but it
was getting to be a real problem now. So I dug in to see what
was going on and analyized the traffic reports. I wanted to see
if there was a pattern to the extraneous tracking downloads.
Were they just duplicates? Were they DDoS attacks? or ???

## Legit But Incorrect

It turns out the entries were all legitimate. There was no
bot-net trying to take down my server. These were not duplicate
entries. What they were, though, was a mistake based on not
understanding how mobile devices download episodes.

The code I have in place to track downloads makes a new entry
for every single request that comes in for an episode. This is
pretty straight-forward and has worked well for a while now.
When a download happens (whether its through iTunes, a direct
download of the file, or however it happens), an entry is made
in the episode tracking. What I didn't anticipate, though, was
the way mobile devices make multiple requests for a single
file.

## HTTP Byte Range Requests

Most browsers and desktop podcast apps like iTunes make a single
request for an episode file when they need it. They reach out
to the podcast media host (SignalLeaf in this case) and 
ask the host for the file. They download it and life goes on.

Mobile devices, however, don't always have a stable network
on which to run. They need to account for downloads starting
and stopping and networks shutting off and coming back on. To
do this, mobile devices use an HTTP Byte Range Request to
request only a small amount of information at a time - something
that will be easy to download on an unreliable network. The
device then records the last request made so that it can
continue where it left off. Continuing the download happens
almost right away in most cases, but sometimes happens much
much later if the device lost it's network connection.

This is significant because a request for a podcast that is
50 megs will generate hundreds or thousands of requests to
download that one file. And SignalLeaf was recording each 
request as a new download. In the worst case that I have 
recorded, there were more than 63,000 requests to download a 
single file! The device in question spent nearly 11 hours
making a request per second for a tiny amount of information
in each request. This is a ridiculously large number of 
requests over a ridiculously large period of time, but it's
what the device was doing.

Imaging having a podcast that gets a few hundred downloads
per episode, and suddenly having 63,000 for one episode! That
wouldn't make sense to you or me. Instead, you would expect
that one device to have 1 entry in the episode download
report. This is what I would expect, too.

## Correcting The Problem, Moving Forward

Having dug in to this, I found it's easy to correct the problem
now that I know what it is. So from here on forward, SignalLeaf
will only make an entry in the episode downloads once per
however many requests are made from a device. No matter how
many requests are made for the file, over how long of a period
of time, the byte range marker in the HTTP request tells me
that this is a continuation of a previous download and I 
don't need to continue tracking it. 

## What This Means For You, Podcaster

From here on out, your download stats for episodes will be
more accurate and less bloated by mobile devices that are
downloading episodes. You may see a reduction in the average
downloads per episodes because of this. This is to be expected
since I am now more accurately tracking the downloads.

Previous episode tracking information is still showing all of
the false-positive entries at the moment. I have not yet
worked out a simple way to correct this for all episodes, but
I have corrected a number of bad entries for the most
egregiously large tracking problems. 

I'll continue to monitor the situation, of course, and will 
make sure that the podcast and episode reports for listens
and downloads are as accurate as possible.
