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
With all of these bit rate exports, I create a special
podcast on SignalLeaf just for these episodes. You can
[subscribe to the podcast RSS feed](http://www.signalleaf.com/podcasts/52b10a635b56000200000011/rss)
and listen to each of the episodes in iTunes and other
podcast players, or you can use the embedded players here.

## Constant Bit Rate Versions

These episodes were exported at a constant bit rate - a rate that stays the same
throughout the entire encoding, regardless of the amount of data that there is to
encode.

#### 16K Constant

<iframe src="http://www.signalleaf.com/embed/52b10a635b56000200000011/52b10ade4cacd40200000050/" width="500" height="70" frameborder="0"></iframe>
Episode exported at 16K Constant bit rate with 20K sampling (max supported by 16K file bit rate). The effect is quite horrible. Everything sounds muffled, warbly, and like its in a tin can with ear muffs. The file is quite small, at 3.9Megs, though.

#### 32K Constant

<iframe src="http://www.signalleaf.com/embed/52b10a635b56000200000011/52b10cf04cacd40200000051/" width="500" height="70" frameborder="0"></iframe>

Episode exported at 32K Constant bit rate with 44.1K sampling. The effect is still pretty bad. Everything sounds warbly and slightly muffled, though not as bad as the 16K file. The highs are especially off, and a lot of the stereo effect in the opening music is gone. The file is still pretty small, at 7.7Megs.

#### 64K Constant

<iframe src="http://www.signalleaf.com/embed/52b10a635b56000200000011/52b10d824cacd40200000053/" width="500" height="70" frameborder="0"></iframe>

Episode exported at 64K Constant bit rate with 44.1K sampling. The quality drop in this file is negligible. There are some points in the opening music where some slight warbles can be heard on the high end sounds. Additional guitar sounds and other instruments tend to have a more pronounced warbled sound at this bit rate. The file size is still quite reasonable and may be considered "small" by some standards, at 15.5Megs.

#### 128K Constant

<iframe src="http://www.signalleaf.com/embed/52b10a635b56000200000011/52b10e6e5b56000200000017/" width="500" height="70" frameborder="0"></iframe>

Episode exported at 128K Constant bit rate with 44.1K sampling. The net effect of this bit rate is no noticeable degradation in audio quality, throughout the podcast episode. If additional instrumentation were present, there would be little to no loss of audio quality. The quality comes at a trade off in file size, though, with the file being 31Megs in size. This size is hardly acceptable for a podcast that is only 32 minutes in length.

#### 256K Constant

<iframe src="http://www.signalleaf.com/embed/52b10a635b56000200000011/52b110185b56000200000018/" width="500" height="70" frameborder="0"></iframe>

Episode exported at 256K Constant bit rate with 44.1K sampling. At 62 megs, this file size is completely unacceptable for distributing a podcast of only 32 minutes in length. The sound quality, however, is near impeccable. There is little chance that anyone would be able to pick up any distortions in the quality of audio.

## Variable Bit Rate Versions

Variable bit rate encoding allows the bit rate to change based on the amount of information
that needs to be encoded. If there is less audio signal to encode, the bit rate goes down.
If there is more, it goes up. This can reduce the file size while still maintaining quality,
in many cases.

#### 48K - 85K Variable

<iframe src="http://www.signalleaf.com/embed/52b10a635b56000200000011/52b111a44cacd40200000059/" width="500" height="70" frameborder="0"></iframe>

Exported at 48K-85K Variable bit rate with 44.1K sampling. There is very little distortion in this file, even in the musical introduction. A direct comparison of the 64K Constant bit rate yields a slight increase in audio quality over that export. The file size, in comparison, dropped from 15.5Megs down to 13Megs. The audio quality vs file size at this bit rate is quite nice.

#### 80K - 120K Variable

<iframe src="http://www.signalleaf.com/embed/52b10a635b56000200000011/52b115e44cacd4020000005a/" width="500" height="70" frameborder="0"></iframe>

Exported at 80K-120K Variable bit rate with 44.1K sampling. There is little to no perceivable distortion in this audio even in the musical introduction. A larger assortment of musical instruments comprising a full band or orchestra may exhibit some minor issues, but not enough to cause serious displeasure. A direct comparison of the 128K Constant bit rate yields approximately the same audio quality, though it is technically slightly less. The file size, in comparison, dropped from 31Megs down to 18.4Megs for a mostly spoken audio file. The audio quality vs file size at this bit rate is quite nice.

#### 145K - 185K Variable

<iframe src="http://www.signalleaf.com/embed/52b10a635b56000200000011/52b117d94cacd4020000005c/" width="500" height="70" frameborder="0"></iframe>

Exported at 145K-185K Variable bit rate with 44.1K sampling. There is little to no perceivable distortion in this audio even in the musical introduction. A larger assortment of musical instruments comprising a full band or orchestra may exhibit some minor issues, but not enough to cause serious displeasure. A direct comparison of the 128K Constant bit rate yields a technically higher quality audio file, but with little perceivable difference (if any). The file size, in comparison, dropped from 31Megs down to 26Megs for a mostly spoken audio file. The audio quality vs file size at this bit rate is acceptable for music based podcasts, but may be slightly larger than desired for spoken podcasts.

#### 170K - 210K Variable

<iframe src="http://www.signalleaf.com/embed/52b10a635b56000200000011/52b119354cacd4020000005e/" width="500" height="70" frameborder="0"></iframe>

Exported at 170K-210K Variable bit rate with 44.1K sampling. There is little to no perceivable distortion in this audio even in the musical introduction. A larger assortment of musical instruments comprising a full band or orchestra should not exhibit any noticeable distortion, except in extreme cases. A direct comparison of the 128K Constant bit rate yields a higher quality that is imperceptibly improved with a spoken podcast. A full orchestra or other large arrangement of instruments may show some perceived improvements. The file size, in comparison, dropped from 31Megs down to 30.4Megs for a mostly spoken audio file - a negligible difference, at best. The audio quality vs file size at this bit rate may be acceptable for music based podcasts, but is too large for spoken podcasts.

#### 220K - 260K Variable

<iframe src="http://www.signalleaf.com/embed/52b10a635b56000200000011/52b11a315b56000200000022/" width="500" height="70" frameborder="0"></iframe>

Exported at 220K-260K Variable bit rate with 44.1K sampling. Good luck finding any perceivable audio quality problems with this one. A direct comparison of the 256K Constant bit rate yields approximately the same audio quality, though it is technically slightly less. The file size, in comparison, dropped from 62Megs down to 39.2Megs for a mostly spoken audio file - a significant reduction. The audio quality vs file size at this bit rate is not acceptable for streaming. The file is simply too large for the amount of content contained within it.

## The (Somewhat Surprising) Results

As you would expect, the low-end results of the 16K bit rate
are attrocious. If it wasn't for the ridiculously small
file size, this would never even be an option. In fact, I'm
going to call it not an option anyways, in spite of the file
size. The audio quality is simply horrible. I wouldn't inflict
that on anyone.

I've always known that a variable bit rate .mp3 file was going
to be smaller, but I had never directly compared the file size
and audio quality with a constant/variable counterpart before.
The ability to keep roughly the same file size while increasing
the over-all quality was a nice effect when comparing 64K Constant
to 80-120K Variable, for example. The Variable is slightly
larger, but with the increase of quality and negligible file size
gain, this was a huge win for variable bit rates!

The other surprising result is how little difference there is,
if there is any perceivable difference, between 128K and 
anything above it. At least with spoken podcasts I don't see
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
