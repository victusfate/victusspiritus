---
layout: post
status: publish
published: true
title: Brushing Up on Computer Science Part 2, Object Oriented Programming (OOP)
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 7682
wordpress_url: http://www.victusspiritus.com/?p=7682
date: '2011-03-15 05:33:59 -0400'
date_gmt: '2011-03-15 12:33:59 -0400'
categories:
- Uncategorized
tags:
- career counseling
- coding
- computer science
comments:
- id: 9360
  author: David Semeria
  author_email: david@lmframework.com
  author_url: http://lmframework.com
  date: '2011-03-15 12:54:00 -0400'
  date_gmt: '2011-03-15 12:54:00 -0400'
  content: |-
    Hi Mark, I think abstraction is the greatest gift modern language design has given us. Unfortunately, it's also the most abused aspect of programming in my humble opinion.

    My favourite tweet (origin unknown) is "Another kid gets out of bed and another abstraction is born".

    Abstraction only makes sense if you know people are unlikely to ever need to peel back the layer, otherwise it just adds confusion.

    I don't know (or care) how this text I'm writing gets sent down the line as electrical impulses to Disqus' servers - that's abstraction at its best....
- id: 9373
  author: Brushing up on Computer Science Part 1, Big O &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/14/brushing-up-on-computer-science-part-1-big-o/
  date: '2011-03-15 08:44:34 -0400'
  date_gmt: '2011-03-15 15:44:34 -0400'
  content: "[...] Object Oriented Programming [...]"
- id: 9375
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-03-15 15:54:00 -0400'
  date_gmt: '2011-03-15 15:54:00 -0400'
  content: Wise words friend.
- id: 9445
  author: Brushing Up on Computer Science Part 3, Data Structures &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/16/brushing-up-on-computer-science-part-3-data-structures/
  date: '2011-03-16 05:04:16 -0400'
  date_gmt: '2011-03-16 12:04:16 -0400'
  content: "[...] Object Oriented Programming [...]"
- id: 9496
  author: Blktiger
  author_email: blktiger@gmail.com
  author_url: ''
  date: '2011-03-17 04:49:00 -0400'
  date_gmt: '2011-03-17 04:49:00 -0400'
  content: You didn't mention Finalize vs Destructors. The finalize method is like
    a destructor but is called before an object is garbage collected.
- id: 9515
  author: Brushing Up on Computer Science Part 4, Algorithms &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/17/brushing-up-on-computer-science-part-4-algorithms/
  date: '2011-03-17 06:34:44 -0400'
  date_gmt: '2011-03-17 13:34:44 -0400'
  content: "[...] Object Oriented Programming [...]"
- id: 9528
  author: Brushing up on Computer Science Part 5, Graphs, Networks, and Operating
    Systems &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/17/brushing-up-on-computer-science-part-5-graphs-networks-and-operating-systems/
  date: '2011-03-17 15:58:21 -0400'
  date_gmt: '2011-03-17 22:58:21 -0400'
  content: "[...] Object Oriented Programming [...]"
