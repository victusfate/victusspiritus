---
layout: post
status: publish
published: true
title: Chromium Updater Updated
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 6207
wordpress_url: http://www.victusspiritus.com/?p=6207
date: '2010-12-11 06:11:06 -0500'
date_gmt: '2010-12-11 13:11:06 -0500'
categories:
- Uncategorized
tags:
- Chrome
- coding
- apple
- mac os x
- chromium
comments:
- id: 8967
  author: Building an App for Mac OS X Part 1 &raquo; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2011/02/16/building-an-app-for-mac-os-x-part-1/
  date: '2011-02-16 05:41:21 -0500'
  date_gmt: '2011-02-16 12:41:21 -0500'
  content: "[...] to create my first Mac store app after some encouragement from my
    wife. While I&#8217;ve created simple apps for myself in the past, I wanted to
    build a simple utility and put it out there for other folks to [...]"
- id: 9677
  author: Setting up Redis.app on Mac OS X &raquo; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2011/03/26/setting-up-redis-app-on-mac-os-x/
  date: '2011-03-26 04:24:12 -0400'
  date_gmt: '2011-03-26 11:24:12 -0400'
  content: "[...] first turned to the appify script I used late last year. Unfortunately
    the script (see chromium updater updated) no longer converted bash shell scripts
    in running .app files. They&#8217;d convert but fail to [...]"
---
<p><a href="http://commons.wikimedia.org/wiki/File:Chromium_Icon.png"><img src="http://www.victusspiritus.com/wp-content/uploads/2010/12/20090607050356Chromium_Icon.png" alt="" title="20090607050356!Chromium_Icon" width="512" height="512" class="aligncenter size-full wp-image-6212" /></a><br />
This morning I determined it was a good time to check for a new release and build for chromium. Low and behold my handy ChromiumUpdater from an old TechCrunch post or a zipped dmg failed to function. I went back to the post via a LifeHacker mention but the script was gone. It was time I dig in a little and find out precisely what the application was doing to see where it was going wrong. After all, how hard could remaking a little copy and install script be?</p>
<p>After a quick search I found a couple of helpful posts. One by <a href="http://www.shad.cc/post/2010/01/How-to-auto-update-Chromium-on-Mac-OS-X,-Linux-and-other">shad</a> to give me the basis for my shell script. The next step was to convert the shell script into a one click desktop application. I called the shell script directly from <a href="http://www.cyberciti.biz/faq/mac-osx-applescript-run-shell-script/">AppleScript</a> since the appify method was no longer supported.</p>
<blockquote>
<div class="gist-file">
<pre>
do shell script "/path/to/yourscript.sh"
</pre>
</div>
</blockquote>
<p><del>I was in luck <a href="http://subtlegradient.com/">Thomas Aylott's</a> handy <a href="https://gist.github.com/672684">appify script</a> and <a href="http://mathiasbynens.be/notes/shell-script-mac-apps">Mathias Bynen's post</a> helped make that happen.</del></p>
<p>After walking through the script line by line, it turns out the snapshot location and directory structure was changed by the chromium project folks. Luckily they left a nice href in the curl (classy chromium folks) to the old location which my earlier script was deleting. Here's a function script and gist:<br />
<script src="https://gist.github.com/737362.js"> </script></p>
<p>Once you have the script working you can convert it to a Mac OS X desktop application with appify (presumed now to be installed in your path):</p>
<pre>
cat ChromiumUpdater.sh | appify ChromiumUpdater
</pre>
