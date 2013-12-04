---
layout: post
title: "When Free Hosting Isn't \"Free\""
date: 2013-12-04 15:31
comments: true
categories: 
---

I found a question over on the StackExchange network recently, regarding
podcast hosting and the use of a CDN, with one answer suggesting
the use of SoundCloud for hosting.

> I am managing a small podcast website hosted on a shared server. Currently there are only eight or nine episodes, each of which are about 50 MB, so bandwidth is not really an issue at the moment.
> 
> However, looking forward, would it be feasible to use a "free" CDN like Cloudflare to serve the audio files? If so, how would I set this up?
> 
> I took a quick look at it before, and it seems you have to have your whole site routed (is that the right term?) through the CDN rather than just specific files or filetypes. I'd like some clarification on this.

It's an interesting question, if you ask me, but one that
comes with a lot of potential problems.

<!-- more -->

If you're not familiar with the idea behind a CDN, don't
worry about that. It's not something that most people need to
know about. If you're interested, though, check out 
[my article on using CDNs in web development](http://www.kendoui.com/blogs/teamblog/posts/13-11-07/know-when-to-cdn.aspx) (external link).

## Reduce Your File Size

Before I address the hosting concerns, you should really try 
to reduce your file size for the podcasts. Unless your podcast 
episodes are 2 to 4 hours long, each, you shouldn't be 
reaching 50 megs per file. Try reducing the audio quality in 
your mp3 files (and use .mp3 file compression if you're not 
already - it's the podcast industry standard). If you have a 
45 minute podcast, you should be able to get your .mp3 file 
down to around 15 to 20 megs, tops, without any significant 
reduction in sound quality for spoken voice podcasts. Music 
podcasts may be different, and you probably want higher 
quality, but those are the exception where voice based 
podcasts tend to be the rule.

## Free Hosting Is Almost Never "Free"

When it comes to bandwidth and hosting, you really want to 
avoid free if possible.

On the bandwidth side, free tends to be awful. CDNs are not 
meant to be used for very large files that are downloaded 
frequently, like podcast files. CDNs are typically meant for 
smaller files, like static HTML, JavaScript, CSS and images. 
You'll quickly realize just how "free" a free CDN is when 
your downloads get throttled down to slow speeds or your 
account gets shut off because you're using too much bandwidth.

In addition to bandwidth and even file size limitations on 
free accounts, you will likely end up with ads placed on your 
content, when using free hosting services for things like 
podcasts. Maybe you don't mind ads being placed on your 
podcast, to get free hosting. But there are some real dangers 
in this [when your podcasts suddenly have ads for sex toys in them](http://schoolofpodcasting.com/how-to-avoid-vibrator-commercials-on-your-podcast-say-no-to-free-media-hosting/)! 

(Note: that link is mostly safe for work. It's an article 
about the dangers of free hosting, including a story that 
is rather shocking, but has no unsafe images in it).

Finally, there is always a risk that your free account will 
be taken out from under you, for no reason. Service providers 
are not obligated to continue providing free service to 
anyone, in the vast majority of cases. They may decide that 
they can no longer afford it, and yank the rug out from 
everyone that is hosted for free, or simply close up shop and 
disappear. It happens more than people want to admit. 

## SoundCloud Has Limits On Free

One of the comments on the question suggested using SoundCloud
as a podcast host. This is a common thing to do, actually. 
SoundCloud offers a unique spin on hosting audio and even
provides RSS and stats for podcasts. The reponder even note
that StackExchanged used SoundCloud (which may or may not
be accurate anymore... that should be verified). 

StackExchange may use SoundCloud for it's podcast hosting, 
but I guarantee they don't use a free account. Perhaps they 
have some deal with SoundCloud where they don't get charged 
anything, but this type of discount arrangement is very 
different than the free account that SoundClod offers. 

[From SoundCloud's website](http://help.soundcloud.com/customer/portal/articles/247820-what-s-the-difference-between-each-subscription-level-), 
you can see exactly what limitations you will run in to with 
the free account:

> 
> Free
>
> - 2 total upload hours
>
> - 100 downloads/sound
>
> - Unlimited playlist creation
>
> - Some stats (see the amount of plays, downloads, comments and favorites of your tracks)

## Free Trial and "Freemium" Are Legit

There are other types of "Free" accounts than "I'll give you
something for nothing", though. 

Many services offer free trials
that give you a set time limit for using the service. This 
type of "free" is usually legit. It gives you a way to try
out a service without having to pay anything, knowing that
if you like the service you'll have to pay to continue with
it. There's nothing wrong with free trials, and I actually
encourage people to try as many free trials as they need to,
to figure out what service fits their needs the best.

Other services, like SoundCloud, offer a "freemium" service
type. This is a service that gives you free service, typically
supported by ads or other monetiziation means. The free
service will have strict limitations on what you can and
cannot do, but won't stop your service after a certain period
of time. The idea is that after you get in to the service,
you'll be hooked and you'll want to pay for the services to
get the better features.

There's some debate about "freemium" services these days, with
a lot of companies saying it's not viable, and even some
companies going out of business because of it. Now imaging
how bad that would be if you were a paying customer of a
service and all the free accounts caused the service to go
out of business! I'd be pretty upset about that.

## Your Best Option: Paid Podcast Hosting Service

In the end, your best option is to pay for podcast hosting 
services. There are a lot of great services available, 
**including my own at [SignalLeaf.com](http://signalleaf.com)**, 
LibSyn, Blubrry, and many more. These services start cheap - 
very cheap - usually with a free trial before you actually 
have to pay for anything. My **SignalLeaf** service has a 
rather lengthy trial period compared to most. This gives you 
plenty of time to figure out if you want to continue with the 
service or not. 

At only a few $ a month, paid podcast hosting services are 
going to give you all the space you need for file storage and 
bandwidth, provide an iTunes and other podcast app compatible 
RSS feed, and give you all the stats and feedback that you 
need for your podcast. 

All of these paid services host their files on servers that 
are going to stream your audio more reliably than any free 
service you would find. By paying a company to host your 
files, you are giving them incentive to make sure they are 
keeping you happy and doing the best job possible to keep 
your podcast rolling smoothly. SignalLeaf, for example, 
uses Amazon S3 storage and streaming of all podcast files. 
There's no way your listeners are going to use up the 
bandwidth of S3. You'll never see a slow-down in delivery, 
or have problems with file storage reliability.

Stats are also important if you're looking for motivation 
to continue podcasting, or want sponsors. You're not going 
to get the stats you need without paying for service, either. 
Generating stats is not as simple as most people thing, which 
is why it always takes a more expensive paid account to get 
great stats. 

---

## Start Your Free Trial, Now!

If you're serious about your podcasts, do yourself a favor 
and get [a podcast hosting service](http://signalleaf.com) to 
handle the heavy lifting and distribution of your content. 
You'll never be happier than if reduce your own burden so 
that you can focus on the content, not the content delivery.

