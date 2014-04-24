---
layout: post
status: publish
published: true
title: Twitter is not "broader" than Pubsubhubbub
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 5197
wordpress_url: http://www.victusspiritus.com/?p=5197
date: '2010-09-15 11:39:24 -0400'
date_gmt: '2010-09-15 18:39:24 -0400'
categories:
- Uncategorized
tags:
- social web
- twitter
- real time web
comments:
- id: 5933
  author: ''
  author_email: jaisen@jmathai.com
  author_url: ''
  date: '2010-09-15 20:10:00 -0400'
  date_gmt: '2010-09-15 20:10:00 -0400'
  content: The name alone will kill PubSubHubbub before it gets very far out the door.
- id: 5934
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-09-15 20:15:00 -0400'
  date_gmt: '2010-09-15 20:15:00 -0400'
  content: PuSH works
- id: 5936
  author: ''
  author_email: jaisen@jmathai.com
  author_url: ''
  date: '2010-09-15 20:21:00 -0400'
  date_gmt: '2010-09-15 20:21:00 -0400'
  content: Good point :).
- id: 5945
  author: BerislavLopac
  author_email: berislav@lopac.net
  author_url: http://berislavlopac.tumblr.com
  date: '2010-09-16 07:52:00 -0400'
  date_gmt: '2010-09-16 07:52:00 -0400'
  content: 'PuSH would be a great technology if it weren''t for one detail: it''s
    HTTP-based. ;)'
- id: 5948
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-09-16 10:56:00 -0400'
  date_gmt: '2010-09-16 10:56:00 -0400'
  content: 'Http has been the publishers protocol of choice for a while now, so pushing
    out updates faster within the context of the standard feels like a good fit. While
    there are plenty of alternative network protocols, and some <a href="http://www.igvita.com/2010/09/03/zeromq-modern-fast-networking-stack/"
    rel="nofollow">groovy connection layers</a>, what would be your ideal choice? '
- id: 5950
  author: BerislavLopac
  author_email: berislav@lopac.net
  author_url: http://berislavlopac.tumblr.com
  date: '2010-09-16 13:55:00 -0400'
  date_gmt: '2010-09-16 13:55:00 -0400'
  content: We need a new standard, and a new network paradigm.
- id: 5951
  author: Michael Greenberg
  author_email: placer14@gmail.com
  author_url: http://nobulb.com
  date: '2010-09-16 14:57:00 -0400'
  date_gmt: '2010-09-16 14:57:00 -0400'
  content: "    A decade of adoption later... \n\n    Them: Shit, this new standard
    doesn't work for the tech of today!\n    OlderBerislav: We need a new standard,
    and a new network paradigm.\n\nSarcasm aside, since there's nothing out there
    that provides adequate transport for PuSH, what features are missing from HTTP
    which you are looking for in your perfect protocol?"
- id: 5964
  author: Berislav Lopac
  author_email: berislav@lopac.net
  author_url: http://berislav.lopac.net
  date: '2010-09-17 00:29:00 -0400'
  date_gmt: '2010-09-17 00:29:00 -0400'
  content: First of all its statelessness, and second its asymmetry. But in general,
    the concept of push (not PuSH) is not *the* solution; it's merely a solution which
    uses technology we already have. We need to think more out of the box.
---
<p>How can something like this:</p>
<p><a href="http://www.victusspiritus.com/wp-content/uploads/2010/09/1910telephoneexchange.jpg"><img class="aligncenter size-full wp-image-5198" title="1910telephoneexchange" src="http://www.victusspiritus.com/wp-content/uploads/2010/09/1910telephoneexchange.jpg" alt="" width="597" height="380" /></a></p>
<p>be broader than something like this:</p>
<p><a href="http://www.victusspiritus.com/wp-content/uploads/2010/09/internet.jpg"><img class="aligncenter size-full wp-image-5199" title="internet" src="http://www.victusspiritus.com/wp-content/uploads/2010/09/internet.jpg" alt="" width="800" height="533" /></a></p>
<p>Right on <a href="http://www.google.com/profiles/116969159384245484847">Brett Slatkin</a> !<br />
<a href="http://www.google.com/buzz/bslatkin/Ue1EA9BfSKx">http://www.google.com/buzz/bslatkin/Ue1EA9BfSKx</a></p>
<p>Brett Slatkins buzz:</p>
<p style="padding-left: 30px;"><strong>Transparent Fud.</strong></p>
<p style="padding-left: 30px;"><a href="http://gigaom.com/2010/09/14/10-things-you-didnt-know-about-the-new-twitter-com/">In item #6 this article quotes</a> Ryan Sarver, Director of Platform at Twitter, explaining why Twitter  doesn't extract snippets from feeds: "[PubSubHubbub] is fast enough, RSS  is not. PSHB isn't broad enough yet."</p>
<p style="padding-left: 30px;">Nevermind the speed admission (which is in itself a small victory)-- <strong>What does he mean by "not broad enough yet?"</strong> PubSubHubbub is <a href="http://www.livejournal.com/">supported</a> <a href="http://blogger.com/">by</a> <a href="http://www.typepad.com/">every</a> <a href="http://wordpress.com/">major</a> <a href="http://www.tumblr.com/">blogging</a> <a href="http://posterous.com/">platform</a>; used by <a href="http://gowalla.com/">location</a> <a href="http://buddycloud.com/">services</a>; powers cross-site follow on <a href="http://status.net/">microblogging</a> <a href="http://cliqset.com/">sites</a>; provides <a href="http://buzz.google.com/">publish</a> and <a href="http://digg.com/">subscribe</a> for <a href="http://myspace.com/">social</a> <a href="http://friendfeed.com/">networks</a>; enables a <a href="http://superfeedr.com/">range</a> <a href="http://www.my6sense.com/">of</a> <a href="http://postrank.com/">search</a> <a href="http://oneriot.com/">and</a> <a href="http://gnip.com/">track</a> <a href="http://collecta.com/">features</a>; produces real-time <a href="http://pheedo.com/">feed</a> <a href="http://feedburner.com/">analytics</a>; has clients for <a href="http://code.google.com/p/pubsubhubbub/wiki/PublisherClients">popular languages</a> and <a href="http://code.google.com/p/pubsubhubbub/wiki/SubscriberClients">CMSes</a>; has existing <a href="http://reader2twitter.appspot.com/">Twitter-bridging</a> <a href="http://twitterfeed.com/">tools</a>; and there's even a prototype of what Twitter's support for PubSubHubbub <a href="http://blog.persistent.info/2009/08/twitter-pubsubhubbub-bridge.html">would look like</a>. (I'm leaving out a lot of links.)</p>
<p style="padding-left: 30px;">I think I understand Ryan, actually: He's in the marketing department  and just doing his job. Since Twitter aspires to be the infrastructure--  the "nervous system" of the web-- they need to provide a compelling  reason to integrate directly with Twitter (lock-in) and not with the <a href="http://openwebfoundation.org/">open web</a>. This is <em>the</em> platform game (<a href="http://microsoft.com/">of antiquity</a>). The easiest way to convince others to put their eggs in one basket is to spread FUD (fear, uncertainty, doubt) about the <strong>other</strong> platform that's out there.</p>
<p style="padding-left: 30px;">This FUD is so transparent it's kind of refreshing.</p>
