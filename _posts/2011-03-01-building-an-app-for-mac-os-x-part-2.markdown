---
layout: post
status: publish
published: true
title: Building an App for Mac OS X Part 2
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 7474
wordpress_url: http://www.victusspiritus.com/?p=7474
date: '2011-03-01 07:36:11 -0500'
date_gmt: '2011-03-01 14:36:11 -0500'
categories:
- Uncategorized
tags:
- coding
- apple
- ruby
- mac os x
- apps
comments: []
---
<p>This is a continuation of my exploration of developing a Mac OS X application, particularly a MacRuby app which has been designed well with deep integration into Cocoa objects implemented in objective C. The series is now two posts strong :)</p>
<ul>
<li><a href="http://www.victusspiritus.com/2011/02/16/building-an-app-for-mac-os-x-part-1/">Building an App for Mac OS X part 1</a></li>
<li>... (I suspect I can craft something presentable in less than 10 posts)</li>
</ul>
<p>The Cocoa framework is designed around a MVC architecture to aid in maintenance and reuse of applications. While I can respect the design decision, I'm confident I can get away with the VC framework for my first MacApp by embedding model data and methods within a controller. One of the major hurdles I had during my first sitting was figuring out how to bind GUI events to source code actions. </p>
<p>No matter what I tried I couldn't get the Controller object to show up on the list of available choices for any NSObjects I added to the graphical view builder (xib). While flying yesterday in my sardine can seat I managed to glean some insight from a few tutorials about developing for the mac (<a href="http://developer.apple.com/library/mac/#documentation/Cocoa/Conceptual/ObjCTutorial/05View/05View.html">1</a>,<a href="http://www.macruby.org/documentation/tutorial.html">2</a>, <a href="http://www.instapaper.com/folder/558214/rss/419835/4zvNFfgw07bdO7xB3CN7QidITk">feed of all my favorite mac docs</a>). </p>
<p>The first problem was solved by declaring the controller as a subclass of NSWindowController. I'm sure there are a variety of controller types I can inherit from depending on the project. But for now I'm going to follow the primordial law of nature KISS (keep it simple stupid), often conflated with Occam's Razor, after all it got me this far.</p>
<p><script src="https://gist.github.com/849150.js"> </script></p>
<p>After that step the Controller class showed up in the in xib drop down interface for NSObjects. I was able to control click from the button view element to the Controller and setup a selector which sends an action (event) to the Controller from the view element (button clicked). I did the same for a text field which I initialized with the basic KeyBindings that provided the motivation for this app. Here's what the xib file interface looks like. The top left window is the .xib wiring and element list. The bottom left is the graphical view builder. The right two frames are the inspector (shows connections) and the Library (for adding objects/classes).<br />
<a href="http://www.victusspiritus.com/wp-content/uploads/2011/03/mac_xcode_xib.png"><img src="http://www.victusspiritus.com/wp-content/uploads/2011/03/mac_xcode_xib.png" alt="" title="mac_xcode_xib" width="500" height="326" class="aligncenter size-full wp-image-7480" /></a></p>
<p>For the next post in the series I'd like to hunt down a satisfactory graphical representation of a Mac and Standard keyboard. My goal is to hook up all the key bindings to button presses, and persist those changes to disk. If something goes wrong there'll be a default button which will rename the .dict file to a backup allowing clients to safely return to default settings.</p>
<p>There's a good chance I'll port the app over to <a href="http://www.macruby.org/trac/wiki/HotCocoa">HotCocoa</a> if for no other reason than to understand the DSL. I'll do so after I get to a point where I'm satisfied with cursory knowledge of Cocoa's API. Depending on HotCocoa's maturity and ability to deploy to the Mac AppStore, I'll decide later whether it's adequate to satiate my app building interests. </p>
