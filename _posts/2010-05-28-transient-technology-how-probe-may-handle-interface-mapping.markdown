---
layout: post
status: publish
published: true
title: Transient Technology, how probe may handle interface mapping
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 3980
wordpress_url: http://www.victusspiritus.com/?p=3980
date: '2010-05-28 05:47:54 -0400'
date_gmt: '2010-05-28 12:47:54 -0400'
categories:
- Uncategorized
tags:
- coding
- probe
- design
comments:
- id: 4627
  author: Analogy and Machine Intelligence | Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/06/27/analogy-and-machine-intelligence/
  date: '2010-06-27 15:56:20 -0400'
  date_gmt: '2010-06-27 22:56:20 -0400'
  content: "[...] or specialized algorithms developed to benefit them. I hinted at
    this topic earlier in the notes section of a post on a language designed to take
    advantage of comparing data with possible interfaces. But [...]"
- id: 9718
  author: Probabilistic Nondeterministic Programming &mdash; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/30/probabilistic-nondeterministic-programming/
  date: '2011-03-30 06:43:18 -0400'
  date_gmt: '2011-03-30 13:43:18 -0400'
  content: "[...] how probe may handle interface mapping [...]"
---
<p>The intentional interconnection of technology happens at surfaces that are matched*. No matter how well thought out, interface assumptions must iteratively adapt to a dynamic data environment. Information and data rarely maintain the same formats, rates, and sizes over time. As much as I'd prefer to never have to write another data reformatter, it is silly to expect other technologies to stand still. What happens when an interface changes, but all of the needed data to satisfy that new interface is readily available? A developer has to go back into that code and manually write up a new interface or retrofit the existing interface to maintain backwards compatibility. This usually produces some hard to maintain and read code over time. Old code has a way of evolving into a thing out of nightmares.</p>
<h2>Smarter Mapping Utilities in probe</h2>
<p>A couple of days ago I described the beginning of a top down designed programming language, <a HREF="http://victusfate.github.io/victusspiritus/uncategorized/2010/05/26/probe-a-fictional-programming-language-design/">probe</a>. This design effort is defined by what I want as an application builder first, with only a hint of implementation details ruminating in my subconscious. </p>
<p>One of the primary design goals I have specified for probe is an advanced interface mapping framework. I'd like to automate as much data reshaping as possible in order to minimize developer time for these tasks. One way interfaces are handled for dynamic or duck typed objects is referencing by method name. If an object has <I>quack</I> it is easily mapped to interfaces that call the <I>quack</I> method. What happens if a needed method is missing? </p>
<p>There are a variety of ways methods can handle the absence of a called method.  </p>
<ul>
<li>New nominal methods can be appended to objects without <i>quack</i></li>
<li>a functioning method can be created on the fly^, constructed from other needed methods. This way an object is scanned for a mininum set of builder methods and <I>quack</I> is created and appended to the object</li>
<li>an error can be raised for a required method, without sufficient builder methods to construct <I>quack</I></li>
</ul>
<p>The act of passing an object to a method can mutate the object. Methods are able to dynamically modify objects**. </p>
<h2>Data I/O blues</h2>
<p>A problem occurs if the input format isn't in a format the software has encountered before. Markup languages like XML, JSON, and RDF attempt to generalize the description of information to grease the wheels for self describing data. A strategy for probe to handle new data is to rely on common descriptions within namespaces. In this way probe can mimick the way dynamic methods are handled for new data formats. Dynamic objects or data are "probed" for building blocks to synthesize required interfaces. New object types can be described in data file formats by leveraging library specified core structures.</p>
<p>A couple of open questions/ideas:</p>
<ul>
<li>How dangerous is it to comingle one's source with data?</li>
<li>Is there an "organic" way novel structures described in data can move into libraries for wider usage & optimization?</li>
<li>Nearly identical data objects can converge into a common library object</li>
<li>The core language interpreter and default librares will be adapted by it's usage, and specialized dialects spun off (Lisp-like)</li>
<li>Can the language benefit from the variety of source already developed in other languages through translation tools?</li>
</ul>
<p>Notes:<br />
* & ^ = Unintended matching surfaces of technology and information can yield wonderful breakthroughs. Enabling this type of serendipity within programming languages is possible with probe. The trick is an application of the generalized <a href="http://grou.pe/">Hive Mind</a> idea <a href="http://blog.botfu.com">Kevin Marshall</a> inspired me to think more about after we discussed it over burgers earlier in the month. The generalized hive mind idea is to expose two or more unmatched sets to look for revealing commonality or missing features. In the case of missing methods we're looking for raw builder methods to satisfy an interface by synthesis.</p>
<p>** = Handling dynamic objects in a fast way is a tough problem (optimizing common structures is much easier than optimizing for malleable objects). Luckily I'm designing this language from a application developers perspective ;). </p>
