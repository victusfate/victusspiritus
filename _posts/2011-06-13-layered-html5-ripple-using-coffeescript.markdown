---
layout: post
status: publish
published: true
title: Layered HTML5 Ripple using CoffeeScript
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9256
wordpress_url: http://www.victusspiritus.com/?p=9256
date: '2011-06-13 03:25:52 -0400'
date_gmt: '2011-06-13 10:25:52 -0400'
categories:
- Uncategorized
tags:
- web/tech
- coding
- visualization
- html5
- coffeescript
comments:
- id: 10153
  author: Peter Beddows
  author_email: pbeddows@missi.com
  author_url: http://www.missi.com/
  date: '2011-06-15 22:22:00 -0400'
  date_gmt: '2011-06-15 22:22:00 -0400'
  content: "Love the effect Mark. Ripples in the web page background: Very interesting
    and obviously you've put some work into setting this up so it is generous of you
    to share the results of your work. \n\nNow if only I could think of somewhere
    to use it, we'd be all set."
- id: 10154
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-06-15 22:42:00 -0400'
  date_gmt: '2011-06-15 22:42:00 -0400'
  content: "I was going to put it behind my blog header.\r\n\r\nThe base code was
    thanks to person I linked to, all I did was rewrite it in CoffeeScript and modify
    it to work in the background. The trick was scaling a small canvas with css to
    make it responsive."
- id: 10227
  author: The secret art of the tutorial &mdash; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2011/07/05/the-secret-art-of-the-tutorial/
  date: '2011-07-05 21:01:08 -0400'
  date_gmt: '2011-07-06 04:01:08 -0400'
  content: "[...] is my early experience with CoffeeScript. I&#8217;ve found it much
    easier to dive in with client side CoffeeScript examples which require only a
    browser and Jeremy Ashkenas&#8217; JavaScript [...]"
---
<p>This weekend I researched various methods for approximating the effect of rippling water. After reviewing a few great options I went with the effect shown <a href="http://www.nixuz.com:8080/html5/water/water.html">here at nixuz.com</a>.</p>
<p>I scaled the canvas element to the size of the background to speed computation, but further work will need to be done to pretty it up.</p>
<p>The <a href="http://victusfate.github.com/html5_layered_ripple/">html5_layered_ripple repo</a> and a snapshot of what it looks like so far:</p>
<p><a href="http://victusfate.github.com/html5_layered_ripple/"><img src="http://www.victusspiritus.com/wp-content/uploads/2011/06/html5_layered_ripple-1024x919.png" alt="" title="html5_layered_ripple" width="630" height="565" class="aligncenter size-large wp-image-9258" /></a></p>
<p>Warning: There are some minor UI tweaks I need to make (ie if you set the refraction or shading you have to reselect an image for the background).</p>
<p><b>Update:</b><br />
In my haste to rush out the door this morning I forgot to embed the key coffeescript. Here's a gist of that code:<br />
<script src="https://gist.github.com/1022646.js"> </script></p>
