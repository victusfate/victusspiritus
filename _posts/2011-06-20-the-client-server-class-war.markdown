---
layout: post
status: publish
published: true
title: The Client Server Class War
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9316
wordpress_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/06/20/the-client-server-class-war/
date: '2011-06-20 06:18:25 -0400'
date_gmt: '2011-06-20 13:18:25 -0400'
categories:
- Uncategorized
tags:
- web/tech
- open design
- open source
comments: []
---
<p>Internet traffic is undergoing an irreversible transition from predominantly pc browsing to smaller mobile devices and large displays for streaming video. Client side software has been a hot development area on mobile and novel display surfaces, as opposed to only supporting local device web browsers. Most active SaS businesses build clients for all the primary platforms - web, iOS, Android, etc., enabling customers to access provided services efficiently from any platform they choose.</p>
<p>Deeply ingrained within <a href="http://en.wikipedia.org/wiki/Representational_State_Transfer">RESTful</a> architecture is the client server relationship. Clients can typically only request to receive and modify resources, while servers are also capable receiving and responding to requests. The World Wide Web is the largest RESTful architecture<sup><a href="#notes">1</a></sup>. </p>
<blockquote>
<h2>What is Representational State Transfer</h2>
<p>REST exemplifies how the Web’s architecture emerged by characterizing and constraining the macro-interactions of the four components of the Web, namely origin servers, gateways, proxies and clients, without imposing limitations on the individual participants. As such, REST essentially governs the proper behavior of participants.</p>
<p>REST-style architectures consist of clients and servers. Clients initiate requests to servers; servers process requests and return appropriate responses. Requests and responses are built around the transfer of representations of resources. A resource can be essentially any coherent and meaningful concept that may be addressed. A representation of a resource is typically a document that captures the current or intended state of a resource.</p>
<p>At any particular time, a client can either be in transition between application states or “at rest.” A client in a rest state is able to interact with its user, but creates no load and consumes no per-client storage on the servers or on the network.</p>
<p>The client begins sending requests when it is ready to make the transition to a new state. While one or more requests are outstanding, the client is considered to be in transition. The representation of each application state contains links that may be used next time the client chooses to initiate a new state transition.<br />
(<a href="http://en.wikipedia.org/wiki/Representational_State_Transfer">source</a>)
</p></blockquote>
<p>REST is best described as a common design specified by a set of shared rules which individual network nodes adhere to. As a reminder and bit of homework for myself, I've included these requirements below (skip to Headless Networks if you're familiar with REST):</p>
<blockquote>
<h2>RESTful Rules</h2>
<p><b>Client–server</b><br />
Clients are separated from servers by a uniform interface. This separation of concerns means that, for example, clients are not concerned with data storage, which remains internal to each server, so that the portability of client code is improved. Servers are not concerned with the user interface or user state, so that servers can be simpler and more scalable. Servers and clients may also be replaced and developed independently, as long as the interface is not altered.</p>
<p><b>Stateless (Clients)</b><br />
The client–server communication is further constrained by no client context being stored on the server between requests. Each request from any client contains all of the information necessary to service the request, and any session state is held in the client. The server can be stateful; this constraint merely requires that server-side state be addressable by URL as a resource. This not only makes servers more visible for monitoring, but also makes them more reliable in the face of partial network failures as well as further enhancing their scalability.</p>
<p><b>Cacheable</b><br />
As on the World Wide Web, clients are able to cache responses. Responses must therefore, implicitly or explicitly, define themselves as cacheable, or not, to prevent clients reusing stale or inappropriate data in response to further requests. Well-managed caching partially or completely eliminates some client–server interactions, further improving scalability and performance.</p>
<p><b>Layered system</b><br />
A client cannot ordinarily tell whether it is connected directly to the end server, or to an intermediary along the way. Intermediary servers may improve system scalability by enabling load balancing and by providing shared caches. They may also enforce security policies<sup><a href="#notes">2</a></sup>.</p>
<p><b>Uniform interface</b><br />
The uniform interface between clients and servers, discussed below, simplifies and decouples the architecture, which enables each part to evolve independently. The four guiding principles of this interface are detailed below.</p>
<p><b>Code on demand (optional)</b><br />
Servers are able to temporarily extend or customize the functionality of a client by transferring logic to it that it can execute. Examples of this may include compiled components such as Java applets and client-side scripts such as JavaScript.<br />
(<a href="http://en.wikipedia.org/wiki/Representational_State_Transfer">source</a>)
</p></blockquote>
<p>Now that we have a firm footing on what client and server mean in the context of RESTful services, we're ready to explore alternatives. After a quick tour of Peer to Peer protocols and services, (hopefully) we'll better understand the conflict between client-server and peer to peer architectures.</p>
<h2>"Headless" Networks</h2>
<p>Peer to Peer distributed software has experienced periods of rising and falling widespread appeal. Napster was the internet's answer to getting files quickly, often without permission from the original owner of the data. Bit torrent has been the go to utility for distributed file sharing for most of my net connected years. As I covered here a <a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/02/04/sing-ly-where-local-apps-compete-on-value-not-network-lock-in/">few months back, Telehash.org</a> has risen as another route for peer to peer communication. </p>
<p>While gratuitous volumes of data have been pushed and pulled through these pipes, they have never had the wide scale commercial success and attraction that web servers have had. One rationale is that businesses don't have obvious bottlenecks in Peer to Peer networks, like they do for web servers. An elementary control surface for organizations is to author the peer to peer software themselves. An open source strategy would have a greater chance of adoption, encourage healthy competition and provide  additional security to developers on top of the protocol.</p>
<p><a href="#notes" id="notes">Notes</a></p>
<ol>
<li>With respect to the World Wide Web, it's arguable that the appearance of manifests and web sockets in http is eroding the distinction between client and server.
<p>Manifests provide clients with local storage. I appreciate the ability to access content while I'm offline, but am limited to tools like Instapaper, DropBox, and CouchDB until manifests get widespread adoption, and client databases grown in size (I believe they can with permission now on modern web browsers).</p>
<p>While client and server are restricted to formal communication of state transfer, nodes exchanging data over a sockets can pass back any desired information without concern for node typing, diminishing the role of dedicated servers as network mediators. Clients and servers may both be stateful, breaking the stateless client requirement</li>
<li>Although layering enables many desirable network features (scaling, logging) it also allows for man in the middle attacks. Https obviates this type of security vulnerability (unless the attacker can decrypt the packets in real time).</li>
</ol>
