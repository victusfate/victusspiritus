---
layout: post
status: publish
published: true
title: Reckless Photo CouchDB App in 60 seconds
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 5214
wordpress_url: http://www.victusspiritus.com/?p=5214
date: '2010-09-19 11:47:23 -0400'
date_gmt: '2010-09-19 18:47:23 -0400'
categories:
- Uncategorized
tags:
- coding
- javascript
- CouchDB
comments:
- id: 7435
  author: Bare Canvas vs Complex Frameworks, a case review of couchapps &raquo; Victus
    Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2010/11/07/bare-canvas-vs-complex-frameworks-a-case-review-of-couchapps/
  date: '2010-11-07 06:51:40 -0500'
  date_gmt: '2010-11-07 13:51:40 -0500'
  content: "[...] Reckless Photo CouchDB App in 60 seconds [...]"
---
<p>Assumption: you have couchapp and couchDB installed, see <a href="http://www.victusspiritus.com/2010/09/04/first-impressions-of-sitting-a-web-app-on-couchdb/">this post</a></p>
<p>Disclaimer: While I've read a bunch about couch's background, I have yet to setup any apps. Today's challenge is to set one up in 60 seconds and blog about it (in a much longer time).</p>
<h2>step one</h2>
<p><em>Clone somebody else's app to see the structure</em></p>
<p>I cloned <a href="http://tyler.couchone.com/pic/_design/pic/moo.html">Tyler's pic app</a>, from <a href="http://couchone.com">CouchOne</a>.  I just realized Tyler may enjoy Dead Can Dance as well.</p>
<pre>couchapp clone http://victusfate.couchone.com/pics/_design/pic pic</pre>
<p>If you point clone to a couchapp it grabs a file tree structure that looks like this:</p>
<pre> .
   |-_attachments
   |---style
   |-evently
   |---items
   |-----_changes
   |---profile
   |-----profileReady
   |-------selectors
   |---------form
   |-lists
   |-shows
   |-template
   |-updates
   |-vendor
   |---couchapp
   |-----_attachments
   |-----docs
   |-----evently
   |-------account
   |---------loggedIn
   |---------loggedOut
   |---------loginForm
   |-----------selectors
   |-------------form
   |---------signupForm
   |-----------selectors
   |-------------form
   |-------docs
   |---------index
   |---------topic
   |-----------edit
   |-------------_init
   |---------------selectors
   |-----------------a.edit
   |-----------------a.run
   |-------profile
   |---------loggedOut
   |---------noProfile
   |-----------selectors
   |-------------form
   |---------profileReady
   |-----lib
   |-views
   |---main
   |---recent-items</pre>
<p>That's more than I want to care about off the bat. Let's see if there's someplace I can stick all my photos without thinking.</p>
<p>The important aspects of accessing CouchDB are well articulated by <a href="http://guide.couchdb.org/editions/1/en/index.html">Noah Slater's definitive guide</a> (I now have the pdf, Kindle version, and iOS app). You can complain about your pain points directly to <a href="http://groups.google.com/group/tumbolia/">Noah here at his mailing list</a> but be nice and RTFM first. My immediate difficulties included:</p>
<ul>
<li><span style="font-size: 15.8333px;">having to manually check all the document members accessed in an if block for any map functions (think keyword searching a B Tree)</span></li>
<pre>function(doc) {
    var store, price, value;
    <strong>if (doc.item && doc.prices)</strong> {
        for (store in doc.prices) {
            price = doc.prices[store];
            value = [doc.item, store];
            emit(price, value);
        }
    }
}</pre>
<li><span style="line-height: 23px;">manually calling get to return a number of available local CouchDB UUIDs. Why can't posting return UUIDs, and identify documents by human readable concepts so I don't have to think about Bacon as "6e1295ed6c29495e54cc05947f18c8af" with _rev version "1-2902191555"</span></li>
<li><span style="line-height: 23px;">block writes are "penalized" because incremental document writes get in quicker forcing the last one to write to resolve conflict issues "whoever saves a change to a document first, wins.</span><span style="line-height: 23px;">"</span></li>
</ul>
<p>I'm all out of time at the moment but you can at least see Tyler's variant of the couchapp and I'll get back to tweaking my local version and documenting later. Looking forward to attaching image files later tonight.</p>
