---
layout: post
status: publish
published: true
title: Setting up Redis.app on Mac OS X
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8084
wordpress_url: http://www.victusspiritus.com/?p=8084
date: '2011-03-26 04:23:57 -0400'
date_gmt: '2011-03-26 11:23:57 -0400'
categories:
- Uncategorized
tags:
- mac os x
comments: []
---
<p>I've been spoiled by <a href="http://www.couchbase.com/downloads">CouchBase</a> which comes with a prepackaged OS X app. It includes a sharp C logo, which sits nicely on my Dock bar (not to be confused with a dickbar*). The database server is ready to launch up with a click although I prefer the relaxing couch image of couchdbx.<br />
<a href="{{ site.url }}/assets/2011/03/CouchBase_icon.png"><img src="{{ site.url }}/assets/2011/03/CouchBase_icon.png" alt="" title="CouchBase_icon" width="63" height="72" class="aligncenter size-full wp-image-8085" /></a><br />
But while whipping through a <a href="http://camp.nodejs.org/">nodejs walkthrough</a>  which was homework for last year's Node.js Camp, I ran into a slight snag. Everything worked fine, but I wanted a Mac OS X clickable app to fire up redis with a Terminal log showing access. Below is the walkthrough homework:</p>
<div class="block homework">
<style type="text/css">
.block {<br />
  background-color: white;<br />
  color: #142833,<br />
  -webkit-border-radius: 7px;<br />
  -moz-border-radius: 7px;<br />
  border-radius: 7px;<br />
  border: 1px solid #e2ecf0;<br />
  padding: 20px;<br />
  margin-bottom: 20px;<br />
}<br />
.block p, .block ul, .block h3, .block h2 {<br />
  padding-bottom: 10px;<br />
}<br />
.block p {<br />
  padding-left: 25px;<br />
}</p>
</style>
<h2>Node.js Camp Homework: How to Get Ready</h2>
<h3>1. Install Node on your laptop.</h3>
<p><a href="http://joyeur.com/2010/12/10/installing-node-and-npm/">Instructions here.</a></p>
<p>Pick one of the install methods <a href="https://gist.github.com/579814">in this gist.</a></p>
<h3>2. Explore creationix's Game Code</h3>
<p><code>npm install connect socket.io</code></p>
<p><a href="https://github.com/joyent/node-camp/tree/master/hexes">Attempt to run it locally.</a></p>
<h3>3. Get WebOS emulator running on your laptop</h3>
<p><a href="https://github.com/joyent/node-camp/blob/master/nodeFor145.markdown">Instructions here.</a></p>
<h3>4. Install node-redis and redis</h3>
<p><code># start the redis server<br><br />
              wget http://redis.googlecode.com/files/redis-2.0.4.tar.gz<br><br />
              tar -zxf redis-2.0.4.tar.gz<br><br />
              cd redis-2.0.4<br><br />
              make<br><br />
              ./redis-server<br><br />
              # install the node library:<br><br />
              npm install redis hiredis<br />
          </code></p>
</p></div>
<p>I first turned to the appify script I used late last year. Unfortunately the script (<a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/12/11/chromium-updater-updated/">see chromium updater updated</a>) no longer converted bash shell scripts in running .app files. They'd convert but fail to execute, raising an error based on an incompatible OS version. Luckily a little web browsing revealed the AppleScript Editor (path /Applications/Utilities/AppleScript Editor.app) which can perform the leg work of converting a shell script into an app by saving as an Application.<br />
The code:<br />
<code><br />
set the_shell_script to "echo $PATH"<br />
tell application "Terminal"<br />
	activate<br />
	do script "/Users/messel/Desktop/Dropbox/scripts/redis-2.0.4/redis-server"<br />
end tell<br />
</code><br />
The AppleScript Editor:<br />
<a href="{{ site.url }}/assets/2011/03/AppleScript_Editor.png"><img src="{{ site.url }}/assets/2011/03/AppleScript_Editor.png" alt="" title="AppleScript_Editor" width="500" height="330" class="aligncenter size-full wp-image-8102" /></a></p>
<p>I've included a few 512x512.png (os x app icon size) logos that I modified. The background of the official one wasn't legible on the dock bar:<br />
<a href="{{ site.url }}/assets/2011/03/redis_logo_full_grey.png"><img src="{{ site.url }}/assets/2011/03/redis_logo_full_grey.png" alt="" title="redis_logo_full_grey" width="512" height="512" class="aligncenter size-full wp-image-8096" /></a></p>
<p><a href="{{ site.url }}/assets/2011/03/redis_logo_full_didot_bolt.png"><img src="{{ site.url }}/assets/2011/03/redis_logo_full_didot_bolt.png" alt="" title="redis_logo_full_didot_bolt" width="512" height="512" class="aligncenter size-full wp-image-8100" /></a></p>
<p><a href="{{ site.url }}/assets/2011/03/redis_logo_full_rain.png"><img src="{{ site.url }}/assets/2011/03/redis_logo_full_rain.png" alt="" title="redis_logo_full_rain" width="512" height="512" class="aligncenter size-full wp-image-8097" /></a><br />
The original wasn't legible on the docking bar:<br />
<a href="{{ site.url }}/assets/2011/03/redis_logo_full.png"><img src="{{ site.url }}/assets/2011/03/redis_logo_full.png" alt="" title="redis_logo_full" width="512" height="512" class="aligncenter size-full wp-image-8098" /></a><br />
Notes:<br />
* = the dickbar is community nickname for the twitter trending banner where paid advertisements go, named after Twitter CEO Dick Costolo.</p>
