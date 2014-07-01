---
layout: post
status: publish
published: true
title: First Impressions of Sitting a Web App on CouchDB
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 5047
wordpress_url: http://www.victusspiritus.com/?p=5047
date: '2010-09-04 12:59:30 -0400'
date_gmt: '2010-09-04 19:59:30 -0400'
categories:
- Uncategorized
tags:
- victus media
- coding
- javascript
- garage dollar
- CouchDB
- databases
comments:
- id: 5751
  author: Jan L
  author_email: jan@apache.org
  author_url: ''
  date: '2010-09-05 17:12:00 -0400'
  date_gmt: '2010-09-05 17:12:00 -0400'
  content: "Hi Mark,\n\nthanks for the nice write-up :)\n\nCheers\nJan\n-- \n"
- id: 5762
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-09-05 19:13:00 -0400'
  date_gmt: '2010-09-05 19:13:00 -0400'
  content: "Anytime Jan, thanks for stopping by. I'm having a great time with the
    Definitive Guide. \n\nIt helps me to better understand novel tech by scribbling
    down notes into a post. That way it serves as a cheat sheet later on when I get
    stuck. Who knows, it may even help somebody else out.\n\nBest of luck with couchio,
    you guys have an all star team."
- id: 5997
  author: Reckless Photo CouchDB App in 60 seconds | Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/09/19/reckless-photo-couchdb-app-in-60-seconds/
  date: '2010-09-19 12:20:02 -0400'
  date_gmt: '2010-09-19 19:20:02 -0400'
  content: "[...] Reckless Photo CouchDB App in 60 seconds  Posted on September 19,
    2010 by Mark Essel   TweetAssumption: you have couchapp and couchDB installed,
    see this post [...]"
- id: 6018
  author: State Propagation with Multiple Databases | Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/09/21/state-propagation-with-multiple-databases/
  date: '2010-09-21 06:33:19 -0400'
  date_gmt: '2010-09-21 13:33:19 -0400'
  content: "[...] it? Go ahead and &#8220;fork it&#8221; by cloning it to your own
    local or couchone.com CouchDB (installation help).   Share and [...]"
- id: 7432
  author: Bare Canvas vs Complex Frameworks, a case review of couchapps &raquo; Victus
    Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/11/07/bare-canvas-vs-complex-frameworks-a-case-review-of-couchapps/
  date: '2010-11-07 06:05:38 -0500'
  date_gmt: '2010-11-07 13:05:38 -0500'
  content: "[...] First Impressions of Sitting a Web App on CouchDB [...]"
- id: 9444
  author: Brushing Up on Computer Science Part 3, Data Structures &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/16/brushing-up-on-computer-science-part-3-data-structures/
  date: '2011-03-16 05:02:31 -0400'
  date_gmt: '2011-03-16 12:02:31 -0400'
  content: "[...] Study: CouchDB BTree [...]"
