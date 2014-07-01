---
layout: post
status: publish
published: true
title: Real Time Publishing, Help with RSSCloud & PubHubSubbub (Push)
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
excerpt: If you're like myself, a fairly active blogger who wants to supply your blog
  as quickly as possible to interested readers and subscribers, real time publishing
  is pretty damn cool. Unfortunately, most of us are not experts in Internet based
  protocols and distribution systems. <a class="zem_slink" title="Representational
  State Transfer" rel="wikipedia" href="http://en.wikipedia.org/wiki/Representational_State_Transfer">REST</a>,
  <a class="zem_slink" title="SOAP" rel="wikipedia" href="http://en.wikipedia.org/wiki/SOAP">SOAP</a>,
  <a class="zem_slink" title="Simple Update Protocol" rel="wikipedia" href="http://en.wikipedia.org/wiki/Simple_Update_Protocol">SUP</a>,
  PubSub... the acronym list goes on but recently there has been a lot of noise about
  RSSCloud vs. Push (PubHubSubbub).
wordpress_id: 1548
wordpress_url: http://www.victusspiritus.com/?p=1548
date: '2009-09-11 10:55:23 -0400'
date_gmt: '2009-09-11 17:55:23 -0400'
categories:
- Uncategorized
tags:
- web/tech
- real time web
comments: []
---
<p>If you're like myself, a fairly active blogger who wants to supply your blog as quickly as possible to interested readers and subscribers, real time publishing is pretty damn cool. Unfortunately, most of us are not experts in Internet based protocols and distribution systems. <a class="zem_slink" title="Representational State Transfer" rel="wikipedia" href="http://en.wikipedia.org/wiki/Representational_State_Transfer">REST</a>, <a class="zem_slink" title="SOAP" rel="wikipedia" href="http://en.wikipedia.org/wiki/SOAP">SOAP</a>, <a class="zem_slink" title="Simple Update Protocol" rel="wikipedia" href="http://en.wikipedia.org/wiki/Simple_Update_Protocol">SUP</a>, PubSub... the acronym list goes on but recently there has been a lot of noise about RSSCloud vs. Push (PubHubSubbub).<a id="more"></a><a id="more-1548"></a></p>
<p>The short short version: Each protocol allows publishers to let hubs know (ping) about new information. The hubs then ping their subscribers to let them know new information is available. Push sends the latest differences in the update, RSSCloud leaves that functionality to the user, and just lets them know there has been an update.</p>
<p><span style="background-color: #ffffff;">I've been hanging around some conversations between friendfeed users that openly share their curiosity, and sometimes expert descriptions of the new protocols. The TechCrunch article ,<a href="http://www.techcrunch.com/2009/09/09/rsscloud-vs-pubsubhubbub-why-the-fat-pings-win/">RSSCloud Vs. PubSubHubbub: Why The Fat Pings Win</a>, by Josh Fraser, delineates some of the features of the protocols, and why if he had to choose one he'd go with Push. Luckily we don't have to choose, both can easily be supported by any publisher. </span></p>
<p><span style="background-color: #ffffff;">Some additional solutions to over polling:</span></p>
<p>Roy T. Fielding added some additional insight on the <a class="zem_slink" title="Publish/subscribe" rel="wikipedia" href="http://en.wikipedia.org/wiki/Publish/subscribe">Pub/Sub</a> debate by describing alternative solutions to event based architectures (Push/RssCloud) vs. <a href="http://en.wikipedia.org/wiki/Representational_State_Transfer">REST</a> based architectures (html), in his post <a href="http://roy.gbiv.com/untangled/2008/paper-tigers-and-hidden-dragons">Paper tigers and hidden dragons</a>. Of course this lead me down the rabbit hole of <a href="http://bitworking.org/news/380/bloom-filter-resources">Bloom Filters</a> (from Joe Gregorio). Bloom filter algorithms support a type of hashing that gives back a controllable level of false positives but is highly compressed and doesn't need information (a legend or key) about a universal set to test for membership (change of users, etc).</p>
<h6 class="zemanta-related-title" style="font-size: 1em;">Related articles by Zemanta</h6>
<ul class="zemanta-article-ul">
<li class="zemanta-article-ul-li"><a href="http://www.jeffisageek.net/blog/2009/09/10/pubsubhubbub-and-rsscloud-adding-them-to-your-wordpress-blog/">PubSubHubBub and RSSCloud : Adding Them To Your Wordpress Blog</a> (jeffisageek.net)</li>
<li class="zemanta-article-ul-li"><a href="http://oreilly.com/catalog/9780596808679/">RESTful Web Services Cookbook: Rough Cuts Version</a> (oreilly.com)</li>
<li class="zemanta-article-ul-li"><a href="http://victusfate.github.io/victusspiritus/uncategorized/2009/09/09/rsscloud-goes-nuclear/">Rsscloud goes nuclear!</a> (victusspiritus.com)</li>
</ul>
<div class="zemanta-pixie" style="margin-top: 10px; height: 15px;"><a class="zemanta-pixie-a" title="Reblog this post [with Zemanta]" href="http://reblog.zemanta.com/zemified/994cc2c2-5676-4fb2-9501-d940f3aed6e2/"><img class="zemanta-pixie-img" style="border: none; float: right;" src="http://img.zemanta.com/reblog_e.png?x-id=994cc2c2-5676-4fb2-9501-d940f3aed6e2" alt="Reblog this post [with Zemanta]" /></a><span class="zem-script more-related pretty-attribution"><script src="http://static.zemanta.com/readside/loader.js" type="text/javascript"></script></span></div>
