---
layout: post
status: publish
published: true
title: Distributed Social App with CouchDB. Brilliant!
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 5375
wordpress_url: http://www.victusspiritus.com/?p=5375
date: '2010-10-05 05:00:08 -0400'
date_gmt: '2010-10-05 12:00:08 -0400'
categories:
- Uncategorized
tags:
- coding
- javascript
- open source
- CouchDB
comments:
- id: 6324
  author: The builders of couchappspora &raquo; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2010/10/07/the-builders-of-couchappspora/
  date: '2010-10-07 05:04:59 -0400'
  date_gmt: '2010-10-07 12:04:59 -0400'
  content: "[...] hacked together their own vision of an interface and CouchDB back
    end. I spotted the git repo on Tuesday morning while waiting for my wife to get
    out of a minor surgery (she&#8217;s fine). There are three active [...]"
---
<p><img src="http://www.victusspiritus.com/wp-content/uploads/2010/10/20101005-075608.jpg" alt="" width="350" height="250" /><br />
While learning how to best lay the groundwork for a shared media application, I happened upon an early alpha of a <a href="http://glitterbacon.couchone.com/couchappspora/_design/couchappspora/index.html">distributed social app on CouchDB</a>. The couchapp allows anyone to register and begin posting so try it out. There's no federation yet, but additional couch databases can be continuously replicated. The distributed nature of the application spawns by setting up two way replication or synchronization between multiple nodes. This is one of the benefits of couchDB that makes it a great system for media sharing, and why I've decided to build on it.</p>
<p>The couchapp was crafted by the skilled PDX web hacker <a href="http://www.twitter.com/maxogden">Max Ogden</a>. I know of Max's knack for building through my cofounder Tyler. While I've been busy reading docs on couchapp frameworks, Max has been busy crafting one app after another. This post is a tip of the hat to Mr. Ogden's work, good hacking.</p>
<p>The source can be found/forked <a href="http://github.com/maxogden/couchappspora">here on github</a>. Max implemented (cloned) the Diaspora interface protocol. But thats where the technical resemblance to the XMPP concept developed by the Diaspora team ends.</p>
<p><a href="http://www.victusspiritus.com/wp-content/uploads/2010/10/couchappspora_focused.png"><img class="aligncenter size-full wp-image-5393" title="couchappspora_focused" src="http://www.victusspiritus.com/wp-content/uploads/2010/10/couchappspora_focused.png" alt="" width="550" height="400" /></a></p>
<p>*update* Max mentioned he's also planning to make couchappspora fully ostatus compliant. Here's <a href="http://github.com/maxogden/ostatus-js">his github repo</a> for that effort.</p>
<blockquote><p>ostatus-js: an attempt to implement OStatus in JavaScript:<br />
note: This will most likely always require E4X</p>
<p>OStatus consists of the following protocols:</p>
<ul>
<li><span style="font-size: 13.3333px;">WebFinger</span></li>
<li><span style="font-size: 13.3333px;">PortableContacts</span></li>
<li><span style="font-size: 13.3333px;">Activity Streams</span></li>
<li><span style="font-size: 13.3333px;">PubSubHubBub</span></li>
<li><span style="font-size: 13.3333px;">Atom</span></li>
<li><span style="font-size: 13.3333px;">Salmon</span></li>
</ul>
</blockquote>