---
<p><a href="http://couchdb.apache.org/"><img class="aligncenter size-full wp-image-4996" title="relax" src="{{ site.url }}/assets/2010/08/relax.gif" alt="" width="176" height="160" /></a><br />
As promised, I've jotted down scattered notes on my first experiences with CouchDB, with ample reliance on references. At this point I have very limited practical experience with CouchDB and more RTFM time, so this post will focus on a little of the theory behind the design.</p>
<p>My initial reaction to couch: it's unlike any other database I've worked with before.</p>
<p>While it shares structural similarities with <a href="http://en.wikipedia.org/wiki/NoSQL">NoSQL</a> relatives*, it's construction in Erlang and ability to be a single solution web server makes it stand apart. For the first time since working with web tools, I felt a convergence of the RESTful concept of client/server with peer to peer distributed technology. Every couchDB can act as both client and server, and CouchDB is being ported to a diverse set of platforms.</p>
<p>I'll begin with a taste of the <a href="http://guide.couchdb.org/editions/1/en/why.html">definitive guide to couch</a> which captures the nature of this database design and communicates a clear message:</p>
<blockquote><p>Relax</p>
<p>If there’s one word to describe CouchDB, it is relax. It is in the title of this book, it is the byline to CouchDB’s official logo, and when you start CouchDB, you see:</p>
<p>Apache CouchDB has started. Time to relax.</p></blockquote>
<p>After <a href="http://guide.couchdb.org/editions/1/en/source.html">installation</a>^, the definitive guide <a href="http://guide.couchdb.org/editions/1/en/tour.html">walks you through</a> some basic HTTP calls to the API. Yup, it's a server and a DB all rolled into one. This simple concept eluded me after browsing over some of the documentation. There's a built in administration tool called <a href="http://answers.oreilly.com/topic/1395-introduction-to-couchdbs-futon-administration-interface/">Futon</a> that guides you through the creation or synchronization of databases.</p>
<p><em>CouchDB + Another Layer as Web Server is Redundant</em></p>
<p>After reading a little about CouchDB, I thought it would be best paired with something like <a href="http://www.sitepen.com/blog/2010/07/14/multi-node-concurrent-nodejs-http-server/">multi Node.js</a> as a web server. What I failed to realize was that CouchDB has a server baked in to each database. According to this <a href="http://stackoverflow.com/questions/3618052/should-i-connect-directly-to-couchdbs-socket-and-pass-http-requests-or-use-node">Stack Overflow question</a> CouchDB is capable of handling a heavy load all on it's own.</p>
<blockquote><p>CouchDB inherits super concurrency handling from Erlang, the language it was written in. Erlang uses lightweight processes and message passing between those processes to achieve excellent performance under high concurrent load. It will take advantage of all cpu cores, too.<br />
...<br />
Both should easily handle tens of thousands of connections, but I would expect CouchDB to handle concurrency better (and with less effort on your part) than Node. And keep in mind that Node adds some latency if you put it in front of CouchDB. That may only be noticeable if you have them on different machines, though.</p>
<p>Writing directly to Couch via TCPSocket is a-ok as long as your write a well-formed HTTP request that follows the spec. (You're not passing a faux request...that's a real HTTP request you're sending just like any other.)</p></blockquote>
<p><em>How CouchDB is Architected</em></p>
<p>Internal storage is JSON data in a <a href="http://guide.couchdb.org/editions/1/en/btree.html">B-Tree</a> structure. This framework enables O(log N) speed lookups, insertions and deletions. The following diagram, from the definitive guide eventual consistency section, shows how a view request is handled:</p>
<p><a href="http://guide.couchdb.org/editions/1/en/consistency.html#key"><img class="aligncenter size-full wp-image-5072" title="GetRequest" src="{{ site.url }}/assets/2010/09/GetRequest.png" alt="" width="578" height="442" /></a></p>
<p>An important restriction that feeds directly into CouchDB's ability to scale, documents are accessible <a href="http://guide.couchdb.org/editions/1/en/consistency.html#key">only by key</a>, and rely on multi-version concurrency control to manage concurrent access (no locking).</p>
<p style="text-align: center;"><a href="http://guide.couchdb.org/editions/1/en/consistency.html#key"><img class="aligncenter size-full wp-image-5073" title="NoLocking" src="{{ site.url }}/assets/2010/09/NoLocking.png" alt="" width="636" height="209" /></a></p>
<p><em>When to use CouchDB</em></p>
<p>At the <a href="http://www.infoq.com/news/2010/06/couchdb">Berlin Buzzwords conference</a> Jan Lehnardt (coauthor of the definitive guide) described compelling benefits of CouchDB as a choice platform for distributed web apps.</p>
<blockquote>
<ul>
<li>ease of installation</li>
<li>document based</li>
<li>JSON as the common subset of data types shared by all programming languages</li>
<li>Well behaved HTTP/REST interface and API</li>
<li>Clean and simple two tier applications (html+javascript in the browser + couch+javascript as server)</li>
<li>Couch Apps</li>
<li>Ability to scale up and DOWN</li>
<li>Availability on many platforms/devices, also mobile (Android, Nokias Maemo/MeeGo and hints on iPhone versions)</li>
<li>Built in synchronisation, conflict handling and replication</li>
<li>Performance</li>
<li>Views generated via map/reduce in javascript</li>
<li>Database change notification support via HTTP-Socket</li>
</ul>
</blockquote>
<p>Notes:</p>
<p>*= there are many NoSQL database formats: Redis,  MongoDB, Cassandra, memcacheDB, Big Table, etc.</p>
<p>^= My very limited experience is with <a href="http://vmx.cx/cgi-bin/blog/index.cgi/geocouch-geospatial-queries-with-couchdb:2008-10-26:en,CouchDB,Python,geo">GeoCouch</a>, Tyler's choice for <a href="http://victusmedia.com">Victus Media's</a> location based <a href="http://garagedollar.com">GarageDollar</a> service. Installation instructions from source for GeoCouch can be found here at <a href="http://github.com/jhs/build-couchdb">Jason Smith's batteries included CouchDB build system</a> (see Cheat Codes). Starting with Ubuntu 9.1 and beyond, vanilla couchDB comes pre-installed on Ubuntu distributions.</p>
<p>Just a few of my favorite CouchDB references:</p>
<ul>
<li><a href="http://guide.couchdb.org/editions/1/en/index.html">The Definitive Guide to CouchDB</a></li>
<li><a href="http://wiki.apache.org/couchdb/">The Apache CouchDB Wiki</a></li>
<li><a href="http://github.com/jhs/build-couchdb">Jason Smiths build-couchdb</a></li>
<li><a href="http://vmx.cx/cgi-bin/blog/index.cgi/geocouch-the-future-is-now:2010-05-03:en,CouchDB,Python,Erlang,geo">vmx's GeoCouch: the future is now</a></li>
<li><a href="http://www.couchapp.org/page/getting-started">Getting Started</a></li>
<li><a href="http://wiki.github.com/couchapp/couchapp/">couchapp</a></li>
<li><a href="http://stackoverflow.com/questions/tagged/couchdb">Stack Overflow's CouchDB tagged questions</a></li>
</ul>
