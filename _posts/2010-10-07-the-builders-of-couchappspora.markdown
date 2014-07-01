---
layout: post
status: publish
published: true
title: The builders of couchappspora
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 5407
wordpress_url: http://www.victusspiritus.com/?p=5407
date: '2010-10-07 05:04:54 -0400'
date_gmt: '2010-10-07 12:04:54 -0400'
categories:
- Uncategorized
tags:
- social web
- open design
- coding
- javascript
- CouchDB
- couchappspora
comments:
- id: 6326
  author: Kevin Marshall
  author_email: falicon33@gmail.com
  author_url: http://blog.botfu.com
  date: '2010-10-07 13:30:00 -0400'
  date_gmt: '2010-10-07 13:30:00 -0400'
  content: Cool...you may also want to check into the efforts of http://telehash.org
    ... really cool stuff.
- id: 6327
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-10-07 14:12:00 -0400'
  date_gmt: '2010-10-07 14:12:00 -0400'
  content: Roger that, thanks for the heads up.
- id: 6338
  author: iN8sWoRLd
  author_email: nate@in8sworld.net
  author_url: http://in8sworld.net/
  date: '2010-10-08 11:09:00 -0400'
  date_gmt: '2010-10-08 11:09:00 -0400'
  content: |-
    I set up an account on a running alpha version of Diaspora running at:<a href="http://openspora.com/people/4c97e1865346806cc3000010" rel="nofollow">http://openspora.com/people/4c97e1865346806cc3000010</a>
    Is couchDB the official database for this project or are you talking about a fork?
---
<p>If you haven't heard already, there's a storm brewing on the distributed social web and it's being lead by a few hackers in Portland. They're building a distributed social app in response to the public interest for alternatives to centralized servers. They've taken the concept of Diaspora and hacked together their own vision of an interface and CouchDB back end. I spotted the git repo on <a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/10/05/distributed-social-app-with-couchdb-brilliant/">Tuesday morning</a> while waiting for my wife to get out of a minor surgery (she's fine). There are three active contributors to the project already, and I'm anxious to find a place to chip in.</p>
<p><i>Quick Repo Tracking on GitHub</i></p>
<p>As I've mentioned before Max Ogden's <a href="http://github.com/maxogden/couchappspora">couchappspora repo</a> is the first I came across, and he's the project lead/code merger. Jesse Hallet has made a number of commits to another <a href="http://github.com/hallettj/couchappspora">fork of the app</a>. Tyler Gillies is hacking away at <a href="http://github.com/tjgillies/couchappspora">his fork</a> and debugging pubsubhubbub implementation this morning. I can see Tyler's tests on twitter, and just now he posted <a href="http://twitter.com/#!/tylergillies/status/26639632108">realtime federation is live</a>. The app currently takes remote status.net compliant messages and posts them to couchappspora, but the reverse isn't built yet.<br />
<a href="http://twitter.com/#!/tylergillies/status/26639632108"><img src="{{ site.url }}/assets/2010/10/couchappspora_realtime_federation_live.png" alt="" title="couchappspora_realtime_federation_live" width="500" height="350" class="aligncenter size-full wp-image-5408" /></a></p>
<p>These guys are all talented PDX hackers so I expect rapid feature development and to learn a bunch from keeping track of the code changes.</p>
