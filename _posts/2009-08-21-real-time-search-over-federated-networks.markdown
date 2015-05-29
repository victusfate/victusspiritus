---
layout: post
status: publish
published: true
title: Real Time Search Over Federated Networks
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 1409
wordpress_url: http://www.victusspiritus.com/?p=1409
date: '2009-08-21 17:36:29 -0400'
date_gmt: '2009-08-22 00:36:29 -0400'
categories:
- Uncategorized
tags:
- web/tech
- social web
- design
comments:
- id: 3243
  author: Open Web Protocols and Discussion Groups &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/03/08/open-web-protocols-and-discussion-groups/
  date: '2010-03-08 06:17:47 -0500'
  date_gmt: '2010-03-08 13:17:47 -0500'
  content: "[...] to get involved by getting feedback on a couple of protocol ideas
    I was batting around. One search like status that will attempt to deal with distributed
    search over federated servers, and the other meta [...]"
---
<p>Been doing a lot of thinking about open social media the past week or so since friendfeed, my favorite social site, got sold to facebook, one of my least favorite sites. One of the problems brought up in the <a href="http://friendfeed.com/openff">OpenFF</a> group I've been contributing to (ideas so far) is addressing the need of users for real time search.</p>
<p>Thus far businesses have solved this issue by keeping their pipelines centrally located for rapid searching. But this bottlenecks both bandwidth and total information flow to one location/limit. Users want to decouple their social connections from any one business so they can rely on their data portability and social connectivity regardless of liquidity events or mergers. <a href="http://openff.org/wiki/index.php/Main_Page">OpenFF</a> is an example of a user fueled desire to make this a reality, initially by supporting version 2 of the friendfeed API.</p>
<p>My solution to real time search over a federated network, or any distributed real time information system, is called "search like status" or SLS for short. SLS's implementation is to broadcast search in much the same way as a status messages by mimicking optimal information data response protocols. In terms of architecture, the messaging system can be implemented in any manner desired. Ultimately patterns matched by local hub or users are sent back to the searching user or host in the form of messages. These receipt messages are only sent if a match is found and are aggregated in an easy to display format at the end user. Local search caches allow for rapid return of recent searches, with additional searches being required for newly updated data.</p>
<p>A great implementation of a fast protocol is <a href="http://code.google.com/p/pubsubhubbub/">pubsubhubbub</a>. The PSHB information system is a multi-tiered architecture that allows for servers, hubs and users to rapidly propagate information in a distributed manner. For more info please consult</p>
<ul>
<li><span style="background-color: #ffffff;"> <a href="http://www.scripting.com/stories/2009/07/10/googlesPubsubhubbub.html">Dave Winer great high level description</a> and </span></li>
<li><span style="background-color: #ffffff;"><a href="http://www.louisgray.com/live/2009/07/pubsubhubbub-real-time-feeds-and-real.html">Louis Gray's link rich dictionary on pubsubhubub</a>. </span></li>
</ul>
<h6 class="zemanta-related-title" style="font-size: 1em;">Related articles by Zemanta</h6>
<ul class="zemanta-article-ul">
<li class="zemanta-article-ul-li"><a href="http://www.readwriteweb.com/archives/is_a_perfect_storm_forming_for_distributed_social_networking.php">Is a Perfect Storm Forming For Distributed Social Networking?</a> (readwriteweb.com)</li>
<li class="zemanta-article-ul-li"><a href="http://regulargeek.com/2009/08/10/why-did-facebook-buy-friendfeed/">Why Did Facebook Buy FriendFeed?</a> (regulargeek.com)</li>
</ul>

