---
layout: post
status: publish
published: true
title: We Swim in a Sea of White Noise
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 3627
wordpress_url: http://www.victusspiritus.com/?p=3627
date: '2010-04-17 07:58:05 -0400'
date_gmt: '2010-04-17 14:58:05 -0400'
categories:
- Uncategorized
tags:
- social web
- social filtering
- design
comments:
- id: 4589
  author: Scale Invariant Patterns - Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/06/23/scale-invariant-patterns/
  date: '2010-06-23 05:32:11 -0400'
  date_gmt: '2010-06-23 12:32:11 -0400'
  content: "[...] you ever caught yourself staring at a white noise screen, or listening
    to static and seen or heard a signal? It&#8217;s not a hallucination but a [...]"
- id: 5862
  author: Cool Breezes, the Messenger of Change, and Fantastic Network Challenges
    | Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/09/10/cool-breezes-the-messenger-of-change-and-fantastic-network-challenges/
  date: '2010-09-10 05:42:12 -0400'
  date_gmt: '2010-09-10 12:42:12 -0400'
  content: "[...] My professional home has become, and likely always will be, tackling
    open network problems. Whether on the web or the broader internet, there is a
    growing need for improving personal relevance as a means of filtering out noise.
    [...]"
---
<p><a href="{{ site.url }}/assets/2010/04/l_500_369_1E93B520-9711-478C-A496-FEB6F5E04E1F.jpeg"><img src="{{ site.url }}/assets/2010/04/l_500_369_1E93B520-9711-478C-A496-FEB6F5E04E1F.jpeg" alt="" class="alignnone size-full" /></a></p>
<p>We're all familiar with uncorrelated static. As a kid when a broadcast station failed to tune in, I'd just get static. The image of light and dark accompanied by a fuzzy spectrum of sound. </p>
<h2>What is White Noise?</h2>
<p>The definition of <a HREF="http://en.m.wikipedia.org/wiki/White_noise?wasRedirected=true">white noise</a> is one I'm intamitely familiar with as a long time signal processing engineer. Simply stated, the signal is uncorrelated over time (or space). There are no repeating patterns and the frequency response (or power spectral density) of the signal is flat, which means signal energy is evenly distributed between all frequencies. </p>
<p>For folks that are interested in detection and pattern matching it may seem an odd strategy to transform measured signals into white noise. But what you're really working to accomplish is to diminish the correlation in background or dominant sources to improve sensitivity to orthogonal signals of interest. Any residual signal power will stand out with optimized signal to noise power. We use sample or theoretical covariances to accomplish the data transforms, but these are fancy ways of describing signal patterns between intervals in either time or space. If you can make the background statistically look like white noise, even very weak signals can stand out and after integration enable detection due to residual correlation. </p>
<h2>Signal to Noise</h2>
<p>Consider a random signal that rises and falls over time with a mean of zero. Although the power (energy/time) of the noise won't change with larger integration, a correlated signal will. Integration of signal yields a square root of N improvement in <a href="http://en.m.wikipedia.org/wiki/Signal-to-noise_ratio?wasRedirected=true">signal to noise</a> ratio where N is the number of frames integrated.</p>
<blockquote><p>
In less technical terms, signal-to-noise ratio compares the level of a desired signal (such as music) to the level of background noise. The higher the ratio, the less obtrusive the background noise is. "Signal-to-noise ratio" is sometimes used informally to refer to the ratio of useful information to false or irrelevant data in a conversation or exchange. For example, in online discussion forums and other online communities, off-topic posts and spam are regarded as "noise" that interferes with the "signal" of appropriate discussion.
</p></blockquote>
<p>If you're a regular reader here, you may see the root of my interest in discussing white noise. A long standing personal infatuation with relevant information and social sharing. Personal relevance engines, filters and virtual assistants are all part of an organic solution to the question:<br />
<I>"what's happening recently, now, or soon that is important and interesting to me?"</I><br />
The challenge is creating algorithms that improve over time to better adapt to the topics and styles we are interested in. </p>
<ul>
<li>Predictive or suggestion engines are one filtering method that attempt to cluster users into groups. If members of a group greatly appreciate some new content, others in the cluster are alerted to the discovery</li>
<li>abstraction of specific interests into topics allows the previous clustering algorithm to introduce new potential categories to people</li>
<li>clustering by content origin or input streams is another method of raising interesting information above noise</li>
</ul>
<p>Because many of our friends may have interests divergent from our own, simple social sharing becomes saturated with noisy or popular mass media content. The most potent information filters will introduce intriguing finds and arouse interests we never knew we had. Serendipity has shown me time and again how little I know about even my own interests. We close ourselves off to so much in the interest of protecting our attention and limited time that our quest for relevance dead ends in <a href="http://victusfate.github.io/victusspiritus/uncategorized/2009/11/04/leaving-a-local-optima-takes-every-ounce-of-our-resolve/">local optimas</a>. My goal with a startup is to ensure that doesn't happen. </p>
