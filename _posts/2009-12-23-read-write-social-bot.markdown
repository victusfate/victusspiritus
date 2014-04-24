---
layout: post
status: publish
published: true
title: Read Write Social Bot
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 2612
wordpress_url: http://www.victusspiritus.com/2009/12/23/read-write-social-bot/
date: '2009-12-23 05:30:44 -0500'
date_gmt: '2009-12-23 12:30:44 -0500'
categories:
- Uncategorized
tags:
- search
- web/tech
- semantic
- victus media
comments:
- id: 2342
  author: Tyler
  author_email: tjgillies@gmail.com
  author_url: tylers-blog.heroku.com
  date: '2009-12-23 15:04:40 -0500'
  date_gmt: '2009-12-23 20:04:40 -0500'
  content: thanks for the helpful links!
- id: 2343
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2009-12-23 15:34:52 -0500'
  date_gmt: '2009-12-23 20:34:52 -0500'
  content: What&#39;s a good page for me to link to when I reference your name. What&#39;s
    your HQ blog, idea platform?
- id: 2345
  author: Tyler
  author_email: tjgillies@gmail.com
  author_url: tylers-blog.heroku.com
  date: '2009-12-24 06:09:56 -0500'
  date_gmt: '2009-12-24 11:09:56 -0500'
  content: Tylergillies.mp<br><br>On Wednesday, December 23, 2009, Disqus
- id: 2730
  author: Failx3, Win! &raquo; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2009/12/28/failx3-win/
  date: '2010-01-24 17:13:25 -0500'
  date_gmt: '2010-01-25 00:13:25 -0500'
  content: "[...] set about a task that I&#8217;ve never seen done before. An interactive
    social search bot, that &#8220;lives&#8221; on the web. My hope is that this type
    of tool will be remarkable enough [...]"
---
<h2><strong>Update: Some breaking news that's fantastic</strong></h2>
<p>The <a class="zem_slink" title="Zemanta" rel="homepage" href="http://www.zemanta.com">Zemanta</a> team (ala @<a class="zem_slink" title="Andraž Tori" rel="twitter" href="http://twitter.com/andraz">Andraz</a>) has crafted <a href="http://test.infoblow.zemanta.com/infoblow/galaxy/">Galaxy</a>, a relational connector between Zemanta and <a class="zem_slink" title="DBpedia" rel="homepage" href="http://dbpedia.org/About">DBpedia</a> + <a class="zem_slink" title="freebase" rel="homepage" href="http://www.freebase.com/">Freebase</a>. This could save me a jump time from entities to connectors! Just heard about it from <a href="http://twitter.com/andraz/status/6964008502">twitter</a>, here's <a href="http://www.zemanta.com/blog/api-showcase-linked-galaxy/">the full blog post </a>with all the cool details. Unfortunately there's no API for such a connection, so we'll have to do it ourselves anyway. At least I'm aware of the DBpedia and Freebase now.</p>
<h2>Crafting a bot that can read & respond with a personality</h2>
<p>Artificial intelligence has come a long way in my lifetime, certainly specialized processing such as chess programs have surpassed human cognitive ability. Late yesterday, inspired by the work of my colleague Tyler, I proceeded down a path few have tread successfully. The challenge chosen is to craft an interactive social bot.</p>
<p>Here are the modules I'm using and why I believe it's possible:<br />
1) semantic entity extraction allows us to quickly identify a category/type and specific person, place or thing<br />
2) relational semantic lookups give multiple connections between entities in the form of verbs or analogies<br />
3) <a class="zem_slink" title="Corpus linguistics" rel="wikipedia" href="http://en.wikipedia.org/wiki/Corpus_linguistics">corpus linguistics</a> or a search API can weave a series of entities and verbs together<br />
4) simple replacement rules can serve as the style, speech, or accent.<br />
5) the spooky hard part is making all these pieces play together. I have some ideas, but I'm interested to see what others are cooking up.</p>
<h2>Why?</h2>
<p>In an effort to improve the appeal and utility of the <a href="http://victus-imm.heroku.com">IMM</a>, we're exploring new ways of looking at social search. An interface that one can send and recieve messages from is both desirable and natural.</p>
<p>The <a href="http://hunch.com">Hunch</a> interface, and API could serve as a potential source of answers. Hunch is founded on a basic assumption: if you have the same priorities as other folks, their solutions are likely to be good options for you. If you capture the important factors this architecture works. I appreciate the founder <a href="http://cdixon.org">Chris Dixon's blog</a> and suspect good stuff from this service.</p>
<h6 class="zemanta-related-title" style="font-size: 1em;">Related articles by Zemanta</h6>
<ul class="zemanta-article-ul">
<li class="zemanta-article-ul-li"><a href="http://www.xconomy.com/boston/2009/11/18/founder-collective-when-entrepreneurs-form-their-own-seed-stage-venture-firm/">Founder Collective: When Entrepreneurs Form Their Own Seed-Stage Venture Firm</a> (xconomy.com)</li>
<li class="zemanta-article-ul-li"><a href="http://www.xconomy.com/boston/2009/11/09/founder-collective-debuts-with-40m/">Founder Collective Debuts with $40M</a> (xconomy.com)</li>
<li class="zemanta-article-ul-li"><a href="http://fulltimechris.blogspot.com/2009/11/zemanta.html">Zemanta</a> (fulltimechris.blogspot.com)</li>
<li class="zemanta-article-ul-li"><a href="http://www.slideshare.net/novaspivack/web-evolution-nova-spivack-twine">Web Evolution Nova Spivack Twine</a> (slideshare.net)</li>
</ul>
<div class="zemanta-pixie" style="margin-top: 10px; height: 15px;"><a class="zemanta-pixie-a" title="Reblog this post [with Zemanta]" href="http://reblog.zemanta.com/zemified/8d65ad3c-ac86-47f5-a1ac-1519841ab893/"><img class="zemanta-pixie-img" style="border: none; float: right;" src="http://img.zemanta.com/reblog_e.png?x-id=8d65ad3c-ac86-47f5-a1ac-1519841ab893" alt="Reblog this post [with Zemanta]" /></a><span class="zem-script more-related pretty-attribution"><script src="http://static.zemanta.com/readside/loader.js" type="text/javascript"></script></span></div>
