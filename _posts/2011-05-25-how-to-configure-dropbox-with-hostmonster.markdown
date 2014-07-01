---
layout: post
status: publish
published: true
title: How to Configure Dropbox with Hostmonster
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9035
wordpress_url: http://www.victusspiritus.com/?p=9035
date: '2011-05-25 04:21:17 -0400'
date_gmt: '2011-05-25 11:21:17 -0400'
categories:
- Uncategorized
tags:
- dropbox
- cloud
comments: []
---
<table>
<tr>
<td>
<a href="http://www.dropbox.com"><img src="{{ site.url }}/assets/2011/05/DropBox_images-300x101.jpg" alt="" title="DropBox_images" width="300" height="101" class="aligncenter size-medium wp-image-9037" /></a>
</td>
<td>
<a href="http://www.hostmonster.com"><img src="{{ site.url }}/assets/2011/05/Hostmonster.jpg" alt="" title="Hostmonster" width="300" height="157" class="aligncenter size-full wp-image-9051" /></a>
</td>
</tr>
</table>
<h2>How to guide</h2>
<p>First thing you'll need to do is get <a href="https://my.hostmonster.com/cgi/help/180?step=180">SSH access</a> to Hostmonster or your favorite Linux host. </p>
<p>From <a href="http://wiki.dropbox.com/TipsAndTricks/TextBasedLinuxInstall">dropbox</a>:</p>
<div class="gist-file">
<blockquote><p>
<strong>Step-by-step version</strong></p>
<p>Log in to your Linux server so you obtain a shell prompt, and change to your home directory.<br />
cd<br />
a. Stable 32-bit: (<em>I installed the 32bit version, Hostmonster's default account</em>)</p>
<pre>
wget -O dropbox.tar.gz "http://www.dropbox.com/download/?plat=lnx.x86"   
</pre>
<p>Stable 64-bit: </p>
<pre>
wget -O dropbox.tar.gz "http://www.dropbox.com/download/?plat=lnx.x86_64"   
</pre>
<p>Sanity check to make sure we're not going to clog our home directory.</p>
<pre>
tar -tzf dropbox.tar.gz   
</pre>
<p>Extract</p>
<pre>
tar -xvzf dropbox.tar.gz
</pre>
<p>Make sure the LANG environment variable is set to something other than NULL, e.g. en_US.iso88591.<br />
If it is NULL, you'll get a cryptic error. (mine was NULL and it worked)</p>
<p>Run dropboxd:</p>
<pre>
~/.dropbox-dist/dropboxd   
</pre>
<p>You should see output like this:<br />
This client is not linked to any account... Please visit </p>
<p>https://www.dropbox.com/cli_link?host_id=7d44a557aa58f285f2da0x67334d02c1 to link this machine.<br />
Dropbox will create a ~/Dropbox folder and start synchronizing it after this step!<br />
Go to the URL given; you should see a success message at the top of your screen.
</p></blockquote>
</div>
<p>From <a href="http://www.fuzedbulb.com/">FuzedBulb's</a> comment on <a href="http://forums.dropbox.com/profile.php?id=1228117">dropbox's forum</a>:</p>
<blockquote><p>
If you've the text based ".dropbox-distro" folder with you, you can try doing:</p>
<pre>
$ nohup ./.dropbox-dist/dropboxd &
</pre>
<p>If HostMonster doesn't disallow background tasks, this will keep the daemon running in the background even when you have logged out from shell.
</p></blockquote>
<p>After this I symbolic linked my public directory under public_html. </p>
<pre>
cd to public_html
ln -s ~/Dropbox/Public DropboxPublic
</pre>
<p>It's still copying information over but the dropbox daemon did stop at one point. I'll have to look into what may have caused it, any suggestions appreciated.</p>
