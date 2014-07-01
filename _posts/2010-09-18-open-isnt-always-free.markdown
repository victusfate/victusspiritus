---
layout: post
status: publish
published: true
title: Open isn't always free
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 5213
wordpress_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/09/18/open-isnt-always-free/
date: '2010-09-18 08:16:44 -0400'
date_gmt: '2010-09-18 15:16:44 -0400'
categories:
- Uncategorized
tags:
- social web
- victus media
- open source
- design
- open
comments:
- id: 5989
  author: Tyler
  author_email: tjgillies@gmail.com
  author_url: http://www.pdxbrain.com
  date: '2010-09-19 04:31:00 -0400'
  date_gmt: '2010-09-19 04:31:00 -0400'
  content: You can replicate to and from a remote DB to a local DB even if you're
    behind NAT as long as the DB you're connecting to is itself not behind NAT
- id: 5996
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-09-19 09:18:00 -0400'
  date_gmt: '2010-09-19 09:18:00 -0400'
  content: you mentioned continuous replication has an issue. It better to periodically
    call replicate for remote nodes you want to keep in synch?
- id: 6020
  author: Mikeal
  author_email: ''
  author_url: http://twitter.com/mikeal
  date: '2010-09-21 16:03:00 -0400'
  date_gmt: '2010-09-21 16:03:00 -0400'
  content: |-
    In 1.0.1 continuous replication doesn't survive restarts.

    Now we have the _replicator db in trunk which fixes a ton of issues including the big one for surviving restarts.  It will ship in CouchDB 1.1
- id: 6021
  author: Mikeal
  author_email: ''
  author_url: http://twitter.com/mikeal
  date: '2010-09-21 16:06:00 -0400'
  date_gmt: '2010-09-21 16:06:00 -0400'
  content: |-
    To clarify a little.

    There are two replication types, push and pull. You can push your data from one CouchDB to another or you can pull data from a remote CouchDB to yours. CouchDB's API for initiating this can be started on either side, so you can make an HTTP request that starts push or pull on a local or remote node.

    If you're worried about a NAT jut setup a CouchDB in the cloud that all interested parties replicate with and use as a central sync point.
- id: 6022
  author: Tyler
  author_email: tjgillies@gmail.com
  author_url: http://www.pdxbrain.com
  date: '2010-09-21 16:15:00 -0400'
  date_gmt: '2010-09-21 16:15:00 -0400'
  content: "I heard someone say if you send a cacel:true flag it stops continuous\r\nreplication,
    is this right?"
- id: 6023
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-09-21 18:24:00 -0400'
  date_gmt: '2010-09-21 18:24:00 -0400'
  content: "Thanks for chiming in Mike.  Couch appears to be pushing &amp; pulling
    quite nicely in my test cases between sync'd nodes.\n\nEverything about how Couch
    works is new to me so it's been fun digging through the documentation and helpful
    blog posts from enthusiastic community members. Tyler lives and breathes hacking
    so he picks up the applications quicker. I enjoy digging in a little slower, then
    really pushing the system hard. \n\nThe easier I can get other folks to install/create/sync
    couch instances, the better. I haven't read into the details behind b-tree hierarchical
    comparisons and rapid copying yet in the definitive guide (later chapter), looking
    forward to it."
---
<p>Social sites have popularized content sharing over large centrally controlled networks^. The Freemium media model is nothing short of attention jiu jitsu. Initially a young service induces early adoption and experimentation while refining its perceived social utility. The value of the service rises as the network grows and members create content and communicate through the new medium. At varying stages of maturity web companies monetize visitor attention, and charge engaged clients and creators for premium services.</p>
<p><I>Closed can come without cost</I></p>
<p>Open source technology is providing compelling alternatives to central corporate systems. We can share created content to a selection of friends without authorizing third party access to monetize redistributed content or our attention. This has motivated many application designers to build their own communication tools and freely share them with others. The technology can be open through public source code, while applications are free to be closed, semi-closed, or fully open.</p>
<p>Let's frame this in the context of a concrete example. Consider a peer to peer photo sharing service consisting of personal photos and collections. This type of sharing is ideal for synchronizing photos between a family or group of friends and is capable of dynamically updating each members local set. My friend Tyler showed me how to replicate an early version of just such a  tool, with synchronization baked into the technology he chose. In order to be independent from intermediary hosting companies, clients would be required to install CouchDB locally and have a way of connecting with each other, such as a public facing site*. Without installation, a Couch database can be created and hosted on CouchOne. Public facing implementations enable access from any authorized client via a web browser. An invite only system could place the content beyond the grasp of third party aggregators, unless access is granted by privileged clients. Watch out, grandma could sell those naked bathtub baby photos of you ;).</p>
<p>Notes:<br />
^= Social sharing sites benefit by having unrestricted access to use client data, while restricting third party companies from doing so. In short data control is optimized towards corporate profit.</p>
<p>*= CouchDB has simple installation on Linux, Windows, and MacOSX. Public facing hosts can be achieved through a variety of methods. Couch responds to HTTP requests natively.</p>
