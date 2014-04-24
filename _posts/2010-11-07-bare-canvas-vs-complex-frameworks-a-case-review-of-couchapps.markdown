---
layout: post
status: publish
published: true
title: Bare Canvas vs Complex Frameworks, a case review of couchapps
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 5861
wordpress_url: http://www.victusspiritus.com/?p=5861
date: '2010-11-07 06:04:20 -0500'
date_gmt: '2010-11-07 13:04:20 -0500'
categories:
- Uncategorized
tags:
- coding
- design
- CouchDB
- couchappspora
comments:
- id: 7604
  author: Where do you get your best work done? &raquo; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2010/11/26/where-do-you-get-your-best-work-done/
  date: '2010-11-26 05:58:23 -0500'
  date_gmt: '2010-11-26 12:58:23 -0500'
  content: "[...] ideal: motion, quiet background white noise, cozy space. As far
    as software utilities go, I feel a cultural fit with sammy on couch app, but haven&#8217;t
    used it yet beyond the simplest of intro apps. Beyond [...]"
---
<p>Over the past couple of months I've gotten a taste of <a href="http://couchdb.apache.org/docs/intro.html">CouchDB</a>, the <a href="http://couchapp.org/page/index">couchapp</a> framework, and a chance to explore several superb <a href="http://couchapp.org/page/list-of-couchapps">applications</a>*. My biggest hurdle to doing anything useful with CouchDB was (and still is) totally understanding the couchapp file structure. Couchapp is a utility written in python that creates a framework for placing applications within, and extracting applications out of couchDBs. The benefit of couchapp over alternative web frameworks that utilize couchDB as a backend, is portability. The application becomes embedded and works anywhere couchDB does (servers, replicated local couchDBs, etc).</p>
<p>Here's the default file tree for an application created by couchapp init:<br />
<a href="http://www.victusspiritus.com/wp-content/uploads/2010/11/Screen-shot-2010-11-07-at-5.55.20-AM.png"><img src="http://www.victusspiritus.com/wp-content/uploads/2010/11/Screen-shot-2010-11-07-at-5.55.20-AM.png" alt="" title="Screen shot 2010-11-07 at 5.55.20 AM" width="268" height="549" class="aligncenter size-full wp-image-5863" /></a><br />
<a href="http://www.victusspiritus.com/wp-content/uploads/2010/11/Screen-shot-2010-11-07-at-6.14.00-AM.png"><img src="http://www.victusspiritus.com/wp-content/uploads/2010/11/Screen-shot-2010-11-07-at-6.14.00-AM.png" alt="" title="Screen shot 2010-11-07 at 6.14.00 AM" width="268" height="977" class="aligncenter size-full wp-image-5866" /></a><br />
As you can observe the basic couchapp is composed of 34 directories and 59 files. If like myself you prefer a bare canvas to begin development you'll be a little overwhelmed by the file and functional breakdown. </p>
<p><i>Craving a cleaner canvas</i></p>
<p>Last weekend while strolling about Bayard cutting I wondered how feasible putting something simple like Sammy.js in front of couchDB would be. A quick search revealed that <a href="http://twitter.com/rmetzler">Richard Metzler</a> and <a href="http://www.quirkey.com/blog/">Aaron Quint</a> had hacked together <a href="https://github.com/quirkey/soca">soca</a> (sammy on couch app), precisely the type of app framework I was seeking (implemented as a ruby gem). Here's a look at the bare soca file tree:<br />
<a href="http://www.victusspiritus.com/wp-content/uploads/2010/11/Screen-shot-2010-11-07-at-5.54.48-AM.png"><img src="http://www.victusspiritus.com/wp-content/uploads/2010/11/Screen-shot-2010-11-07-at-5.54.48-AM.png" alt="" title="Screen shot 2010-11-07 at 5.54.48 AM" width="248" height="364" class="aligncenter size-full wp-image-5869" /></a><br />
From this image you can see 8 directories and 14 files. Soca sacrifices the ability to extract the application from an existing couchDB but gains in both flexibility for app designers to place files where they prefer, as well as much more compact set of files which capture the interaction of the app.</p>
<p>The design advantage is freedom that comes with choices between optional frameworks. It's not unlike the relationship Sinatra has with Rails. Both frameworks have their benefits, but appeal more to specific developers or have a better fit with certain applications.</p>
<p><i>But wait there's more, node.js for writing couchapps</i></p>
<p>While writing this post I came across <a href="http://twitter.com/mikeal">Mikeal Rogers'</a> couchapp toolkit, <a href="https://github.com/mikeal/node.couchapp.js">node.couchapp.js</a>. As of yet I have no idea how to create apps with it, but I've reinstalled node on my iMac and Air since my Ubuntu desktop is on the road to retirement. Juggernaut is powered down. I may install Mac OS X and hackintosh it for my folks. </p>
<p>Would appreciate your feedback in the comments here or on the <a href="http://news.ycombinator.com/item?id=1879258">HackerNews reactions</a>.</p>
<p>Notes:<br />
* = Related posts</p>
<ul>
<li><a href="http://www.victusspiritus.com/2010/09/04/first-impressions-of-sitting-a-web-app-on-couchdb/">First Impressions of Sitting a Web App on CouchDB</a></li>
<li><a href="http://www.victusspiritus.com/2010/09/19/reckless-photo-couchdb-app-in-60-seconds/">Reckless Photo CouchDB App in 60 seconds</a></li>
<li><a href="http://www.victusspiritus.com/2010/09/21/state-propagation-with-multiple-databases/">State Propagation with Multiple Databases</a></li>
<li><a href="http://www.victusspiritus.com/2010/10/05/distributed-social-app-with-couchdb-brilliant/">Distributed Social App with CouchDB. Brilliant!</a></li>
<li><a href="http://www.victusspiritus.com/2010/10/07/the-builders-of-couchappspora/">The builders of couchappspora</a></li>
</ul>
