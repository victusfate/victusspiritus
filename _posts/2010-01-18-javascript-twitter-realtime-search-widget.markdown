---
layout: post
status: publish
published: true
title: Javascript Twitter Realtime Search Widget
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 2764
wordpress_url: http://www.victusspiritus.com/?p=2764
date: '2010-01-18 05:30:44 -0500'
date_gmt: '2010-01-18 12:30:44 -0500'
categories:
- Uncategorized
tags:
- coding
- javascript
comments: []
---
<p>Part of Social Gravity, a new interface we're building for social data, relies on a clean search portal to track entities/hashtags. After browsing through several remote scripts options I decided on the <a href="http://twitter.com/goodies/widget_search">offical Twitter search widget</a> which is functional, branded, but limited in how much we can adapt it. The alternative was modifying a simple but easy to understand script example, the <a href="http://tutorialzine.com/2009/10/jquery-twitter-ticker/">jquery Twitter ticker</a>. Our baseline is the official Twitter widget code, while I explore what can be done with the raw JavaScript interface to the pipeline of data. Even if the script I write gets discarded (which is likely), the skill of slightly more competent JavaScript coding will come in handy.</p>
<p>After a number of hours yesterday afternoon/evening (mostly reading up on JavaScript &amp; jquery), I ended up with a self updating modified Twitter search widget (it's not super clean as I'm learning the basics). It would be easy to plug this into rails or any other web framework. I couldn't get a clean looking version of the source while on my phone (default blogging platform), but I'll insert it below as a placeholder.</p>
<p>The changes I made were to demo.html and script.js. In demo.html I deleted the loading image div so that tweets aren't covered up. In script.js I changed and added a few functions:</p>
<p><script src="https://gist.github.com/823854.js?file=sample%20twitter%20real%20time%20search"></script></p>
<p>TweetTick is the pulse function which asks if there are any new matching search results from all or a subset of users. The format function updates the existing search results with the first of the results and redisplays the list with update times.</p>
<p>The github repo is available <a href="https://github.com/victusfate/TwitterRealTimeSearchWidget">here</a> and you can see the widget live in the iframe below and at this <a href="http://victusfate.github.com/TwitterRealTimeSearchWidget/">twitter real time search demo site</a>.</p>
<p>[iframe http://victusfate.github.com/TwitterRealTimeSearchWidget/ 500 800]</p>
<h6 class="zemanta-related-title" style="font-size: 1em;">Related articles by Zemanta</h6>
<ul class="zemanta-article-ul">
<li class="zemanta-article-ul-li"><a href="http://www.nofluffjuststuff.com/blog/matthias__wessendorf_/2010/01/flexible_ads__combining_popups_with_activedataservice?utm_source=blogitem&amp;utm_medium=rss&amp;utm_campaign=blogrss">Flexible ADS - Combining popups with ActiveDataService</a> (nofluffjuststuff.com)</li>
<li class="zemanta-article-ul-li"><a href="http://thenextweb.com/apps/2010/01/22/twitter-launches-trends-area/">Twitter launches Trends for YOUR Area.</a> (thenextweb.com)</li>
<li class="zemanta-article-ul-li"><a href="http://www.twitterrati.com/2010/01/24/twitter-just-buy-mr-tweet/">Twitter: Just Buy Mr. Tweet</a> (twitterrati.com)</li>
</ul>

