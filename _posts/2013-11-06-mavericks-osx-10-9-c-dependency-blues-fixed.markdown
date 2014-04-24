---
layout: post
status: publish
published: true
title: Mavericks, OSX 10.9 c++ dependency blues -> Fixed
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 10044
wordpress_url: http://www.victusspiritus.com/?p=10044
date: '2013-11-06 15:09:50 -0500'
date_gmt: '2013-11-06 22:09:50 -0500'
categories:
- Uncategorized
tags:
- apple
- c++
- osx
- homebrew
comments: []
---
<p>This is a quick shout to folks who are suffering with the latest version of osx breaking all their locally <a title="homebrew" href="http://brew.sh/">homebrewed</a> (or otherwise installed) applications. This is not <strong>the only</strong> or <strong>best</strong> way to install software on your Mac, but it worked for my configuration.</p>
<p>First I rebuilt my critical c++ tools using clang++ and libc++ by modifying brew formulas with the following additional section (c stuff was aok):<br />
<script src="https://gist.github.com/victusfate/7345295.js"></script></p>
<p>Then in any native nodejs modules I had that referenced symbolic libraries I used the following section in bindings.gyp<br />
<script src="https://gist.github.com/victusfate/7345319.js"></script></p>
<p><a href="https://gist.github.com/victusfate/7344987">Examples</a> of customized homebrew formulas to link with libc++.</p>
