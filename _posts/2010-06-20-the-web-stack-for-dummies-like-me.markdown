---
layout: post
status: publish
published: true
title: 'The Web Stack for Dummies (like me) '
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 4193
wordpress_url: http://www.victusspiritus.com/?p=4193
date: '2010-06-20 05:05:01 -0400'
date_gmt: '2010-06-20 12:05:01 -0400'
categories:
- Uncategorized
tags:
- web/tech
- coding
comments:
- id: 4585
  author: Dave Pinsen
  author_email: impossibledistances@yahoo.com
  author_url: http://steamcatapult.com/
  date: '2010-06-23 02:49:17 -0400'
  date_gmt: '2010-06-23 07:49:17 -0400'
  content: Figures you&#39;d post that pic when I&#39;m on Atkins. :)
- id: 4588
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-06-23 10:00:06 -0400'
  date_gmt: '2010-06-23 15:00:06 -0400'
  content: Darn this post title. Finally satisfied my pancake craving at IHOP last
    night.
- id: 4590
  author: Ron E Wolf
  author_email: ron.e.wolf@ieee.org
  author_url: ''
  date: '2010-06-23 14:32:01 -0400'
  date_gmt: '2010-06-23 19:32:01 -0400'
  content: i don&#39;t know if you want nerdy discussion on this. if so, your layer
    <br>    3. Web Page Markup, HTML <br>isn&#39;t really a layer in the sense that
    you are using it. instead HTML (and Flash & pdf & javascript ... are more of a
    transport here. the overwhelming % of HTML (etc) is generated by apps running
    in the app server (i think what you refer to as logic). also, there is an increasingly
    thick app layer (javascript, flash, java, ...)  running on the client. yes, in
    the browser container, but, a critical and significant layer, it &#39;should&#39;
    get a layer of its own.<br><br>____________Ron Wolf
- id: 4591
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-06-23 16:09:11 -0400'
  date_gmt: '2010-06-23 21:09:11 -0400'
  content: First off-&gt; always appreciate nerdy discussion, thanks for bringing
    it you pointed out some wrongness which is awesome.<br><br>I need to rethink the
    layers I describe, which is great for posts. I didn&#39;t give enough attention
    to the Client Browser, which includes some of what you refer to.<br><br>Fixing
    it now.
---
<p><a href="{{ site.url }}/assets/2010/06/PancakesAreBetterThanTheWeb.jpg"><img class="aligncenter size-medium wp-image-4208" title="PancakesAreBetterThanTheWeb" src="{{ site.url }}/assets/2010/06/PancakesAreBetterThanTheWeb.jpg" alt="" width="500" height="380" /></a><br />
<em>pancake stacks are better than web stacks</em></p>
<p>Let's follow some bytes as they make the journey from their source server  to a client system over <a class="zem_slink" title="Hypertext Transfer Protocol" rel="wikipedia" href="http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol">HTTP</a>.</p>
<ol>
<li>Server Hardware</li>
<li>Server Software</li>
<li>Script + Web Page Markup</li>
<li>Routing Hardware/Network</li>
<li>Client Browser</li>
<li>Client Hardware</li>
</ol>
<h2>Choice layers explained</h2>
<p><strong>Server Software</strong></p>
<ul>
<li>App Server
<ul>
<li>Logic/Algorithm</li>
<li>Web Framework</li>
<li>ORM</li>
<li>Database</li>
</ul>
</li>
<li>Web Server (Reverse Proxy)</li>
</ul>
<p>The App Server creates the dynamic web content for a site and is the culmination of customized logic that leverages a web framework, ORM, and database to serve up web pages.</p>
<p><a href="http://en.wikipedia.org/wiki/Web_application_framework">Web Framework</a> defined:</p>
<blockquote><p>A Ruby framework is collection of pre-written libraries, functions and controls that can be downloaded and used to make your programming task easier. In addition to a time saving, there is also a significant benefit in terms of programming efficiency and implicitly a more consistent programming style (since so much is pre-defined, one begins to use or utilize the paradigm of the underlying framework when writing a program)</p></blockquote>
<p><a href="http://en.wikipedia.org/wiki/Object-relational_mapping">ORM</a> defined:</p>
<blockquote><p>Object-relational mapping (ORM, O/RM, and O/R mapping) in computer software is a programming technique for converting data between incompatible type systems in relational databases and object-oriented programming languages. This creates, in effect, a "virtual object database" that can be used from within the programming language. There are both free and commercial packages available that perform object-relational mapping, although some programmers opt to create their own ORM tools.</p></blockquote>
<p><a href="http://code.alexreisner.com/articles/anatomy-of-a-ruby-web-application.html">Web server</a> <a href="http://en.wikipedia.org/wiki/Reverse_proxy">Reverse Proxy</a> defined:</p>
<blockquote><p>Another Web Server?</p>
<p>At this point you may be wondering why people are talking about using Apache or Nginx in their stack. Don’t we already have a web server? We do, but the Ruby app server is not a full-featured web server, and it’s not very good at sending images and other kinds of static files (in fact all app servers are terrible at this, which is why it’s better to call them “app servers” than “web servers,” though the two terms are often used interchangeably). So what we want to do is use a general purpose web server for static files, and pass other requests along to our app server.</p>
<p>This is one of the most complicated and least standardized parts of Ruby web app configuration. Serving static files and handing off requests doesn’t take much processor power, so for a small web site our web server shouldn’t be too busy. The app server, on the other hand, is running our complicated Ruby application, and could be quite busy. For this reason one usually deploys multiple app servers (listening on different ports) for the web server to choose from when a request comes in. The process of handing requests off to these servers is called reverse proxy.</p>
<p>(If you’ve worked for a large company you’re probably familiar with accessing the Internet through a forward proxy server. Forward proxy is for outbound—client-side—requests, reverse proxy is for inbound—server-side—requests.)</p></blockquote>
<p>Ron called out an incorrect mixing of layers, so here's a shot at clearing up the discrepancy.<br />
<strong>Script + Web Page Markup</strong></p>
<ul>
<li>content (text, audio, video)</li>
<li>Graphics, Image editing</li>
<li>CSS styling</li>
<li>scripting (Javascript/AJAX)</li>
<li>HTML page</li>
</ul>
<p>Routing Hardware/Network Layer<br />
<strong>Client Browser</strong></p>
<ul>
<li>script interpreted at Client side (Javascript/AJAX)</li>
<li>final HTML page rendered and interpreted</li>
</ul>
<h2>Simple Example of Server Software</h2>
<p><a href="http://www.sinatrarb.com/intro.html">Sinatra</a> (framework) using <a href="http://datamapper.org/">Datamapper</a> (ORM) with <a href="http://www.sqlite.org/">Sqlite</a> (database) &amp; <a href="http://code.macournoyer.com/thin/">Thin</a> (web server)</p>
<p>References:</p>
<ul>
<li>The last time I talked about HTTP details was a <a href="http://victusfate.github.io/victusspiritus/uncategorized/2009/07/14/peer-to-peer-parallel-networking-for-your-iphone/">Peer 2 Peer notion</a></li>
<li>Alex Reisner's <a href="http://code.alexreisner.com/articles/anatomy-of-a-ruby-web-application.html">Anatomy of a Ruby Web Application</a></li>
<li>I was happy to get additional inspiration for this post from <a href="http://www.solosignal.com/solo-signal-series-the-web-stack-explained">this SoloSignal.com post</a> after a little searching. Here's Solo's web stack:
<ol>
<li>Physical Server and Infrastructure</li>
<li>Web Server Software</li>
<li>Database Management System</li>
<li>Business Logic Programming</li>
<li>HTML and Markup</li>
<li>Cascading Style Sheets</li>
<li>Graphic Design</li>
<li>Client-side Scripting</li>
</ol>
</li>
</ul>

