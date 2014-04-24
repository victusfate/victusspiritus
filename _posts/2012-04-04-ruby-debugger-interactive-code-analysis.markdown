---
layout: post
status: publish
published: true
title: Ruby Debugger, interactive code analysis
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9976
wordpress_url: http://www.victusspiritus.com/?p=9976
date: '2012-04-04 06:34:39 -0400'
date_gmt: '2012-04-04 13:34:39 -0400'
categories:
- Uncategorized
tags:
- coding
- ruby
comments: []
---
<p>Hat tip to <a href="http://intridea.com/blog/2010/12/7/debug_rails_application_with_ruby-debug">intridea</a>, and of course the definitive documentation <a href="http://guides.rubyonrails.org/debugging_rails_applications.html">guides.rubyonrails.org</a>.</p>
<p>1) install the gem.<br />
<script src="https://gist.github.com/2301049.js?file=install.sh"></script></p>
<p>2) place the hook. Enter "debugger" where ever you want your debugging session to begin.<br />
<script src="https://gist.github.com/2301049.js?file=example_debugger.rb"></script></p>
<p>3) navigate the code</p>
<blockquote><p>
h is for help, what can you do<br />
l is for list, where are you in the code<br />
n is for next line, step over<br />
s is for step in<br />
fin is for finish / step out<br />
p is for print, p <var>
</p></blockquote>
<p>That's it.</p>
<p>There's more to it, but that should be enough to understand and evaluate the state of your code.</p>
