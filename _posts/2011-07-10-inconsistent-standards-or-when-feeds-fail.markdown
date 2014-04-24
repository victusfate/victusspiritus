---
layout: post
status: publish
published: true
title: Inconsistent Standards or When Feeds Fail
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9657
wordpress_url: http://www.victusspiritus.com/?p=9657
date: '2011-07-10 14:13:30 -0400'
date_gmt: '2011-07-10 21:13:30 -0400'
categories:
- Uncategorized
tags:
- web/tech
- open design
- coding
- open standards
- open source
- API
comments: []
---
<p>One of the biggest time sinks I encountered while hacking the <a href="http://www.victusspiritus.com/2011/07/09/coffeescript-tracker/">CoffeeScript Tracker 0.0</a> was errors with response data. The CoffeeScript that hit dedicated APIs for the most part just worked, and the closer the interaction was to pure RESTful http the better. But problems arose when querying rss and atom feeds due to inconsistencies between the formats.</p>
<p>The YQL or <a href="http://developer.yahoo.com/yql/">Yahoo Query Language</a> was what I attempted to use to provide a standard feed interface. Response formats returned to the callback functions varied at the top with <code>data.response.entries</code> or <code>data.response.results</code>. Then within these json structures the entries and results had keys to describe urls. This lead to a variety of handlers and comparisons like <code>obj.link.href</code>, <code>obj.link[0].href</code>, <code>obj.origLink</code>, etc. The differences arise between atom, rss, version releases, and the particular provider. In theory I could write or find a JavaScript/CoffeeScript Swiss army knife of feed parsing, much like the fine <a href="http://nokogiri.org/">Nokogiri</a> Ruby gem I long took for granted.</p>
<p>It's sad when feeds, the open "lingua franca" of the Internet, are such a mess that hitting unique APIs is both simpler and more reliable. At least with feeds the formats have a slower divergence rate compared to one shot APIs, but middleware is advised when juggling with variations. </p>
