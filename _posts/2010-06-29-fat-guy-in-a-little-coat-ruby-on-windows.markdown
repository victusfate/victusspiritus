---
layout: post
status: publish
published: true
title: Fat Guy in a little coat, Ruby on Windows
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 4337
wordpress_url: http://www.victusspiritus.com/?p=4337
date: '2010-06-29 05:24:57 -0400'
date_gmt: '2010-06-29 12:24:57 -0400'
categories:
- Uncategorized
tags:
- software
- coding
- ruby
comments:
- id: 4648
  author: eli
  author_email: eli_sacks@hotmail.com
  author_url: ''
  date: '2010-06-29 22:34:23 -0400'
  date_gmt: '2010-06-30 03:34:23 -0400'
  content: Is a gem just a library?
- id: 4649
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-06-29 22:43:30 -0400'
  date_gmt: '2010-06-30 03:43:30 -0400'
  content: Much like a very focused packaged object, that grabs any dependencies if
    needed
- id: 4729
  author: Scott Anderson
  author_email: sanderson7@gmail.com
  author_url: http://geeksharp.com
  date: '2010-07-09 14:43:57 -0400'
  date_gmt: '2010-07-09 19:43:57 -0400'
  content: Glad my little blog could be of help to you.  Cheers! :)
- id: 10106
  author: Don&#8217;t you think she looks tired &mdash; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2011/06/07/dont-you-think-she-looks-tired/
  date: '2011-06-07 07:32:30 -0400'
  date_gmt: '2011-06-07 14:32:30 -0400'
  content: "[...] the same time I was running into web dev woes with Windows&#8217;
    sad support of Ruby, Python, git, browsers and pretty much anything related to
    web, open source, or [...]"
---
<p style="text-align: center;"><object classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" width="480" height="385" codebase="http://download.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=6,0,40,0"><param name="allowFullScreen" value="true" /><param name="allowscriptaccess" value="always" /><param name="src" value="http://www.youtube.com/v/oGWbt3DSje0&amp;hl=en_US&amp;fs=1&amp;" /><param name="allowfullscreen" value="true" /><embed type="application/x-shockwave-flash" width="480" height="385" src="http://www.youtube.com/v/oGWbt3DSje0&amp;hl=en_US&amp;fs=1&amp;" allowscriptaccess="always" allowfullscreen="true"></embed></object><em>There's just too much awesome in Ruby for a clean windows install and development environment.<br />
</em></p>
<p>Just yesterday I started laying the pavement for using Ruby at work. I didn't want to cough up a few hundred for a dev license of <a href="http://www.sapphiresteel.com/Products/Ruby-In-Steel/Ruby-In-Steel-Developer-Overview">Ruby In Steel</a>, a slick Visual Studio plugin.  My first instinct was to dual boot a flavor of linux. Ubuntu's not cleared for work, but Centos (&amp; Redhat) are. The Centos install will have to wait until I torrent the DVD at home later this week (internet at work is low bandwidth). Alternatively, I can go with VirtualBox and emulate my way to happiness.</p>
<p>I remember first setting up Ruby at home on my then Vista system and groaning over failed native gem builds which finally prompted me to jump to Ubuntu (<a href="http://www.victusspiritus.com/2010/01/31/cutting-ties-with-my-old-friend-microsoft/">among many other issues</a>). Going through the usual hoops, JDK, Netbeans for an IDE, Ruby one click installer everything went smoothly. Then I hit a road block:</p>
<p style="padding-left: 30px;">gem install json</p>
<p>ERROR:  http://gems.rubyforge.org/ does not appear to be a repository<br />
ERROR:  could not find gem json locally or in a repository</p>
<p>It couldn't find the json gem (or any others).</p>
<p>Turns out I'm behind a universal proxy, thanks to Google search and <a href="http://stackoverflow.com/questions/2238340/how-can-i-get-past-http-gems-rubyforge-org-does-not-appear-to-be-a-repository/2238383#2238383">stack overflow</a> for clearing up my issue.</p>
<div>
<blockquote><p>Your browser might be using system-wide proxy  settings or some sort of automatic configuration. The gem command  probably doesn't. I'm behind an university proxy and I can't  install/update any gems normally, but can access everything with my  browser. To install gems, I normally create a tunnel to my server so I  can bypass the proxy server.</p>
<p>This might help you to configure the proxy settings for the gem  command: <a href="http://stackoverflow.com/questions/4418/how-do-i-update-ruby-gems-from-behind-a-proxy-isa-ntlm">http://stackoverflow.com/questions/4418/how-do-i-update-ruby-gems-from-behind-a-proxy-isa-ntlm</a></p></blockquote>
</div>
<p>Here's the fix in a comment under that answer:<br />
gem install --http-proxy http://proxyserveraddress:proxyport _name_of_gem_</p>
<h2>Native Gems</h2>
<p>Now what I'm really concerned about is building native gems on windows and debugging what goes wrong. Most native C gems leverage gcc on Linux (<a href="http://packages.debian.org/sid/build-essential">and lots of other stuff)</a>. There's a mingw port of gcc for windows, and there's also cygwin, but I'm leery of trusting either of these alternatives to work flawlessly. Luckily Scott Anderson posted a useful trick for debugging native extensions at <a href="http://geeksharp.com/2010/01/18/windows-ruby-native-gems-1-9-1/">Geeksharp.com</a> (thanks Scott). You gotta love the ability of hackers to figure something out, and share it with the world rapidly.</p>
<p>I'll update my progress and experiences with Ruby on Windows over the next couple of weeks.</p>
