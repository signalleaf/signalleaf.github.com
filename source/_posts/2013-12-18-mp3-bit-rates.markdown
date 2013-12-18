---
layout: post
title: "MP3 Bit Rates, File Size, And Audio Quality"
date: 2013-12-18 07:54
comments: true
categories: [mp3, bit-rate, file compression, quality, podcast]
---

In [a previous blog post](/blog/2013/12/10/audio-vs-file-compression/)
I talked about the need for both file and audio compression
on your podcasts. At the end of that post, I linked out to
[an article from Scott Burton on audio compression](https://gist.github.com/scottburton11/3222152),
but did not have any information on MP3 file compression at
the time.

![](/images/blog_posts/c-clamp-mp3.png)

Well, I have all the MP3 file compression information, along with
bit rates and my own judgement on audio quality vs file size now.
And you might be surprised at the results! I know I was!

<!-- more -->

## The Episode Content And Bit Rates

I recorded a 32 minute podcast episode that contains 2 things:

0. A musical introduction
0. A lengty spoken track

The musical introduction takes not quite a minute, with the
spoken audio taking up the rest of the 32 minutes. The spoken
audio is not a complete episode, however. It is only a 1+ 
minute description of the episode's purpose, repeated over
and over and over again to get a podcast episode of 
approximately average length. In other words, **don't bother
listening past the first minute and a half**. It just repeats
for a long time to make the point of file size vs content 
length.

After recording the episode, I exported it under 10
separate bit rate settings, using [Aadacity](http://audacity.sourceforge.net/).
The bit rates include:

* 16K Constant Rate
* 32K Constant Rate
* 64K Constant Rate
* 128K Constant Rate
* 256K Constant Rate

And:

* 48K - 85K Variable Rate
* 80K - 120K Variable Rate
* 145K - 185K Variable Rate
* 170K - 210K Variable Rate
* 220K - 260K Variable Rate

## The Episodes

With all of these bit rate exports, I create a special
podcast on SignalLeaf just for these episodes. You can
[subscribe to the podcast RSS feed](http://www.signalleaf.com/podcasts/52b10a635b56000200000011/rss)
and listen to each of the episodes in iTunes and other
podcast players, or you can use the embedded players here.

#### Constant Bit Rate Versions

<iframe src="http://www.signalleaf.com/embed/52b10a635b56000200000011/52b10ade4cacd40200000050/" width="500" height="70" frameborder="0"></iframe>

<iframe src="http://www.signalleaf.com/embed/52b10a635b56000200000011/52b10cf04cacd40200000051/" width="500" height="70" frameborder="0"></iframe>

<iframe src="http://www.signalleaf.com/embed/52b10a635b56000200000011/52b10d824cacd40200000053/" width="500" height="70" frameborder="0"></iframe>

<iframe src="http://www.signalleaf.com/embed/52b10a635b56000200000011/52b10e6e5b56000200000017/" width="500" height="70" frameborder="0"></iframe>

<iframe src="http://www.signalleaf.com/embed/52b10a635b56000200000011/52b110185b56000200000018/" width="500" height="70" frameborder="0"></iframe>

<p>&nbsp;</p>

#### Variable Bit Rate Versions

<iframe src="http://www.signalleaf.com/embed/52b10a635b56000200000011/52b111a44cacd40200000059/" width="500" height="70" frameborder="0"></iframe>

<iframe src="http://www.signalleaf.com/embed/52b10a635b56000200000011/52b115e44cacd4020000005a/" width="500" height="70" frameborder="0"></iframe>

<iframe src="http://www.signalleaf.com/embed/52b10a635b56000200000011/52b117d94cacd4020000005c/" width="500" height="70" frameborder="0"></iframe>

<iframe src="http://www.signalleaf.com/embed/52b10a635b56000200000011/52b119354cacd4020000005e/" width="500" height="70" frameborder="0"></iframe>

<iframe src="http://www.signalleaf.com/embed/52b10a635b56000200000011/52b11a315b56000200000022/" width="500" height="70" frameborder="0"></iframe>

## The (Surprising) Results

As you would expect, the low-end results of the 16K bit rate
are attrocious. If it wasn't for the ridiculously small
file size, this would never even be an option. In fact, I'm
going to call it not an option anyways, in spite of the file
size. The audio quality is simply horrible. I wouldn't inflict
that on anyone.

I had always thought that a variable bit rate .mp3 file was going
to be smaller, but I had no idea just how much smaller they
would be - especially when comparing the file audio quality 
near their counterpart in the constant rates. 

The other surprising result is how little difference there is,
if there is any perceivable difference, between 128K and 
anything above it. At least with spoken podcasts, I don't see
any need to ever use anything above 128K Constant rate, or
the near equivalent quality of 80K-120K Variable rate.

## Final Recommendation 80K-120K Variable Rate

If I were going to recommend one signal bit rate to encode
your podcast .mp3 files, it would be 80K-120K Variable bit
rate. The audio quality vs file size is superb, with little
to not distortion or wobbles in a mostly spoken podcast.

If you press me hard enough, I'll admit that I want the
145K-185K Variable rate for music based podcasts. The additional
layers of sound found in music can present some warbles
and distortion on the high end frequencies at lower rates.
Honestly it's probably not going to bother anyong at the
80K - 120K rate, but I prefer to be safe when it comes to
my music encoding.

Be sure to compress your audio files according to your
podcast needs, weighing file size vs audio quality and 
available bandwidth.

Happy podcasting, all you Signalers!
