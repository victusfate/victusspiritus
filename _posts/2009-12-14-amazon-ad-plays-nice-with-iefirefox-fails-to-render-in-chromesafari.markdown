---
layout: post
status: publish
published: true
title: Amazon Ad Plays Nice with IE/Firefox, Fails to Render in Chrome/Safari
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 2520
wordpress_url: http://www.victusspiritus.com/2009/12/14/amazon-ad-plays-nice-with-iefirefox-fails-to-render-in-chromesafari/
date: '2009-12-14 05:49:49 -0500'
date_gmt: '2009-12-14 12:49:49 -0500'
categories:
- Uncategorized
tags:
- semantic
- victus media
- advertising
- google
- amazon
comments:
- id: 2094
  author: Tyler Gillies
  author_email: None
  author_url: http://twitter.com/tylergillies
  date: '2009-12-14 21:10:55 -0500'
  date_gmt: '2009-12-15 02:10:55 -0500'
  content: '"Amazon Affiliate lair." love it!'
- id: 2147
  author: Tyler Gillies
  author_email: None
  author_url: http://twitter.com/tylergillies
  date: '2009-12-15 04:10:55 -0500'
  date_gmt: '2009-12-15 09:10:55 -0500'
  content: '"Amazon Affiliate lair." love it!'
- id: 5656
  author: anonymous coward
  author_email: nopenope@nope.com
  author_url: ''
  date: '2009-12-14 19:00:00 -0500'
  date_gmt: '2009-12-14 19:00:00 -0500'
  content: stop spamming reddit.
---
<h2>Product Preview</h2>
<p>Amazon product links have an interesting optional functionality called Product Preview. It has had other arcane names in the past (link enhancer), but has a similar functionality to <a href="http://www.snap.com/">Snapshots</a>. Basically when you mouse over an enhanced link, the browser renders a small image with detailed information. </p>
<p>The function has a few nifty features:</p>
<ul>
<li>It shows the Amazon logo/frame that triggers more consumer trust than a random link</li>
<li>It gives latest pricing information</li>
<li>it shows a product image</li>
<li>it conserves page real estate</li>
</ul>
<h2>Getting it to work</h2>
<p>So after some html and scripting views of an old website (<a href="http://www.dreamsnare.com">my first</a>) both Tyler and I dug up the official documentation at the Amazon Affiliate lair. With some tweaking of the URL and the appended image we were in business on our end. Then we added the Amazon JavaScript and whala: </p>
<ul>
<li>It worked in Firefox</li>
<li>An empty Amazon box popped up on Chrome</li>
<li>It worked in Internet Exploder</li>
</ul>
<p>It worked in IE but not Chrome, (*engineering expletives deleted?!?*).<br />
Why had my beloved speed demon of a browser forsaken me? It turns out <a href="http://www.problogger.net/archives/2006/10/12/amazon-launches-product-preview-to-associates/">there's a known issue with Product Preview with WebKit browsers</a>. Problogger Darren Rowse (sharp fellow that I bumped into on Twitter a while back) discovered this almost three years ago. As you can witness, this has been a HOT BUTTON topic for the folks at Safari and Chrome land. It's a rendering problem they don't care to fix or that Amazon doesn't see value in working around.</p>
<p>My gut instinct is to punt and show the boxes in the widget all the time, and to revisit alternate designs that work cross browser and cross ad platform (Google, Microsoft, our own). Generic views my ass :).</p>
<h2>Why we looked at the design</h2>
<p>The <a HREF="http://victusmedia.com">Intelligent Media Manager</a> has a widget ad box that is in a continual state of improvement. In addition to planned and implemented semantic functional upgrades the base ad display was in need of spiffing up. </p>
<p>Before we hire on a web designer pro to make the ad box a sexy irresistable force of nature, we want to gather more information and gradually grow our user base. I figured an evening of elbow polish would help after some feedback from designer friend <a href="http://www.linkedin.com/pub/shana-carp">Shana Carp</a> (she wants to support our concept by hosting the box, but thinks it's a bit of an eyesore). Ideally the ad widget will be fully customizable by the host to allow for smooth thematic integration.</p>
