---
layout: post
status: publish
published: true
title: Even Old Dogs Can Learn New Tricks, Rethinking Interfaces
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 4630
wordpress_url: http://www.victusspiritus.com/2010/07/19/even-old-dogs-can-learn-new-tricks-rethinking-interfaces/
date: '2010-07-19 05:04:17 -0400'
date_gmt: '2010-07-19 12:04:17 -0400'
categories:
- Uncategorized
tags:
- coding
- design
comments: []
---
<p>
<p><strong>Epiphany</strong><br></p>
<p><br><br></p>
<p>After many years of designing software to implement a wide variety of algorithms, late last year I was about to experience a drastic change in thinking that I could never have predicted. I discovered a precious tool or perhaps a more apt name is that it's a key to more productive (less frustrating) software design. When I first visited web programming with scripting languages (php, python, ruby) I attempted to design code to be c++ with a different syntax. I still thought about prescribed heirarchical class interfaces and polymorphism for flexibility. Never did it dawn on me how much mental baggage we carry when we think about objects in only an inheritance centric way. </p>
<p><br><br></p>
<p>Refactoring and rewriting libraries helps, but things change over time. I regularly discovered  something vital missing or the code had to communiate with a different algorithm and was forced to rework all the class interfaces. Baggage. All solved with simple adapters and carefully understanding object state with scripting tools.</p>
<p><br><br></p>
<p><strong>Adapters</strong><br></p>
<p><br><br></p>
<p>It didn't click that classes were malleable with on the fly adapters and that code flow was driven by well designed interfaces until early this year. A method name is like a binding contract, and every object with a getGeolocation function will try and return information in the same way, at least within the scope of an app or library. When well crafted with agnostic data structures (XML,json), interfaces transcend languages much like popular APIs found at Google, Twitter, Microsoft or Yahoo. The essence of an object survives intact from c to python to Ruby to JavaScript when provided over an accessible protocol. </p>
<p><br><br></p>
<p><strong>It's not Static vs Dynamic</strong><br></p>
<p><br><br></p>
<p>Although reading up on duck typed and dynamic languages sped up my renewed understanding of interfaces, the pattern of seeing interfaces differently can apply to my work with static languages. Satisfying interfaces with a high level of abstraction is possible within all programming languages. Encapsulation is an old trick of the object oriented designer, while proxies and dynamic adapters are easily available in newer scripting tools. </p>
<p><br><br></p>
<p>The greatest challenge for me is returning to c++ at my day job from a style and productivity perspective. I haven't come across dynamic languages that feel and read like Ruby that run as fast as static equivalents for taxing numeric computations. Plus we have developed a deep collection of algorithm implementations in c++. Maybe it's time I revisit Rubinius a Ruby implementation using Ruby and c++. At the very least a front end like duby slapped on c/c++ might make reading new application more pleasurable.<br></p>
<p><br><br></p>
<p><br></p>
