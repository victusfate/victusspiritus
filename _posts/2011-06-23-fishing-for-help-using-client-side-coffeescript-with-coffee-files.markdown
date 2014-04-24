---
layout: post
status: publish
published: true
title: Fishing for help using Client Side CoffeeScript with .coffee files
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9330
wordpress_url: http://www.victusspiritus.com/2011/06/23/fishing-for-help-using-client-side-coffeescript-with-coffee-files/
date: '2011-06-23 05:01:35 -0400'
date_gmt: '2011-06-23 12:01:35 -0400'
categories:
- Uncategorized
tags:
- web/tech
- coding
- coffeescript
comments:
- id: 10177
  author: ''
  author_email: trevorburnham@gmail.com
  author_url: ''
  date: '2011-06-23 17:10:00 -0400'
  date_gmt: '2011-06-23 17:10:00 -0400'
  content: |-
    The code you posted should work fine. There is, however, an issue with Chrome, where for security reasons it won't fetch CoffeeScript files (or any other Ajax-requested files) from `file://`. (I mention this in the book.) Try your page in a non-Chrome browser, or use some kind of server software so that your files are on `localhost://` instead.

    By the way, my patch for coffee-script.js (or rather, someone else's improved version) has already been incorporated as of 1.1.0+, so you don't have to worry about CoffeeScript includes being inconsistently ordered anymore.
- id: 10178
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-06-23 17:18:00 -0400'
  date_gmt: '2011-06-23 17:18:00 -0400'
  content: "Oh yes, I ran into that and set up a script to open chromium with the
    option to access the local file system (--allow-file-access-from-files). But I
    may not have had that flag set when I hit the issue. \n\nThanks for stopping by
    Trevor (and yeah I caught that was fixed on the issue trail, surprised it took
    a few months to get that patch in)."
---
<p>As my client side CoffeeScript hacks grow larger<sup><a href="#notes">1</a></sup>, I'm finding the constraint of keeping all the code in html script tags wrapper on page to be awkward. One little project that I'm hoping to have time for this weekend requires combining several html5 canvas effects, they may share some common elements, and each is growing unwieldy for their separate html header tags.</p>
<p>Here's what I'd like to see in my html file:<br />
<script src="https://gist.github.com/1042426.js"> </script></p>
<p>So far I haven't got the above setup to work and have had to fall back on keeping all my CoffeeScript in the html file (yuck).</p>
<h2>Update</h2>
<p>After more searching I found trusty Trevor Burnham debugging and patching browser CoffeeScript in the <a href="https://github.com/jashkenas/coffee-script/issues/1054">following issue</a>:</p>
<blockquote>
<p>Under the patch, you can now write</p>
<pre><code>&lt;script type="text/javascript" src="coffee-script.js"&gt;&lt;/script&gt;
&lt;script type="text/coffeescript" src="one.coffee"&gt;&lt;/script&gt;
&lt;script type="text/coffeescript"&gt;
  console.log 'two'
&lt;/script&gt;
&lt;script type="text/coffeescript" src="three.coffee"&gt;&lt;/script&gt;
</code></pre>
<p>and be certain that <code>one.coffee</code> will run first, then the inline code, then <code>three.coffee</code>.</p>
<p>Note, however, that there are no guarantees with respect to the order of mixed JavaScript and CoffeeScript code, except that any JavaScript code that comes before <code>coffee-script.js</code> will of course run before any CoffeeScript. This should probably be mentioned in the docs.</p>
</blockquote>
<p>I recognize a simple solution is to compile the CoffeeScript to JavaScript once and just include it normally. I also understand that clients will be compiling CoffeeScript each time to JavaScript on their local systems, and this is a waste of clock cycles. But my goal is to have cleanly readable CoffeeScript available for each visitor, with dependencies limited to Jeremy's CoffeeScript interpreter and any web browser with JavaScript. It lowers the barrier to entry for folks who aren't comfortable with installing node and maintaining up to date packages, and allows CoffeeScript coding for folks who don't have administrative privileges on their local hosts.</p>
<p><a href="#notes" id="notes">Notes:</a></p>
<ol>
<li>Here are a few client side CoffeeScript hacks:
<ul>
<li><a href="http://www.victusspiritus.com/2011/05/30/clientside-coffeescript-with-jquery/">Client side intro</a></li>
<li><a href="http://victusfate.github.com/html5_layered_ripple/">Html5 Layered Ripple</a></li>
<li><a href="http://victusfate.github.com/html5_chaos/">html5 chaos</a></li>
</ul>
</li>
</ol>
