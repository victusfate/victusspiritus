---
layout: post
status: publish
published: true
title: Duostack vs Nodester Node.js Hosting, Day Zero
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8756
wordpress_url: http://www.victusspiritus.com/?p=8756
date: '2011-05-10 06:26:03 -0400'
date_gmt: '2011-05-10 13:26:03 -0400'
categories:
- Uncategorized
tags:
- web/tech
- coding
- node.js
- coffeescript
comments:
- id: 10013
  author: Vississ
  author_email: vsss@bagaduce.com
  author_url: ''
  date: '2011-05-21 19:53:00 -0400'
  date_gmt: '2011-05-21 19:53:00 -0400'
  content: |-
     "Duostack gets the slight edge due to supporting coffee-script out of the box"

    In what sense in their support "out of the box"? Coffeescript needs to be compiled down to Javascript to run on Duostack.
- id: 10015
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-05-21 21:51:00 -0400'
  date_gmt: '2011-05-21 21:51:00 -0400'
  content: I had a simple server written in coffeescript and it just worked. On Nodester
    I'd had have to manually compile, not a biggy.
---
<p>This morning I'll take a peak at two competing node.js hosting providers. Both Duostack and Nodester were straightforward to install and configure, if only other configurations were so easy. My first impression was that Duostack gets the slight edge due to supporting coffee-script out of the box, but Nodester get's the service award and mentioned that coffee-script support is coming soon.<br />
[blackbirdpie url="https://twitter.com/nodester/status/67754811642220544"]</p>
<div class="hbox bluebox left">
<h1><a href="http://duostack.com">Duostack</a></h1>
<ol>
<li>instant sign up</li>
<li>
<pre>npm install duostack</pre>
</li>
<li>add duostack to path</li>
<li>
<pre>duostack create appname</pre>
</li>
<li>
<pre>git push duostack master</pre>
<p> and your app is deployed (supports node or rails) </li>
</ol>
<blockquote><p>
<b>Dependency Resolution on Duostack</b></p>
<p>Upon receiving a push of your app, the Duostack app compiler will look for a package.json file and install the listed dependencies into your app for deployment.</p>
<p>If the app compiler encounters an error installing dependencies, it will print a warning in the push output but still allow the app to boot.<br />
(<a href="http://docs.duostack.com/node/introduction">source</a>)
</p></blockquote>
</div>
<div class="hbox bluebox right">
<h1><a href="http://nodester.com">Nodester</a></h1>
<ol>
<li>sign up for a coupon</li>
<li>
<pre>npm install nodester-cli -g</pre>
</li>
<li>
<pre>nodester app create myapp</pre>
</li>
<li>
<pre>nodester app init myapp</pre>
</li>
<p>have an existing app?</p>
<li>
<pre>nodester app create myapp</pre>
</li>
<li>
<pre>nodester app info myapp</pre>
</li>
<li>
<pre>git remote add nodester
 the_url_returned_by_our_api</pre>
</li>
<li>
<pre>git push nodester master</pre>
</li>
<p>use npm modules?<br />
nodester npm install myapp express socket.io etc</p>
<p>nodester app start myapp</p>
<p>Nodester doesn't yet support coffee-script directly, but it can be hosted by translation to JavaScript.
</p></div>
<p><br/><br/><br/></p>
