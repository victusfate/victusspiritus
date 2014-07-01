---
layout: post
status: publish
published: true
title: 'Back in Action: iTunes is the only #fail for putting on Linux pants'
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 2917
wordpress_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/02/01/back-in-action-itunes-is-the-only-fail-for-putting-on-linux-pants/
date: '2010-02-01 05:48:57 -0500'
date_gmt: '2010-02-01 12:48:57 -0500'
categories:
- Uncategorized
tags:
- web/tech
- coding
comments:
- id: 2823
  author: RealMaverick
  author_email: reillyt@gmail.com
  author_url: http://wolfsongs.com
  date: '2010-02-02 04:30:03 -0500'
  date_gmt: '2010-02-02 09:30:03 -0500'
  content: Nice! I was talking at work about installing Linux on my computer. My biggest
    worry is that Mel will have a hard time with any distro I use. Also, we live off
    of iTunes with my iPod touch, so that is a big negative right there.
- id: 2824
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-02-02 09:12:02 -0500'
  date_gmt: '2010-02-02 14:12:02 -0500'
  content: I&#39;m working around the iTunes problem by researching how to use my
    phone more like a computer where *shock* I&#39;m allowed to admin/root priveleges.
    Too tied up at the moment and no driving need (Michelle got an iMac so I can use
    iTunes on her machine with my account).
---
<p>Yesterday evening I was back to nearly full functionality after leaving my old friend Windows. The surprising casualty of the switch from Windows to Ubuntu Linux is iTunes. Apple hasn't released a Linux client yet, as I suspect the unix to unix port to be a heavy burden (JFDI).</p>
<p>The largest troublemaker was getting my Logitech (MX518) mouse to function. I found a <a href="http://articles.rootsmith.ca/linux/logitech-mx-revolution-mouse-on-linux">helpful web guide</a> that lead me to edit xorg.conf and set some options (note: I didn't need to change the server layout file). After that I grabbed the following must have (for me) software: </p>
<ul>
<li>Google Chrome: preferred browser, email client, social media UI, backup blog platform</li>
<li>Java Runtime Environment/Java Developer Kit, (bundled with Netbeans): must have for eclipse or JVM languages (scala)</li>
<li>Adobe Flash</li>
<li>Ruby, Gem Installer, Rails, Apatana RadRails: our web development environment at Victus Media & my favorite IDE for ruby/rails, JavaScript or even php. Supporting installs, many gems, Mongrel, Sqlite, and dependencies</li>
<li>git: a promising software management tool</li>
<li>Dropbox: fantastic file sharing & syncronization</Li>
<li>VLC media player</li>
<li>WINE: an emulator for Windows. Have your cake and eat it? Tried making iTunes work with this but found additional tricks were needed to get it to connect to my iPhone. It could still come in handy for must have winOS software</li>
<li>VirtualBox: another virtual machine emulator, this one from Sun. I enjoyed Centos under my windows os, may install windows in VB to see how it runs</Li>
</ul>
<p>The installation of the software was done through command line:<br />
<i>sudo apt-get ApplicationName</i><br />
Or by using the Ubuntu package handler in the UI (under the applications tab).<br />
And the last installation method I used was clicking on .deb files. All methods worked equally well.</p>
<p>Installation was straight forward and setup didn't vary much from a windows experience. It wasn't quite as smooth as setting up Michelle's iMac (she did it all easily and is the bane of all computers). It wasn't substantially harder, although it was significantly less expensive.</p>
