---
layout: post
status: publish
published: true
title: Sing.ly where Local Apps Compete on Value not Network Lock In
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 7083
wordpress_url: http://www.victusspiritus.com/?p=7083
date: '2011-02-04 06:32:37 -0500'
date_gmt: '2011-02-04 13:32:37 -0500'
categories:
- Uncategorized
tags:
- startups
- open source
- design
- apps
comments:
- id: 8835
  author: Tweets that mention Sing.ly where Local Apps Compete on Value not Network
    Lock In » Victus Spiritus -- Topsy.com
  author_email: ''
  author_url: http://topsy.com/www.victusspiritus.com/2011/02/04/sing-ly-where-local-apps-compete-on-value-not-network-lock-in/?utm_source=pingback&amp;utm_campaign=L2
  date: '2011-02-04 07:19:57 -0500'
  date_gmt: '2011-02-04 14:19:57 -0500'
  content: "[...] This post was mentioned on Twitter by Mark Essel, HN Firehose. HN
    Firehose said: Sing.ly where Local Apps Compete on Value not Network Lock In:
    http://bit.ly/fWoVe1 [...]"
- id: 8871
  author: Jeremie Miller
  author_email: ''
  author_url: http://twitter.com/jeremie
  date: '2011-02-08 18:14:00 -0500'
  date_gmt: '2011-02-08 18:14:00 -0500'
  content: |-
    Heya Mark, thanks for the awesome post!

    On the last bit about TeleHash, it's fully distributed/P2P, so there isn't anything that can really go down, in fact it should be more resilient than nearly any other service that I know of :)
- id: 8872
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-02-08 18:42:00 -0500'
  date_gmt: '2011-02-08 18:42:00 -0500'
  content: Thanks for stopping by and clarifying Telehash's bulletproof nature Jeremie.
    So if I hit telehash.org with a remote call it hit's different surfaces of the
    network?
- id: 10171
  author: The Client Server Class War &mdash; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2011/06/20/the-client-server-class-war/
  date: '2011-06-20 14:42:44 -0400'
  date_gmt: '2011-06-20 21:42:44 -0400'
  content: "[...] go to utility for distributed file sharing for most of my net connected
    years. As I covered here a few months back, Telehash.org has risen as another
    route for peer to peer [...]"
---
<p>I woke up this morning to catch a fresh off the virtual presses <a href="http://m.readwriteweb.com/archives/creator_of_instant_messaging_protocol_to_launch_ap.php">post</a> by Marshall Kirkpatrick's virtual capacities (ReadWriteWeb) on a bold new app architecture. </p>
<blockquote><p>
Here's how The Locker Project will work. Users will be able to download the data capture and storage code and run it on their own server, or sign up for hosted service - like WordPress.org and WordPress.com.
</p></blockquote>
<p>Jeremie Miller, who crafted XMPP which powers most instant messaging apps, has founded the <a href="https://github.com/quartzjer/Locker">Locker Project</a>.  <a href="http://sing.ly">Sing.ly</a> is the corporate backing providing resources to the open source effort. </p>
<p>The open source effort is in it's alpha stages so it's likely a little too green to bet your company on. Nonetheless, I have confidence an app architecture and network model will take shape and gain momentum much like the one described by Sing.ly and the Locker Project. CouchDB and Couchone have a similar relationship but focus on distributed apps and data access without a uniform routing layer.</p>
<p><I>How Locker Projects Communicate</I></p>
<p>The magic of bringing together isolated islands of personal content is <a href="http://telehash.org">Telehash.org</a>, an implementation of an open source p2p layer that enables network edges to act like servers. I mentioned the routing power of <a href="http://en.wikipedia.org/wiki/Kademlia">Kademlia</a> and Telehash a couple of days back while <a href="http://www.victusspiritus.com/2011/02/02/p2pmsg-a-distributed-message-network/">describing p2pmsg</a>, a notional message layer built on the network. </p>
<p>One concern I have is that if Telehash.org is the primary hub for negotiating connections between Lockers, what happens when it goes down? I imagine it's much like domain name servers going offline, other Kademlia routers pick up the slack but this step isn't automated. I'll do a little follow up research this morning and find out if and how this distributed network design protects against the failure of the routing layer.</p>
