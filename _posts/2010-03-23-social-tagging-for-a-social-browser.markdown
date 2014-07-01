---
layout: post
status: publish
published: true
title: Social Tagging for a Social Browser
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 3363
wordpress_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/03/23/social-tagging-for-a-social-browser/
date: '2010-03-23 04:11:55 -0400'
date_gmt: '2010-03-23 11:11:55 -0400'
categories:
- Uncategorized
tags:
- social web
- victus media
- opengardin
- crowd sourced
comments:
- id: 3569
  author: William Mougayar
  author_email: william@eqentia.com
  author_url: http://portal.eqentia.com
  date: '2010-03-24 13:07:31 -0400'
  date_gmt: '2010-03-24 18:07:31 -0400'
  content: 'The issue is that creators & consumers don&#39;t always have the same
    context requirements, and that&#39;s a key factor. <br>Curators are typically
    closely aligned with the needs of the consumers of info. It&#39;s a tough balance
    for deciding where to tag: at the source, or at the destination.'
- id: 3570
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-03-24 13:23:05 -0400'
  date_gmt: '2010-03-24 18:23:05 -0400'
  content: We&#39;re betting both is the right answer. Thanks for stopping in and  <br>sharing
    your expertise William! Have you read Louis Gray&#39;s posts on  <br>My6sense
    and Zite. In addition to Cascaad many are joining in to  <br>explore the opportunities
    of social search & the never ending quest  <br>for relevance.
- id: 3603
  author: Laurent Boncenne
  author_email: lboncenne@gmail.com
  author_url: ''
  date: '2010-03-26 14:55:07 -0400'
  date_gmt: '2010-03-26 19:55:07 -0400'
  content: Virtual rewards sounds a lot like how GetGlue works (somehow), based on
    a product, you may get a free ticket to see the premiere of X movie or whatnot...<br>I
    would take a look at a recent article posted either on TC or Mashable (maybe VentureBeat
    or RWW, I&#39;m really not sure sorry) about how Facebook is going to apparently
    massively roll out a Like button for pretty much anything. It seems this year&#39;s
    F8 is going to be big.<br><br>As for tagging, I can see the advantage for the
    technology itself, but is it really what the consumer wants ? Instead, should
    it not show a visual mapping of the User Interests space ?<br>Check out also <a
    href="http://pearltrees.com" rel="nofollow">pearltrees.com</a> it&#39;s a "social
    bookmarking tool" I don&#39;t really use it much, but I need to dig deeper into
    it...
- id: 3609
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-03-26 18:43:23 -0400'
  date_gmt: '2010-03-26 23:43:23 -0400'
  content: I had tried out GetGlue, but didn&#39;t like it because of the requirement
    for a browser addon (why not use cookies). Delicio.us was a fun way to share my
    bookmarks, but the tags aren&#39;t related to a common standard. I think this
    is an issue we have to decide on, my preference is to allow any tags, but to encourage
    common ones (maybe from linked semantic data).
---
<p>In the quest to design a social reader thats fun and useful, Tyler and I have previously leaned heavily on semantic entity extraction from web feeds. While useful, entity matching APIs are lossy, noisy, and can become expensive very quickly (many thousands of dollars per month). It is our belief that between the creators and curators of content there is more than enough "human intelligence" out there to categorize media. In nearly all instances a knowledgable reader is capable of more precisely tagging content. </p>
<p>Here are the benefits of setting up opengard.in this way:</p>
<ul>
<li>creators and curators will get virtual rewards for contributing
</li>
<li>we get over the heavy cost in automation of semantic tagging for a great number of feeds by using what's there already and creating a framework for additional human knowledge.
</li>
<li>we can build statistical algorithms to suggest tags by learning from human decisions given content/data. I think this could be a fun project where we can leverage open source & algorithms. I was thinking of starting with titles, first paragraphs, and song/video beginnings and converting them to binary arrays of "word" data. There may even be correlations between compression and content topics that are worth exploring</li>
</ul>
