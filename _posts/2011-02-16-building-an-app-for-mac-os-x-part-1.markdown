---
layout: post
status: publish
published: true
title: Building an App for Mac OS X Part 1
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 7280
wordpress_url: http://www.victusspiritus.com/?p=7280
date: '2011-02-16 05:41:05 -0500'
date_gmt: '2011-02-16 12:41:05 -0500'
categories:
- Uncategorized
tags:
- coding
- apple
- ruby
- mac os x
- apps
comments:
- id: 9060
  author: Building an App for Mac OS X Part 2 &raquo; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2011/03/01/building-an-app-for-mac-os-x-part-2/
  date: '2011-03-01 07:37:22 -0500'
  date_gmt: '2011-03-01 14:37:22 -0500'
  content: "[...] Building an App for Mac OS X part 1 [...]"
- id: 9063
  author: Robert McGhee &raquo; March 2nd
  author_email: ''
  author_url: http://robertmcghee.co.uk/2011/march-2nd/
  date: '2011-03-02 05:56:38 -0500'
  date_gmt: '2011-03-02 12:56:38 -0500'
  content: "[...] Bookmarked Building an App for Mac OS X Part 1 » Victus Spiritus
    [...]"
---
<p>This is the first post in a series on understanding the basics of developing for the Mac platform. As I proceed with building the app, I'll share helpful documentation and discoveries along the way.</p>
<p>I decided to create my first Mac store app after some encouragement from my wife. While I've created <a href="http://www.victusspiritus.com/2010/12/11/chromium-updater-updated/">simple apps</a> for myself in the past, I wanted to build a simple utility and put it out there for other folks to use. My background for Mac OS X apps is zero, although I have walked through a hello world tutorial for iOS.</p>
<p>I started out by signing up for the <a href="http://developer.apple.com/">Apple developer license</a> (free), downloaded the latest Xcode (3.2.5) build, and dropped $99 bucks on gaining access to sell through the Mac store. I'm pretty sure that fee covers distributing apps through iOS for the iPhone, iPod, and iPad as well. If you're just interested in trying out the build tools or building for yourself and distributing your software through other means (go github!) you can skip the fee.</p>
<p><i>Docs</i></p>
<p>There's plenty of documentation available at the Mac Dev Center, but I found <a href="http://developer.apple.com/library/mac/#featuredarticles/UsingMacRuby/">Using MacRuby</a> particularly helpful for my app plans. A solid foundation for Mac apps is discussed in the <a href="http://developer.apple.com/library/mac/#documentation/Cocoa/Conceptual/ObjCTutorial/01Introduction/01Introduction.html">introduction to cocoa tutorial</a>, or if you prefer you can grab the <a href="http://developer.apple.com/library/mac/documentation/Cocoa/Conceptual/ObjCTutorial/ObjCTutorial.pdf">pdf</a> of the same documentation. Thus far the most helpful docs in understanding how to connect view (the user interface) to the controller/models are <a href="http://developer.apple.com/library/mac/documentation/Cocoa/Conceptual/ObjCTutorial/05View/05View.html#/">Defining the view</a> which cover Next Interface Build (nib) files, and <a href="http://developer.apple.com/library/mac/#documentation/Cocoa/Conceptual/ObjCTutorial/06Controller/06Controller.html#/">Bridging the model and view</a>.  Even though the latter doc is focused on objective c implementation it covers how any Cocoa view is glued to model functionality through a controller (actions, outlets, etc).</p>
<p>Here's a peak at the alpha interface for KeyBinder:<br />
<a href="http://www.victusspiritus.com/wp-content/uploads/2011/02/keybinder.png"><img src="http://www.victusspiritus.com/wp-content/uploads/2011/02/keybinder.png" alt="" title="keybinder" width="536" height="442" class="aligncenter size-full wp-image-7282" /></a></p>
<p>What I'm planning for the app is straight forward (setting keybindings), and in follow on posts I'll describe how I build out the interface into a visual control system for keybinds. It's fine by me if other folks build similar apps, my main goal is understanding how Mac apps are constructed and deployed to the App Store.</p>
