---
layout: post
status: publish
published: true
title: Rocking Chair, Portable Realtime Feeds ala CouchDB
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 5910
wordpress_url: http://www.victusspiritus.com/?p=5910
date: '2010-11-12 13:52:49 -0500'
date_gmt: '2010-11-12 20:52:49 -0500'
categories:
- Uncategorized
tags:
- coding
- open standards
- open source
- CouchDB
comments:
- id: 7485
  author: ''
  author_email: support@readwriteweb.com
  author_url: ''
  date: '2010-11-13 10:39:00 -0500'
  date_gmt: '2010-11-13 10:39:00 -0500'
  content: Nice writeup!
- id: 7499
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-11-14 00:19:00 -0500'
  date_gmt: '2010-11-14 00:19:00 -0500'
  content: hey thanks, short and sweet are my weekend favorites.
---
<p><a href="http://www.victusspiritus.com/wp-content/uploads/2010/11/rockingchair.jpeg"><img src="http://www.victusspiritus.com/wp-content/uploads/2010/11/rockingchair.jpeg" alt="" title="rockingchair" width="229" height="220" class="aligncenter size-full wp-image-5911" /></a><br />
Imagine subscribing to your favorite real time feeds on the go, and having them automagically cached to your favorite local database. I like to think of portable feeds as a variant of Instapaper but for my rss reader. Look no further there's open source code that does just this.</p>
<p>In the past week or so <a href="http://twitter.com/julien51">Julien</a> of <a href="http://blog.superfeedr.com/">Superfeedr</a> hacked together a fork of <a href="https://github.com/tjgillies">Tyler Gillies'</a> and <a href="https://github.com/maxogden">Max Ogden's</a> <a href="https://github.com/maxogden/couchpubtato">Couchpubtato</a>. To see the app in action visit <a href="http://superfeedr.couchone.com/push/_design/push/index.html?utm_source=twitterfeed&utm_medium=twitter">superfeedr.couchone.com</a>. If you'd like to see the source code for Rocking Chair, the repo is at <a href="https://github.com/julien51/rocking-chair">Julien's github</a>.</p>
<p>Several apps serve precisely this type of function, but they may not be as web and network friendly as an HTTP responding database that you can bring with you. For starters I can replicate all my friends feeds very fast. Here's Max's write up that sums up why couchpubtato (and Rocking Chair) are so cool:</p>
<blockquote>
<h2>Why is this cool?</h2>
<p>So I reckon you have some old and busted RSS or ATOM feeds that you need to pull from whenever you want updates, right?</p>
<p>Well, little buddy, it's time to enter the world of push!</p>
<p>Hook your pull feeds into the magic that is PubSubHubbubb (superfeedr.com does this for you... for free!) and they will push to a specific PubSubHubbubb subscriber endpoint whenever they have new content.</p>
<p>You might be asking "where am I going to get a valid PubSubHubbubb subscriber endpoint to store all of these awesome feed pushes"? Well, i'm glad you asked!</p>
<p>With Couchpubtato, you can make any Couch database act like a valid PubSubHubbubb subscriber endpoint.</p>
<h2>I still don't get it</h2>
<p>Ok, so lets say you want to embed a feed of upcoming calendar events on your sweet blog, but the calendar page only has a junky RSS feed! You can use Superfeedr to push new RSS updates in realtime to a CouchDB of your choice, which turns your previously junky RSS feed into a full JSONP enabled API for maximum client side widget goodness!</p>
<p>Here's an example of this whole thingy working: I log all Portland, OR 911 calls and make them available as ActivityStreams here: http://pdxapi.com/pdx911/feed?descending=true&limit=5
</p></blockquote>
