---
layout: post
status: publish
published: true
title: 'Simple CSS Tricks: Gradients & Curved Divs'
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 4879
wordpress_url: http://www.victusspiritus.com/?p=4879
date: '2010-08-14 05:46:39 -0400'
date_gmt: '2010-08-14 12:46:39 -0400'
categories:
- Uncategorized
tags:
- victus media
- design
comments:
- id: 5913
  author: Browsers aren&#8217;t Operating Systems, but will Dominate as an Application
    Platform | Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/09/14/browsers-arent-operating-systems-but-will-dominate-as-an-application-platform/
  date: '2010-09-14 06:32:55 -0400'
  date_gmt: '2010-09-14 13:32:55 -0400'
  content: "[...] top of this, attractive features that will be in future standards
    (HTML5) like curved corners or dynamic gradients are supported in multiple browsers,
    but have different tags and interfaces. Native video support is [...]"
---
<p>[caption id="attachment_4900" align="aligncenter" width="300" caption="example of rounded corners and css gradients"]<a href="{{ site.url }}/assets/2010/08/Screenshot.png"><img class="size-medium wp-image-4900" title="Screenshot" src="{{ site.url }}/assets/2010/08/Screenshot-300x187.png" alt="" width="300" height="187" /></a>[/caption]</p>
<p style="text-align: left;">Yesterday I came across two simple techniques while working on mapme.heroku.com, an app that will help me ramp up quickly on displaying maps and getting location from just about any browser. The first is gradients defined as image backgrounds. Here's an example of code:</p>
<pre> background-image:
        -moz-linear-gradient(top,#00BFFF,#ffffff,#00ff00);</pre>
<p>The code splits the div it inhabits into 3 smooth color gradients for browsers which define mozilla linear gradients. To do the same thing for webkit based browsers:</p>
<pre>    background-image:
        -webkit-gradient(linear,
         left top,
         left bottom,
         color-stop(0.25, #00BFFF),
         color-stop(0.49, rgb(255,255,255)),
         color-stop(1.0, #00ff00));</pre>
<p>Colors can be added or removed in either definition, and if you want to support both mozilla and webkit browsers you can add both to the same style block:</p>
<pre>#welcometext {
    background-image:
        -moz-linear-gradient(top,#00BFFF,#ffffff,#00ff00); 
    background-image:
        -webkit-gradient(linear,
         left top,
         left bottom,
         color-stop(0.25, #00BFFF),
         color-stop(0.49, rgb(255,255,255)),
         color-stop(1.0, #00ff00));
}</pre>
<p>The second trick I came across was rounded corners for divs. Webkit defines this with border-radius and mozilla defines this as -moz-border-radius. Again to handle curved divs for multiple browser types simple define both:</p>
<pre>#welcometext {
    -moz-border-radius: 15px;
    border-radius: 15px;
}</pre>
<p>You can see examples of both of these effects at the sinatra based image browser <a href="http://knowsinatra.heroku.com">knowsinatra</a> and it's rails cousin <a href="http://imagebrowser.heroku.com">imagebrowser</a>.</p>
