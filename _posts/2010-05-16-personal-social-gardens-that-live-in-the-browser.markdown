---
layout: post
status: publish
published: true
title: Personal Social Gardens that Live in the Browser
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 3851
wordpress_url: http://www.victusspiritus.com/?p=3851
date: '2010-05-16 08:18:04 -0400'
date_gmt: '2010-05-16 15:18:04 -0400'
categories:
- Uncategorized
tags:
- web/tech
- social web
- social design
- open design
comments:
- id: 4332
  author: Leland
  author_email: leland@pickple.com
  author_url: ''
  date: '2010-05-17 03:00:20 -0400'
  date_gmt: '2010-05-17 08:00:20 -0400'
  content: Mark, my initial reaction to your article. Features are good, but I want
    to know how it can improve my life, in straight-faced words. Due to my technical
    background, I can figure out for myself all the ways in which this technology
    could help me with my digital identity et al. However, many readers who don&#39;t
    have an extensive background in SNS services and/or don&#39;t care to read through
    paragraphs of features to figure out the benefit might find a one or two sentence
    description of the potential direct benefits welcoming and helpful.<br><br>:)
- id: 4334
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-05-17 10:00:21 -0400'
  date_gmt: '2010-05-17 15:00:21 -0400'
  content: Heh, well put. I use the blog as a white board to scratch out ideas  <br>rapidly,
    buy often fail to distill a brief "benefits" list out of the  <br>thought riff.<br><br>After
    a short discussion with Tyler I&#39;m not sure the "routing server"  <br>idea
    of <a href="http://status.net" rel="nofollow">status.net</a> isn&#39;t good enough
    for a first cut. As we work  <br>towards a living, proof of concept for less centralized
    social  <br>networks the personal garden, living in a browser becomes more  <br>feasible.
    For now a peer to peer network would require admin  <br>permissions on the host
    to share out files, and this type of  <br>functionality is a little beyond the
    sandbox JavaScript browser  <br>language. Maybe a one click plugin?<br><br>The
    benefits are coming, most certainly when we&#39;re closer to a soft  <br>launch.
- id: 8935
  author: Startup Strategies that Survive, Prosper, and Win &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/02/12/startup-strategies-that-survive-prosper-and-win/
  date: '2011-02-12 16:32:06 -0500'
  date_gmt: '2011-02-12 23:32:06 -0500'
  content: "[...] Personal Social Gardens that live in the browser [...]"
---
<p><a href="{{ site.url }}/assets/2010/05/NorthernCentralParkPond1.jpg"><img class="aligncenter size-full wp-image-3867" title="NorthernCentralParkPond" src="{{ site.url }}/assets/2010/05/NorthernCentralParkPond1.jpg" alt="" width="500" height="375" /></a></p>
<p>My esteemed colleague and cofounder Tyler hacked out a 100 line message sharing server. He used Ruby and Sinatra and we chatted on it briefly this morning. But the model follows the way of Facebook and Twitter with one database back end serving as a middle man between people. <a href="http://joindiaspora.com/2010/04/30/a-response-to-mr-villa.html">Even Diaspora</a>'s proposed solution involves a server middle layer route if you opt for their suggested hosted solution (i.e. they host "seeds" on a .com domain). They're stand alone "seeds" or servers are no different than many web servers that serve html pages today, with the added promise of intercommunication. I suspect stand alone servers will be more difficult than an average user will be capable or want to set up. I'd like to offer an alternative.</p>
<h2>Proposal: OpenGard.in a Network of Personal Gardens or Social Servers</h2>
<p>Desired elements of a truly distributed social web network:</p>
<ul>
<li>It can live in the browser. As a user I can spin up a local server that lives in my current browser environment and communicate with other nodes with a simple click of a button (my OpenID). Whether I'm on or offline, other users that I give permission to can access my social data with a Push method. I may observe other nodes and they can observe me by subscribing to updates. We can have private encrypted messages, share files freely back and forth, or share public messages all determined at time of sending.</li>
</ul>
<ul>
<li>Standard web servers can also connect and communicate with nodes, and host pages using supported web languages (protocols and standards as opposed to database apis). They can act in the same way as nodes, but provide scale to popular network super nodes (news sites),"blogstars", and celebrities. You don't have to spin up a local node server to browse public node information that you subscribe to, simply hit a known web page which curates that topic.</li>
</ul>
<ul>
<li>Distributed Moderation is a key feature of spam resistant and quality community social networks. If users flag spam or network abusers the abuser's ID can easily be added to public blacklists.</li>
</ul>
<ul>
<li>People need an easy way of identifying themselves and finding others. OpenID can aid universal identification, and Oauth will help connect users to existing services. To find others it should be as simple as typing in a real name or pseudonym at a web directory page or using a personal garden accessing a network directory. Anonymous users can carry a pseudonym and post, but their identities are still subject to distributed moderation. Pseudonyms can be blacklisted, continued creation of pseudonyms should be discouraged (I'm open to ideas here). Nodes aren't forced to ignore users that are blacklisted, they can opt in or out at anytime.</li>
</ul>
<ul>
<li>Open source code, to be extended and customized as needed</li>
</ul>
<ul>
<li>Data storage can exist simultaneously locally and in the cloud on services like <a href="http://dropbox.com">Dropbox</a></li>
</ul>
<p>Peer 2 Peer networks may provide guidance on infrastructure or usage patterns for dynamic social networks. In these type of networks, nodes dynamically appear and vanish. Users of personal gardens won't be able to hit a static URL like http://mark.com/ to pull my updates unless hosted by standard web servers, which are setup to serve social information in that way. Instead they are free to browse their own personal garden if they subscribe to my updates. My information goes to them (Push), they don't have to come to, or hit my page with a request.</p>
<p>Related Links &amp; References:</p>
<ul>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/03/08/open-web-protocols-and-discussion-groups/">Open Web Protocols &amp; Discussion Groups</a></li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/03/13/data-silos-or-a-social-web-pattern/">Data Silos or a Social Web Pattern</a></li>
<li><a href="http://www.victusspiritus.com/?s=%22opengard.in%22">Open Garden</a></li>
<li><a href="http://diso-project.org/">DiSo</a></li>
<li><a href="http://www.peerson.net/">PeerSon</a></li>
<li><a href="http://www.joindiaspora.com/">Diaspora</a></li>
</ul>
<h6 class="zemanta-related-title" style="font-size: 1em;">Related articles by Zemanta</h6>
<ul class="zemanta-article-ul">
<li class="zemanta-article-ul-li"><a href="http://blog.ibeentoubuntu.com/2010/05/diaspora-focusing-on-p2p-shunning-s2s.html">Diaspora Focusing on P2P, Shunning S2S</a> (ibeentoubuntu.com)</li>
<li class="zemanta-article-ul-li"><a href="http://carsonified.com/blog/dev/whats-going-on-with-open-source-and-standards/">What's Going on with Open Source and Standards?</a> (carsonified.com)</li>
</ul>
<div class="zemanta-pixie" style="margin-top: 10px; height: 15px;"><a class="zemanta-pixie-a" title="Reblog this post [with Zemanta]" href="http://reblog.zemanta.com/zemified/6c65ea00-7788-479f-9b95-653161983b48/"><img class="zemanta-pixie-img" style="border: none; float: right;" src="http://img.zemanta.com/reblog_e.png?x-id=6c65ea00-7788-479f-9b95-653161983b48" alt="Reblog this post [with Zemanta]" /></a><span class="zem-script more-related pretty-attribution"><script src="http://static.zemanta.com/readside/loader.js" type="text/javascript"></script></span></div>
