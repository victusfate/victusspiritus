---
layout: post
status: publish
published: true
title: State Propagation with Multiple Databases
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 5233
wordpress_url: http://www.victusspiritus.com/2010/09/21/state-propagation-with-multiple-databases/
date: '2010-09-21 04:28:13 -0400'
date_gmt: '2010-09-21 11:28:13 -0400'
categories:
- Uncategorized
tags:
- web/tech
- victus media
- coding
- javascript
- CouchDB
- databases
comments: []
---
<p><a href="http://victusfate.couchone.com/pic/_design/pic/_list/images/main"><img class="aligncenter size-full wp-image-5236" title="Pics" src="http://www.victusspiritus.com/wp-content/uploads/2010/09/Pics.png" alt="" width="500" height="280" /></a>Between a few stolen moments last night and early this morning, I was able to tweak the photo sharing app, <a href="http://victusfate.couchone.com/pic/_design/pic/_list/images/main">Pics</a>. One open issue, I may have borked Pics' upload interface this morning by commenting out a bit.ly url shrinking call.</p>
<p>The files I cared about most in the local couchapp were moo.html, Tyler's template for uploading files, and image.js, the specific JavaScript for creating the image array html. There's also a style sheet I'll need to track down if I want to customize the interface later.</p>
<p>I initially cloned the couchapp directory from a couchDB (please pardon any url errors, I'll update if needed when I get home):</p>
<pre>couchapp clone http://(server)/(database)/_design (dir name)</pre>
<p>After creating an empty database locally with Futon, I made changes and iteratively pushed them to my local couchDB:</p>
<pre>couchapp push http://localhost:5984/(database)</pre>
<p><em>The magic is in how state changes propagate</em></p>
<p>Late yesterday evening I continuously replicated a localhost couchDB to a remote one on couchone.com. Then I setup continuous replication back from the remote couch to my localhost. Two way continuous replication communicates state changes between either database's documents and design code (which is itself a document), providing synchronization. I haven't done tests to see how efficiently thousands or more remote nodes synchronize yet.</p>
<p>I extended the relationship to another couchone.com database so Michelle would have her own photo app site, and synchronized it with my remote couchDB. Changes to Michelle's couch propagated back to my couchone server, which propagated back to my localhost, all within a moment. Daisy chaining nodes worked flawlessly. I needed to manually refresh the browser, but I should be able to update part of the view if represented data changes, we'll see.</p>
<p><em>What's next</em></p>
<p>Besides mimicking features of peer to peer distributed file sharing systems (torrents), there are a few basic tasks I'll focus on this week. Loading directory trees of documents at once, as well as dumping multiple files to local disk would make use easier. I'd like to jazz up the interface to handle folders and/or organization tags and labels. Shared file repos could be browsed at a high level, likely as separate databases to enable independent synchronization. This enables sharing different media with my wife, my family, with Tyler, and and with my other friends. This form of segregated synchronization plays well with the different social groups I interact with.</p>
<p>Most production apps require some kind of authentication, so I'll add that as well. After that I'll investigate file support to enable sharing, showing (and editing?) additional media formats: video, music, PDF, doc, ePub, or anything that's easy to do in a browser.</p>
<p>Like it? Go ahead and "fork it" by cloning it to your own local or couchone.com CouchDB (<a href="http://www.victusspiritus.com/2010/09/04/first-impressions-of-sitting-a-web-app-on-couchdb/">installation</a> help).</p>
