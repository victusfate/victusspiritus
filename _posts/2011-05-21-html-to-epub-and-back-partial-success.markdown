---
layout: post
status: publish
published: true
title: HTML to ePub and back, partial success
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8961
wordpress_url: http://www.victusspiritus.com/?p=8961
date: '2011-05-21 07:25:22 -0400'
date_gmt: '2011-05-21 14:25:22 -0400'
categories:
- Uncategorized
tags:
- web/tech
- epublishing
comments:
- id: 10011
  author: Mike Cane
  author_email: ''
  author_url: http://twitter.com/mikecane
  date: '2011-05-21 15:13:00 -0400'
  date_gmt: '2011-05-21 15:13:00 -0400'
  content: "&gt;&gt;&gt;Convert an intriguing site (Python for Fun) from html to epub
    to enable easy mobile or tablet reading while offline.\n\nHello!  Just get the
    dotepub browser extension!  It will convert just about any site to an ePub file. 
    I use it a LOT.  They just added capturing images too although if there are more
    than 10 or they are large, it will say you can have only the text.\n\nhttp://dotepub.com/\n "
- id: 10014
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-05-21 21:51:00 -0400'
  date_gmt: '2011-05-21 21:51:00 -0400'
  content: Mr. Cane you rule, gracias!
---
<h2>What I'd like to accomplish with epublishing software:</h2>
<ol>
<li>Convert an intriguing site (<a href="http://openbookproject.net/py4fun/">Python for Fun</a>) from html to epub to enable easy mobile or tablet reading while offline. Automate that process for future sites which I enjoy and which have far more content than I can consume in one sitting.</li>
<p><br/></p>
<li>Convert an existing PDF (<a href="http://victusgames.com/Welcome_to_Victus_Games.html">Children of the Ark</a>) document into a living editable wiki/web site. There are plenty of static PDFs which beg to be opened for editing by the public. Our game beta is just one of them.</li>
<p><br/></p>
<li>Convert select topics and posts from this blog into a transportable epub friendly format. I often refer to earlier blog posts. It's fun to review what and how I thought before, and how my understanding has changed with time. Some readers prefer focused batches of content in pamphlet and book forms. I should be able to easily deliver that by organizing a few dozen posts into bundled ebook content.</li>
</ol>
<p>This morning's post discusses a first crack at the former. I'm hung up at a reasonable quality PDF to ePub stage. Another path of going directly from html to ePub may prove more fruitful.</p>
<h2>Scanning the web for tools</h2>
<p>After reading a number of questionable looking sites providing enormous amounts of information about how to use their $40-50 dollar tool to convert from one format to another I happened upon a google code tool called wkhtmltopdf. This provided the foundation for the conversion from html to pdf, one step in converting to a bundled format. I documented the transformation of Python for Fun into PDF form on <a href="https://github.com/victusfate/Python-for-Fun-by-Chris-Meyers">github</a>, and it was straightforward.</p>
<blockquote>
<h2>What is wkhtmltopdf?</h2>
<h3>Description</h3>
<p>Simple shell utility to convert html to pdf using the webkit rendering engine, and qt. </p>
<h3>Introduction</h3>
<p>Searching the web,  I have found several command line tools that allow you to convert a HTML-document to a PDF-document, however they all seem to use their own, and rather incomplete rendering engine,  resulting in poor quality. Recently QT 4.4 was released with a WebKit widget (WebKit is the engine of Apples Safari, which is a fork of the KDE KHtml), and making a good tool became very easy. (from wkhtmltopdf site)</p>
</blockquote>
<p>Here's how I proceeded so far:</p>
<blockquote>
<p>Converted local html to pdf with <a href="http://code.google.com/p/wkhtmltopdf/">wkhtmltopdf</a><br><br />
Script:   </p>
<pre style="overflow:scroll;">/Applications/wkhtmltopdf cover index.html collection.html toc lode/lode.html buckets/buckets.html tower/tower.html animal/animal.html gui/tkPhone.html gui/sqlPhone.html gui/wxPhone.html erlang/erlang.html erlang/erlang2.html forth/forth.html lisp/lisp.html prolog/intro.html prolog/prolog1.html prolog/prolog2.html prolog/prolog3.html huffman/huffman.html rtn/rtn.html sir/sir.html unicode/unicode.html logic/logic.html logic2/logic2.html mm/simulator.html mm/assembler.html mm/compiler.html sql/sql.html wave/wave.html py4fun.pdf
</pre>
<p>output pdf:<br><br />
<a href="https://github.com/victusfate/Python-for-Fun-by-Chris-Meyers/blob/master/py4fun.pdf?raw=true">py4fun.pdf</a></p>
<ol>
<li>First attempt at pdf to epub:<br />
<blockquote><p>
    uploaded and converted pdf to epub with <a href="http://www.2epub.com/">2epub.com</a>  </p>
<ol>
<li>Browse to pdf file</li>
<li>upload file</li>
<li>download epub</li>
</ol>
<p>    First epub:<br />
    <a href="https://github.com/victusfate/Python-for-Fun-by-Chris-Meyers/raw/master/orig_py4fun.epub">orig_py4fun.epub</a>  (360kbytes)</p>
<p>    But the links weren't working in that file on my iOS devices...
    </p></blockquote>
</li>
<li>Second try:<br />
<blockquote><p>
I used the Mac Store PDF Converter (by Shenzhen Wondershare Software Co. Ltd) to create py4fun.epub (11mbytes). The quality of the output epub was much lower than the free version.<br />
output file: deleted.
</p></blockquote>
</li>
<li>Third try:<br />
<blockquote><p>
I snagged <a href="http://www.lexcycle.com/desktop">Lexcycle Stanza</a> for the desktop. It imported the PDF kinda funky and requested access to a PDF viewer. Begrudgingly, I reinstalled Adobe's PDF reader again (~420mbytes) and it opened the file fine. But this time the option to export to epub wasn't available. Bollocks!
</p></blockquote>
</ol>
</blockquote>
<p>Unfortunately the process of transforming the PDF to ePub file proved even more frustrating. The first site I tried broke all the internal hyperlinks (2epub.com), but at least created a mostly readable epub file (some code sample formatting was lost). </p>
<p>The second tool I tried was a $60 dollar download from the Mac App Store, so I expected a high quality product. Instead what I purchased was a steaming pile of crap. It generated a huge output file (~30 times the size of the free epub file) full of broken hyper links and random blank pages. Definitely do not buy that terrible software: PDF Converter (by Shenzhen Wondershare Software Co. Ltd).</p>