---
<p>"I paint objects as I think them, not as I see them."<br />
Pablo Picasso</p>
<p>This is the second part in a brief review of a selection of topics from Computer Science.</p>
<ol>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/14/brushing-up-on-computer-science-part-1-big-o/">Intro and Big O</a></li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/15/brushing-up-on-computer-science-part-2-object-oriented-programming-oop/">Object Oriented Programming</a></li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/16/brushing-up-on-computer-science-part-3-data-structures/">Data Structures</a>: arrays, lists, trees, hash tables</li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/17/brushing-up-on-computer-science-part-4-algorithms/">Algorithms</a> (searches, sorts, maths!)</li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/17/brushing-up-on-computer-science-part-5-graphs-networks-and-operating-systems/">Graphs, Networks, and Operating Systems</a></li>
</ol>
<p>The content within this post focuses on one of the most popular software design pattern groups, <a href="http://en.wikipedia.org/wiki/Object-oriented_programming">OOP</a>. In fact our encyclopedic ally wikipedia refers to OOP as a paradigm.</p>
<blockquote><p>Object-oriented programming (OOP) is a programming paradigm using "objects" – data structures consisting of data fields and methods together with their interactions – to design applications and computer programs. Programming techniques may include features such as data abstraction, encapsulation, messaging, modularity, polymorphism, and inheritance. Many modern programming languages now support OOP.</p></blockquote>
<p>For several popular languages OOP is grafted on, a set of features nearly at odds with the core intent of their host language. In contrast there are a handful of languages crafted where encapsulation is essential to their design (syntax and semantics). <a href="http://en.wikipedia.org/wiki/Smalltalk">SmallTalk</a>, <a href="http://diveintopython3.org/your-first-python-program.html#everythingisanobject">Python</a> and <a href="http://www.ruby-lang.org/en/about/">Ruby</a> are prominent examples where everything is an object.</p>
<p>Let's dive right into to some of the terminology rattled off by Steve Yegge in <a href="http://sites.google.com/site/steveyegge2/five-essential-phone-screen-questions">Five Essential Phone Screen Questions</a>. Anyone who can call out this list of constructs off the top of their head is an OOP <a href="http://en.wikipedia.org/wiki/Equilibrium_(film)">Grammaton Cleric</a>.</p>
<blockquote>
<ol>
<li>class, object (and the difference between the two)</li>
<li>instantiation</li>
<li>method (as opposed to, say, a C function)</li>
<li>virtual method, pure virtual method</li>
<li>class/static method</li>
<li>static/class initializer</li>
<li>constructor</li>
<li>destructor/finalizer</li>
<li>superclass or base class</li>
<li>subclass or derived class</li>
<li>inheritance</li>
<li>encapsulation</li>
<li>multiple inheritance (and give an example)</li>
<li>delegation/forwarding</li>
<li>composition/aggregation</li>
<li>abstract class</li>
<li>interface/protocol (and different from abstract class)</li>
<li>method overriding</li>
<li>method overloading (and difference from overriding)</li>
<li>polymorphism (without resorting to examples)</li>
<li>is-a versus has-a relationships (with examples)</li>
<li>method signatures (what's included in one)</li>
<li>method visibility (e.g. public/private/other)</li>
</ol>
</blockquote>
<p><em>A series of OOP definitions, made as human friendly as possible (many are open to interpretation)</em></p>
<p>A class is a definition for an object, and serves as blueprints. An object is an instance of a class. </p>
<p>Methods are functions defined in classes and operate on object data or members, or are purely required interfaces (pure virtual methods). A method signature is the syntax which declares the methods interface (name, arguments, returned objects, visibility).</p>
<p>A class containing pure virtual functions is referred to as an abstract class and may contain other method definitions and state information, an interface serves a similar role but has no state or implementation*. </p>
<p>A derived or subclass inherits an interface and structure from a base, super or parent class^. Virtual methods enable subclasses to replace or augment method implementation of the parent class. Method overriding describes subclasses replacing super class members with identical signatures. Method overloading describes multiple methods which share the same name but have varied signatures. </p>
<p>A static method is defined once for all object instances, while class methods are defined for each instance. Likewise, static initializers are performed once per class, while class initializers are called for each instance. </p>
<p>A constructor call is made whenever an object is created, while a destructor method is called whenever an object is destroyed to release required resources (<a href="http://images.wikia.com/starwars/images/b/b1/Exds.jpg">this is what destructors look like</a>). Methods are encapsulated with data through bundling or restricted access.</p>
<p>Polymorphism allows various data types to be handled with a uniform interface. <i>"Parametric polymorphism allows a function or a data type to be written generically, so that it can handle values identically without depending on their type"</i> (<a href="http://en.wikipedia.org/wiki/Polymorphic_%28computing%29#Parametric_polymorphism">parametric polymorphism</a>)</p>
<p>Simple example of polymorphism:<br />
<script src="https://gist.github.com/870626.js?file=c%2B%2B%20polymorphic%20example"></script></p>
<p>Multiple inheritance occurs when a subclass inherits traits from multiple super classes. An example of multiple inheritance is the infamous killer-clown class which inherits attributes and methods from aliens and space-monsters.</p>
<p>Delegation is defined as routing method calls from one object to another. Deferring a task to another object, defines the receiving object as the delegate. Delegation may occur at run time unlike most inheritance which is defined with the class type (<a href="http://en.wikipedia.org/wiki/Delegation_%28programming%29#As_a_language_feature">reference</a>). An example of delegation occurs in Cocoa when GUI elements actions send notifications to the app controller class.</p>
<p>Method visibility is important for defining encapsulation by restriction. A member or method may be public, protected or private. Private visibility allows only class member access to the method or member. Protected visibility enables class and child class access. Public visibility allows ubiquitous access to the entire cosmos of calling programs.</p>
<p>Relationships between classes can be categorized as is-a versus has-a. Is-a defines an inherited or strict type, as in <i>I am (mostly) human</i>. Has-a defines a container or ownership relation, ie <i>I have a piece of bacon</i>. Object aggregation or composition occurs when container classes have several member classes (has-a). Complex structures can be built up from simple members. When a Composition is destroyed, so are all of it's member objects (the database containing these posts). Aggregation describes an order of several objects, but the parts remain after the destruction of the whole (glass jar of marbles).</p>
<div style="width:425px" id="__ss_1489191"> <strong style="display:block;margin:12px 0 4px"><a href="http://www.slideshare.net/jmgimeno/objectoriented-programming-in-python" title="Object-oriented Programming in Python">Object-oriented Programming in Python</a></strong> <object id="__sse1489191" width="425" height="355"><param name="movie" value="http://static.slidesharecdn.com/swf/ssplayer2.swf?doc=classes-090526052058-phpapp02&stripped_title=objectoriented-programming-in-python&userName=jmgimeno" /><param name="allowFullScreen" value="true"/><param name="allowScriptAccess" value="always"/><embed name="__sse1489191" src="http://static.slidesharecdn.com/swf/ssplayer2.swf?doc=classes-090526052058-phpapp02&stripped_title=objectoriented-programming-in-python&userName=jmgimeno" type="application/x-shockwave-flash" allowscriptaccess="always" allowfullscreen="true" width="425" height="355"></embed></object>
<div style="padding:5px 0 12px"> View more <a href="http://www.slideshare.net/">presentations</a> from <a href="http://www.slideshare.net/jmgimeno">Juan-Manuel Gimeno</a> </div>
</p></div>
<div id="__ss_203408" style="width: 425px;"><strong style="display: block; margin: 12px 0 4px;"><a title="Object Oriented Programming with Java" href="http://www.slideshare.net/backdoor/object-oriented-programming-with-java">Object Oriented Programming with Java</a></strong> <object id="__sse203408" width="425" height="355"><param name="movie" value="http://static.slidesharecdn.com/swf/ssplayer2.swf?doc=object-oriented-programming-with-java-1197643931263339-3&amp;stripped_title=object-oriented-programming-with-java&amp;userName=backdoor" /><param name="allowFullScreen" value="true" /><param name="allowScriptAccess" value="always" /><embed type="application/x-shockwave-flash" width="425" height="355" src="http://static.slidesharecdn.com/swf/ssplayer2.swf?doc=object-oriented-programming-with-java-1197643931263339-3&amp;stripped_title=object-oriented-programming-with-java&amp;userName=backdoor" name="__sse203408" allowscriptaccess="always" allowfullscreen="true"></embed></object></p>
<div style="padding: 5px 0 12px;">View more <a href="http://www.slideshare.net/">presentations</a> from <a href="http://www.slideshare.net/backdoor">backdoor</a></div>
</div>
<div id="__ss_1397762" style="width: 425px;"><strong style="display: block; margin: 12px 0 4px;"><a title="Object Oriented Programming In .Net" href="http://www.slideshare.net/gregsohl/object-oriented-programming-in-net-1397762">Object Oriented Programming In .Net</a></strong> <object id="__sse1397762" width="425" height="355"><param name="movie" value="http://static.slidesharecdn.com/swf/ssplayer2.swf?doc=objectorientedprogrammingin-net-090506224235-phpapp02&amp;stripped_title=object-oriented-programming-in-net-1397762&amp;userName=gregsohl" /><param name="allowFullScreen" value="true" /><param name="allowScriptAccess" value="always" /><embed type="application/x-shockwave-flash" width="425" height="355" src="http://static.slidesharecdn.com/swf/ssplayer2.swf?doc=objectorientedprogrammingin-net-090506224235-phpapp02&amp;stripped_title=object-oriented-programming-in-net-1397762&amp;userName=gregsohl" name="__sse1397762" allowscriptaccess="always" allowfullscreen="true"></embed></object></p>
<div style="padding: 5px 0 12px;">View more <a href="http://www.slideshare.net/">presentations</a> from <a href="http://www.slideshare.net/gregsohl">Greg Sohl</a></div>
</div>
<div style="width:425px" id="__ss_1995516"> <strong style="display:block;margin:12px 0 4px"><a href="http://www.slideshare.net/kwatch/basic-mechanism-of-oopl" title="Basic Mechanism of OOPL">Basic Mechanism of OOPL</a></strong> <object id="__sse1995516" width="425" height="355"><param name="movie" value="http://static.slidesharecdn.com/swf/ssplayer2.swf?doc=basicmecanismofoopl-090914101335-phpapp02&stripped_title=basic-mechanism-of-oopl&userName=kwatch" /><param name="allowFullScreen" value="true"/><param name="allowScriptAccess" value="always"/><embed name="__sse1995516" src="http://static.slidesharecdn.com/swf/ssplayer2.swf?doc=basicmecanismofoopl-090914101335-phpapp02&stripped_title=basic-mechanism-of-oopl&userName=kwatch" type="application/x-shockwave-flash" allowscriptaccess="always" allowfullscreen="true" width="425" height="355"></embed></object>
<div style="padding:5px 0 12px"> View more <a href="http://www.slideshare.net/">presentations</a> from <a href="http://www.slideshare.net/kwatch">kwatch</a> </div>
</p></div>
<blockquote><p>When the mind's eye rests on objects illuminated by truth and reality, it understands and comprehends them, and functions intelligently; but when it turns to the twilight world of change and decay, it can only form opinions, its vision is confused and its beliefs shifting, and it seems to lack intelligence.
</p></blockquote>
<p>Plato, Republic</p>
<p>Notes:<br />
*= Differences between abstract classes and interfaces references: <a href="http://stackoverflow.com/questions/761194/interface-vs-abstract-class-general-oo/761342#761342">1</a>,<a href="http://stackoverflow.com/questions/558164/how-do-you-decide-between-using-an-abstract-class-and-an-interface/558173#558173">2</a>,<a href="http://www.codeproject.com/KB/cs/abstractsvsinterfaces.aspx">3</a></p>
<p>^= Beware the <a href="http://en.wikipedia.org/wiki/Yo-yo_problem">Yo-Yo</a> problem. Long lived layered libraries that continue to change are particularly vulnerable to an issue of complex inheritance. As I've gotten older (and hopefully a bit wiser), I much prefer a concise dynamic interface to widely distributed class interfaces.</p>
