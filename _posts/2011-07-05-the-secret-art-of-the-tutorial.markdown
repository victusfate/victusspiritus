---
layout: post
status: publish
published: true
title: The secret art of the tutorial
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9612
wordpress_url: http://www.victusspiritus.com/?p=9612
date: '2011-07-05 09:59:27 -0400'
date_gmt: '2011-07-05 16:59:27 -0400'
categories:
- Uncategorized
tags:
- web/tech
- coding
comments:
- id: 10229
  author: Jim de Graff
  author_email: riverzak@gmail.com
  author_url: ''
  date: '2011-07-06 15:57:00 -0400'
  date_gmt: '2011-07-06 15:57:00 -0400'
  content: |-
    "Start small, build up in steps". My major beef is with turorials that do just that. For example, some time back I was looking for an example of how to use groups in a VB tree control. Several examples that I found were so overburdened with the details of the previous steps that the examples were useless. I finally got exactly what I needed from a coder on daniweb (www.daniweb.com) - a simple example that focused on ONLY the tree control - that within 10 minutes I had the code sample plugged into my existing application. I also now understand the working of groups.

    My second beef is with excessive attention to details. I used to work with someone who would explain a beach by describing each grain of sand on it (a common failing of the documentation on Microsoft sites). With that much attention to the minutiae, the lesson gets completely obscured.
- id: 10234
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-07-07 10:47:00 -0400'
  date_gmt: '2011-07-07 10:47:00 -0400'
  content: "Strong reason for a variety of tutorials Jim. So you would like to see
    more medium level dedicated tutorials? In your case you were more interested in
    a specific feature tutorial than an intro to a language or framework. Was that
    feature a complex case, or was it a fairly straight forward usage of groups?\r\n\r\nAppreciate
    the reminder that not all tutorials are introductory."
---
<p>For savvy folks who love learning, there's nothing quite like working through a polished interactive tutorial. Today's riff will focus on the importance of great documentation, and the qualities which separate superior experiences from failed documentation efforts.</p>
<p>In the last couple of years I've crawled through thousands of blog posts, web docs, how to guides, tech reviews, video tutorials, along with a couple dozen technical ebooks<sup><a href="#notes">1</a></sup>. I simply can't get enough quality documentation on languages, libraries, sdks and frameworks which kick start my enthusiasm and imagination.</p>
<p>I've developed a fine appreciation for well crafted tutorials while delving deeply into the world of modern tech docs. Master crafted guides <b>start small and build up in simple steps</b>, while focusing on the elegance and value of the specific tool under review. Installation and dependencies are boiled down to bare essentials to <b>remove any potential impedance</b> to adoption. </p>
<p>A moment of interruption during a first impression can turn off potential devs or trigger their attention to drift to other sources and technologies. Hackers are short on time, and quick to jump to another solution they can hastily patch together. </p>
<p>One recent example that highlights the advantage of minimized dependencies is my early experience with CoffeeScript. I've found it much easier to dive in with <a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/05/30/clientside-coffeescript-with-jquery/">client</a> <a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/06/13/layered-html5-ripple-using-coffeescript/">side</a> <a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/06/24/chaotic-coffeescript/">CoffeeScript</a> <a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/06/25/visualization-layered-like-music-tracks/">examples</a> which require only a browser and Jeremy Ashkenas' JavaScript interpreter, than to work through server apps which depend on node, several packages, along with databases and interfaces (redis, mongo, couch, etc). I'd love to become intimately familiar with all those layers and plan to dig into cs server apps, but at the beginning they're a distraction.</p>
<p>The critical resource for developers is not discovering sufficient material, but freeing up ample time to work through and understand relevant examples. Competition is fierce in the war to earn mind share from potential partners, and if you want to win it's worth the extra effort spent honing any tech tutorials or documents. Docs are the first and most important surface with which devs contact your technology, whether it's an open source library or an API so make them amazing and keep them up to date.</p>
<h2>Common Traits of Polished Tutorials</h2>
<p>I've danced about a few of the keys to effective documentation, and now it's time to boil those features down into one definitive hit list:</p>
<ul>
<li><b>Start with great technology:</b><br/>Document products that don't suck. If the library, language, or framework you're documenting is horrible, and you absolutely must document it...</li>
<p><br/></p>
<li><b>Focus on the good parts:</b><br/>Douglas Crockford did a fantastic job of highlighting the best aspects of JavaScript, learn from his example by diving into the best aspects of the tech you're reviewing</li>
<p><br/></p>
<li><b>Start small, build up in steps:</b><br/>Don't begin with the most complex example you can imagine just because it shows every possible configuration of a given tech. Start small with hello world, and build up by adding one tool at a time. As a tutorial author you're a tour guide. Bring devs along for a magic carpet ride by starting on the ground. A drive by pickup at Mach 1 makes for a messy start</li>
<p><br/></p>
<li><b>Minimize dependencies:</b><br/>The less I have to do to begin a tutorial the better, browser based walkthroughs are ideal. You don't have to include you're own c compiler but consider a binary instead of having devs build Erlang from scratch<sup><a href="#notes">2</a></sup></li>
<p><br/></p>
<li><b>Stylize the experience:</b><br/>Use large sparse elements, quality fonts, and generous whitespace to separate tutorial steps. Let me chew on precisely what's going on in one example before proceeding into something more complicated. Experienced devs can always fast forward simple steps and white space to jump into the deep end</li>
</ul>
<p>I could extend this list indefinitely with pet peeves and desired aspects of brilliant tutorials, but this is where reader feedback does a much better job. Please pitch in with documentation features you're enamored with, or mistakes that doc authors keep repeating. I continually strive to make my "how to" posts more fun and effective, and your input helps me achieve that goal.</p>
<p><a href="#notes" id="notes">Notes:</a></p>
<ol>
<li>I grab inexpensive ebooks on topics that I want more cohesive references on. My preferred format is ePub so that I own the file and can read it on my phone, tablet, laptop or desktop. But I have picked up a few texts that are Kindle only. Not all the books I purchase are for cover to cover reading, and unfortunately the references age quickly (ie I upgraded The Rails 2 Way to The Rails 3 Way because it was obsolete in under a year)</li>
<p><br/></p>
<li>Cheap shot on local CouchDB installations. The database and bundled http server depend on building a local Erlang environment and boy does it take a while. The build is only necessary if you're running something customized like GeoCouch. Nifty Mac, Linux, and Windows single server installs are available from <a href="http://www.couchbase.com/downloads">Couchbase</a>.</li>
</ol>
