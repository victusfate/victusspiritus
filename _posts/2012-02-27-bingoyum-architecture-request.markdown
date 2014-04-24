---
layout: post
status: publish
published: true
title: Bingoyum architecture request
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9961
wordpress_url: http://www.victusspiritus.com/?p=9961
date: '2012-02-27 04:12:54 -0500'
date_gmt: '2012-02-27 11:12:54 -0500'
categories:
- Uncategorized
tags:
- javascript
- coffeescript
- bingoyum
- couch
comments: []
---
<h2>The app</h2>
<p>I was thinking about how to best setup a project this morning. It will be composed of a couchDB editor app, a visual editor/GUI, and backbone hooks to the couch. </p>
<p>The editor is Dale Harvey's inception (freaking slick), and I was thinking of making that a git submodule to my fork of the tool. I was going to do the same for GUI/backbone app. </p>
<p>But couchapps require a very specific folder setup to deploy properly. Should I keep them as separate couch apps, and combine in a third app which utilizes them, or should I bring all the source together for one larger couchapp. Any and all all suggestions welcome.</p>
