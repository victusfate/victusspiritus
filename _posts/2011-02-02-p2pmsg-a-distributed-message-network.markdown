---
layout: post
status: publish
published: true
title: p2pmsg a distributed message network
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 7064
wordpress_url: http://www.victusspiritus.com/?p=7064
date: '2011-02-02 05:42:50 -0500'
date_gmt: '2011-02-02 12:42:50 -0500'
categories:
- Uncategorized
tags:
- social web
- coding
- open source
comments:
- id: 8834
  author: Sing.ly where Local Apps Compete on Value not Network Lock In &raquo; Victus
    Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/02/04/sing-ly-where-local-apps-compete-on-value-not-network-lock-in/
  date: '2011-02-04 06:32:51 -0500'
  date_gmt: '2011-02-04 13:32:51 -0500'
  content: "[...] like servers. I mentioned the routing power of Kademlia and Telehash
    a couple of days back while describing p2pmsg, a notional message layer built
    on the [...]"
- id: 9837
  author: Under the Tent Mesh &mdash; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/04/15/under-the-tent-mesh/
  date: '2011-04-16 04:17:39 -0400'
  date_gmt: '2011-04-16 11:17:39 -0400'
  content: "[...] distributed routing would require optimization for a highly dynamic
    network such as torrents and Kademlia hash tables. //   Share and [...]"
---
<p>Talented socweb hacker Tyler Gillies has been busy late night coding. His latest alpha crafting is a fresh look at communication architectures. <a href="https://github.com/tjgillies/p2pmsg">p2pmsg</a> is actually a three part peer to peer com system. It's composed of a client or message generator, a receiver (server), and a routing layer which all facilitate communication between nodes.</p>
<p><I>Client</I></p>
<p>The client first negotiates a pipe to the router.<br />
<script src="https://gist.github.com/807611.js?file=p2p%20client%20connect%20to%20router"></script><br />
It then creates a listening function on the socket which transfers composed messages.<br />
<script src="https://gist.github.com/807607.js?file=client%20listener%20from%20p2pmsg"></script><br />
See <a href="https://github.com/tjgillies/p2pmsg/blob/master/client.js">client.js</a> or <a href="https://github.com/tjgillies/p2pmsg/blob/master/client.php">client.php</a> for implementation details.</p>
<p><I>Router</I></p>
<p>The routing layer is based on <a href="http://en.wikipedia.org/wiki/Kademlia">Kademlia</a> and is implemented by <a href="http://www.telehash.org">Telehash.org</a>. The following is a brief description for Kademlia:</p>
<blockquote><p>
Kademlia is a distributed hash table for decentralized peer-to-peer computer networks designed by Petar Maymounkov and David Mazières.[1] It specifies the structure of the network and the exchange of information through node lookups. Kademlia nodes communicate among themselves using UDP. A virtual or overlay network is formed by the participant nodes. Each node is identified by a number or node ID. The node ID serves not only as identification, but the Kademlia algorithm uses the node ID to locate values (usually file hashes or keywords). In fact, the node ID provides a direct map to file hashes and that node stores information on where to obtain the file or resource.
</p></blockquote>
<p>If you're interested in learning more about Kademlia's design, please follow the above wikipedia link. The random neighborhood assignment and choice of exor for a distance-like metric were new to me.</p>
<p><I>Receiver</I></p>
<p>The receiver is composed of a database, an http server, a renderer and a socket connection. The minimal receiver is a socket connection, and is similar to the client with the addition of configuring itself as an end point for the Telehash router.<br />
<script src="https://gist.github.com/807622.js?file=p2p%20receiver%20socket%20code"></script><br />
In the test receiver Tyler has coded up he also has a database for storing messages, and an http server with a renderer for serving a view to that data. The full receiver implementation can be found within <a href="https://github.com/tjgillies/p2pmsg/blob/master/server.js">server.js</a>. </p>
<p>Last I checked Tyler has a live receiving server at <a href="http://nostat.us:8080/tweets">nostat.us:8080/tweets</a> (not prettyfied yet). A note of caution: it's bleeding edge alpha, the implementation and server are subject to change. If you run a client you send messages to it as an end point.</p>
