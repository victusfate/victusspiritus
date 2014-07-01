---
layout: post
status: publish
published: true
title: LazyMiracleDB, because you're never alone on a network
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 5209
wordpress_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/09/17/lazymiracledb-because-youre-never-alone-on-a-network/
date: '2010-09-17 06:04:27 -0400'
date_gmt: '2010-09-17 13:04:27 -0400'
categories:
- Uncategorized
tags:
- coding
- design
- databases
comments:
- id: 5990
  author: Tyler
  author_email: tjgillies@gmail.com
  author_url: http://www.pdxbrain.com
  date: '2010-09-19 04:34:00 -0400'
  date_gmt: '2010-09-19 04:34:00 -0400'
  content: I'm tempted to buy a case just to make you dance ;)
- id: 5995
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-09-19 09:14:00 -0400'
  date_gmt: '2010-09-19 09:14:00 -0400'
  content: I suspected that extended footnote may come back to haunt me.
- id: 6027
  author: Paul W. Homer
  author_email: paul_homer@yahoo.ca
  author_url: ''
  date: '2010-09-21 19:49:00 -0400'
  date_gmt: '2010-09-21 19:49:00 -0400'
  content: I thought of a design for lazyMiracleDB twenty years ago. I've tried a
    dozen times to get some type of backing to build the sucker, but people/money
    weren't interested. For one it would take too long to build. Another problem is
    that in solving all of the problems, programmers would intrinsically hate it;
    they'd rather fiddle with something intricate and clunky. The biggest problem
    however is that I couldn't guarantee that it would run efficiently. It would entirely
    encapsulate all of the problems, but it might be slower than a glacier. Perfect,
    but useless.  I'm afraid that although I believe it is possible, we won't see
    lazyMiracleDB in our lifetimes. I guess we have to crawl for a while, before we
    can run ...
- id: 6028
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-09-21 20:26:00 -0400'
  date_gmt: '2010-09-21 20:26:00 -0400'
  content: Maybe LazyMiracle is simply an interface to an array of databases that
    perform various functions behind the veil. They each have strengths and weaker
    areas.
- id: 6059
  author: Paul W. Homer
  author_email: paul_homer@yahoo.ca
  author_url: ''
  date: '2010-09-22 20:47:00 -0400'
  date_gmt: '2010-09-22 20:47:00 -0400'
  content: |-
    The big problems with databases that I've seen have been the expressibility of the underlying model, sharing between different applications and being able to mitigate the work of a new software version release.  RDBMs can't handle the full structural range of data that code can, the mapping between them is non-trivial and subject to problems (thus vendor specific enhancements to handle things like hierarchies or times series). Each application has  its own view of the data, so mapping that back to a universal view can cause major problems. And often with a release of a new application comes a complex chunk of work solely intended to 'upgrade' the database from an older schema to a new one. Performance and distribution are better understood issues, these other problems generally mean loads of work for programmers having to repetitively write essentially masses of self-similar code. In most apps, half the work is the interface and the other half is the database. Some technologies like OODBs made the code easy (just declare an Object as persistent and you're done), but at the cost of making the upgrades horrible (and dangerous).

    Paul.
- id: 6061
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-09-22 21:11:00 -0400'
  date_gmt: '2010-09-22 21:11:00 -0400'
  content: "Good experiential info Paul. \n\nYour description reminds me of woes of
    deep library modifications over the years. \n\"Change the interface to work with
    orangutans instead of image data\"\n\nMy psyche is forever scarred by the foul
    mutations I inflicted on my own code to make things work in a hurry. Every hair
    brained jury rig was another debt of maintenance hell down the road.\n"
---
<p><I>Disclaimer, I'm not peddling new software but thinking over exactly what I want from DBs</I></p>
<p>I'm impressed with the marketing acumen of technology like CouchDB with Relax, or RESTful design principles. There's a science and art to naming which immediately imparts a message. Google is BIG, Microsoft makes software for microcomputers, and <strike>Apple</strike> Steve Jobs is all about sharp design. </p>
<p><i>Where's LazyMiracleDB, is it you?</I><br />
I want a persistence layer that I <strong>never</strong> have to think about. You can store my data in an ocean cooled center in <a href="http://royal.pingdom.com/2010/09/15/googles-mega-data-center-in-finland/">Finland</a> for all I care. The perfect state machine is a black box I throw data in and forget about until I, or someone else needs it. It's always there, and it's Freakin' Fast, and if no one <i>needs</I> it, it dies (archived) after a grace period. It's language agnostic. I don't want to have to know^ anything about how it works at the application level, just tell me how to throw stuff in and get it in one line of code or a single click. And if my personal LazyMiracleDB needs more resources or another server it let's me know with a polite text or email: "resources over 80% @ URL.node, please confirm dialing up another server (Y/N), I could use a coffee break, shall I order you one as well?"^^.</p>
<p>I know what some of you are thinking, use Couch, Redis, Mongo, FluidDB or some other smooth DB*. While these are impressive technologies I still have to worry about a bunch of other stuff, so here's my worries and wish list combined. My DB pain points:</p>
<ul>
<li>How will my persistence layer interact with other services and databases. You're never alone on a network</li>
<li>security of information</li>
<li>Reckless synchronization: I want to be able to voice to text edit source on my phone, and have it live on thousands of public facing servers instantly. Eat that QA tests!</li>
<li>Ubiquitous. Availability across clusters and clients</li>
<li>phenomenal visualization and editing of what's inside. It has to work on any platform, think Dropbox (local files on my phone) combined with Chromium's search bar & universal doc handler but specialized for network apps. Instant search for my DB</li>
<li>and worst of all installation across platforms. Groovy new tech is notorious for custom builds and tricky porting, something I never want to think about before 5am again**</li>
</ul>
<p>Notes:<br />
^= I really do want to know how lazymiracleDB works, the curse of insatiable curiosity</p>
<p>^^= if you don't imbibe caffeine, you're not allowed to use LazyMiracleDB. Exceptions to blogger/geniuses I follow on twitter, or anyone who buys me a case of <a href="http://www.squidoo.com/RedlinePowerRush">Redline Power Rush</a>. Yeah, I wrote that page. If me, Seth Godin, and the 5% charity all become filthy rich and the servers disintegrate under the referral traffic coming from this post, I'll do the Macarena on a YouTube video proudly displayed on Google's homepage (assuming Larry, Sergey and the old guy are cool with it).</p>
<p>*= found a great tutorial on <a href="http://simonwillison.net/static/2010/redis-tutorial/">Redis</a> this AM. Instapapered it to my phone with slides and all, go Simon, Antirez and the big Redis community, there's a crapton of clients for your favorite language.</p>
<p>**= I am blessed with Ubuntu as my primary dev machine. All of you, whoever you are that make packages and dev libs (apt-get, debian, yum...) or source and install scripts that <strong>just work</strong>, Thank You! It's really been a pleasure working on Ubuntu over the past 4-5 months after years of windows only development.</p>
