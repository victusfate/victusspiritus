---
layout: post
status: publish
published: true
title: Dynamic scripting with static speed, the best of both worlds
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 6961
wordpress_url: http://www.victusspiritus.com/?p=6961
date: '2011-01-28 13:14:34 -0500'
date_gmt: '2011-01-28 20:14:34 -0500'
categories:
- Uncategorized
tags:
- coding
comments:
- id: 8214
  author: Frank
  author_email: victusspiritus.com@frankhirsch.net
  author_url: ''
  date: '2011-01-29 10:54:00 -0500'
  date_gmt: '2011-01-29 10:54:00 -0500'
  content: |
    I am right now working on something just like that.
    As a seasoned professional embedded software developer my language of choice is usually C. I need it because of its speed and small memory footprint. But C is not up to date in the language features department. Therefore I wrote an interpreter for a C-like language with scripting features, especially reflection. I am right now in the process of coding the part which dumps the parts of the program that do not use any dynamic features to C source code.
    My goal is to be able to write embedded software and a dynamic testing framework for the software in the same language. Especially the testing framework will benefit from the scripting features of the langage, and will greatly reduce the work of testing the high-level functionality of the distributed embedded systems I am developing to pay my mortgage.
    Also metaprogramming and manipulation of the embedded code by higher order functions will be possible. After code manipulation and high-level testing are done, I will dump the resulting embedded code to C and cross-compile it to the target platform.
    And on top of all that, the whole ongoing process is a freaking joyride, i.e. I'm having fun playing with my very own language, with is specifically designed to please me and to support the coding style I prefer! ;-)
- id: 8215
  author: DGentry
  author_email: denny+disqus@geekhold.com
  author_url: http://codingrelic.geekhold.com
  date: '2011-01-29 13:45:00 -0500'
  date_gmt: '2011-01-29 13:45:00 -0500'
  content: |-
    Just a couple years ago when looking to add a dynamically scriptable feature to a large C/C++ project, the main choices were Tcl and Lua. Python and Ruby, though wonderful languages, really want to run their interpreter as the main loop of a process and delegate calls out to C/C++ extensions. They are not particularly amenable to being embedded.

    The next time something like this comes up, I suspect V8 will be the best choice. Its normal operation is embedded within a large block of C++ code, such that I hope integration would be easier. Additionally JavaScript has an active ecosystem around it the way Lua never had and which has mostly dissipated from Tcl.
- id: 8216
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-01-29 15:23:00 -0500'
  date_gmt: '2011-01-29 15:23:00 -0500'
  content: |+
    I had a feeling you may have come across something like this, great to hear about practical experience and your take on javascript being a natural fit.

    For glue languages I was under the impressions they'd coordinate the flow of data to different specialized execution blocks, but hadn't spent much thought about how interpreters might bottleneck event loops. There a cozy space between threads, processes, systems, and really big networks, and paying for an interpreter side by side can get expensive quick.


- id: 8217
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-01-29 15:28:00 -0500'
  date_gmt: '2011-01-29 15:28:00 -0500'
  content: What an inspirational and awesome adventure Frank, I'm jealous :). From
    the sounds of it you've nailed a real problem and can use it to navigate and prioritize
    how you build out language features. You can leverage paying customers to fuel
    your craft.
- id: 8223
  author: Frank
  author_email: victusspiritus.com@frankhirsch.net
  author_url: ''
  date: '2011-01-30 10:57:00 -0500'
  date_gmt: '2011-01-30 10:57:00 -0500'
  content: |+
    Thank you very much for the kind words!
    I am naturally very exited about the whole thing, hence the rather long comment.
    Maybe I should be doing a little writeup about it at one point or another...

---
<p>Many dream of success. A rare few focus on grand visions to reshape the future. Me, I fantasize about ideal software structures*. </p>
<p>Just a few days back I dreamt of middleware that would take completely dynamic objects and map required information into static structures which are connected to blazing fast compiled pipelines. In other words, flexible routing tables that bind dynamic to static objects, in tandem with interpreted scripts which call compiled code. This is something that I not only think is cool, but can readily apply. This form of middleware opens the door to scripting languages calling compiled c++ libraries at my day job. If you do this type of thing, I'd love to hear from you.</p>
<p><i>Highly desirable forms lead to blindspots</i></p>
<p>While this idea was baking in the background of my noodle, I scanned the following tweet from <a href="http://twitter.com/andraz">Andraz Tori</a> (CTO of Zemanta):<br />
[blackbirdpie url='http://twitter.com/andraz/status/30571012311482368']<br />
Protocol buffers transfer encoded data into binary streams. Not only are dynamic calls to thinly wrapped compiled code happening, they're common place. In the HackerNews post Andraz referred to, several folks commented on their own development of rapid protocol buffers callable from Python. So the I/O layer was already well developed.</p>
<p><i>*Cough* Node.js Yo</i></p>
<p>Speaking of dynamic scripting language bindings to compiled c++ code, what about <a href="http://nodejs.org/">node.js</a>? I've read a good deal of documentation on node, and toyed around with servers. One of my favorite high level descriptions of node is a post by Denton Gentry, <a href="http://codingrelic.geekhold.com/2010/08/nodejs-from-30000-feet.html">node.js from 30000 feet</a>:</p>
<blockquote><p>
Node.js Overall Structure</p>
<p>The JavaScript implementation in node.js is Google's V8. As mentioned in an earlier article, V8 compiles the source JavaScript directly to machine code the first time it is executed. There is no intermediate bytecode format and no JS interpreter. In addition to V8, node.js relies on libev for its event loop, libeio for asynchronous I/O, and c-ares for asynchronous DNS support. Like everything else in the known universe, it relies on OpenSSL for cryptography and SSL/TLS support.</p>
<p><a href="{{ site.url }}/assets/2011/01/nodejsarch.png"><img src="{{ site.url }}/assets/2011/01/nodejsarch.png" alt="" title="nodejsarch" width="256" height="206" class="aligncenter size-full wp-image-6964" /></a></p>
<p>A standard library in JavaScript is supplied. This provides access to the underlying C++ implementation, and also has helpful bits like a URL parser and a REPL shell for easy experimentation. One thing it does not provide is the DOM. Node.js is not a browser, there is no HTML document to interact with.
</p></blockquote>
<p>There are likely dozens of examples of bindings for dynamic scripting languages to static structures and executable pipelines. For my own personal usage it's just a matter of selecting the right tools for the job after a little more research. I'm leaning towards ruby, javascript or python calling c++ dynamic libraries with narrow exposed interfaces.</p>
<p>Notes:<br />
*= Ideal software structure posts</p>
<ul>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/02/08/each-time-i-get-my-hands-dirty-i-learn/">Each time I get my hands dirty I learn</a></li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/02/11/mind-tools-dynamic-and-static-typing/">Mind tools dynamic and static typing</a></li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/04/03/ideal-coding-easy-to-pickup-yet-abundant-in-function/">Ideal coding easy to pickup yet abundant in function</a></li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/04/20/instant-utility-optimal-execution-syntactic-sugar/">Instant utility optimal execution syntactic sugar</a></li>
</ul>
<p>Probe, loose ideas for a programming language</p>
<ul>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/05/26/probe-a-fictional-programming-language-design/">Probe a fictional programming language</a></li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/05/28/transient-technology-how-probe-may-handle-interface-mapping/">Transient technology how probe may handle interface mapping</a></li>
</ul>
