---
layout: post
status: publish
published: true
title: Practical Web Programming with the friendfeed API & Google App Engine
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
excerpt: "<object classid=\"clsid:d27cdb6e-ae6d-11cf-96b8-444553540000\" width=\"480\"
  height=\"385\" codebase=\"http://download.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=6,0,40,0\"><param
  name=\"allowFullScreen\" value=\"true\" /><param name=\"allowscriptaccess\" value=\"always\"
  /><param name=\"src\" value=\"http://www.youtube.com/v/_MNyvs08x2U&amp;hl=en&amp;fs=1&amp;color1=0x006699&amp;color2=0x54abd6\"
  /><param name=\"allowfullscreen\" value=\"true\" /><embed type=\"application/x-shockwave-flash\"
  width=\"480\" height=\"385\" src=\"http://www.youtube.com/v/_MNyvs08x2U&amp;hl=en&amp;fs=1&amp;color1=0x006699&amp;color2=0x54abd6\"
  allowscriptaccess=\"always\" allowfullscreen=\"true\"></embed></object>\r\n<h2>Long
  Day Coding</h2>\r\nHad a helluva weird 17 hour coding spree yesterday. By setting
  up and slightly modifying the friendfeed application example, I nearly drove one
  of the super helpful friendfeed developers bonkers (yeah I'm that bad with questions).
  The plus side, I have a basic handle on the Google App Engine (GAE), Python, Django
  html scripting and jury rigging eclipse projects to run php (why oh why doesn't
  GAE support PHP)."
wordpress_id: 1159
wordpress_url: http://www.victusspiritus.com/?p=1159
date: '2009-07-24 12:25:02 -0400'
date_gmt: '2009-07-24 19:25:02 -0400'
categories:
- Uncategorized
tags:
- startups
- coding
- google
- google appengine
- design
comments:
- id: 259
  author: Vladimir Vukicevic
  author_email: None
  author_url: http://twitter.com/Vukicevic
  date: '2009-07-24 14:53:12 -0400'
  date_gmt: '2009-07-24 19:53:12 -0400'
  content: Wow. 17 hours is impressive. I&#39;m quite sure the hard work will be worth
    it - at least from the learning perspective, but beyond as well.
- id: 260
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2009-07-24 14:54:21 -0400'
  date_gmt: '2009-07-24 19:54:21 -0400'
  content: I blame the rain, I usually only have 3-4 hours tops a night but the stars
    aligned yesterday.
- id: 1308
  author: 14 million ways to skin a cat &#8211; web programming
  author_email: ''
  author_url: http://www.victusspiritus.com/2009/10/28/14-million-ways-to-skin-a-cat-web-programming/
  date: '2009-10-28 04:43:33 -0400'
  date_gmt: '2009-10-28 11:43:33 -0400'
  content: "[...] Practical Web Programming with the friendfeed API &amp; Google App
    Engine (victusspiritus.com) [...]"
- id: 2168
  author: Vladimir Vukicevic
  author_email: vuki777@gmail.com
  author_url: http://vukicevic.blogspot.com/
  date: '2009-07-24 20:53:12 -0400'
  date_gmt: '2009-07-25 01:53:12 -0400'
  content: Wow. 17 hours is impressive. I&#39;m quite sure the hard work will be worth
    it - at least from the learning perspective, but beyond as well.
- id: 2169
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2009-07-24 20:54:21 -0400'
  date_gmt: '2009-07-25 01:54:21 -0400'
  content: I blame the rain, I usually only have 3-4 hours tops a night but the stars
    aligned yesterday.
---
<p><object classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" width="480" height="385" codebase="http://download.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=6,0,40,0"><param name="allowFullScreen" value="true" /><param name="allowscriptaccess" value="always" /><param name="src" value="http://www.youtube.com/v/_MNyvs08x2U&amp;hl=en&amp;fs=1&amp;color1=0x006699&amp;color2=0x54abd6" /><param name="allowfullscreen" value="true" /><embed type="application/x-shockwave-flash" width="480" height="385" src="http://www.youtube.com/v/_MNyvs08x2U&amp;hl=en&amp;fs=1&amp;color1=0x006699&amp;color2=0x54abd6" allowscriptaccess="always" allowfullscreen="true"></embed></object></p>
<h2>Long Day Coding</h2>
<p>Had a helluva weird 17 hour coding spree yesterday. By setting up and slightly modifying the friendfeed application example, I nearly drove one of the super helpful friendfeed developers bonkers (yeah I'm that bad with questions). The plus side, I have a basic handle on the Google App Engine (GAE), Python, Django html scripting and jury rigging eclipse projects to run php (why oh why doesn't GAE support PHP).<a id="more"></a><a id="more-1159"></a></p>
<h2>Friendfeed Developers Rock</h2>
<p>First off a big thanks to <a href="http://friendfeed.com/bgolub">Benjamin Golub</a> of <a href="http://friendfeed.com/">friendfeed</a> for his patience yesterday. I owe you a debt of gratitude for supporting non-friendfeed related code. A tip of the hat to all the friendfeed development staff who went out of their way (<a href="http://friendfeed.com/bret">Bret Taylor</a>, <a href="http://friendfeed.com/gburd">Gary Burd</a>) the last couple of days to get eager developers using their new API.</p>
<p>The GAE is definitely worth learning, if Google is going to continue to support it. It's basically free scalable hosting for your project (with some limitations) and you only pay for bandwidth plus storage needs over the free threshold (~5million pageviews a month). It was rolled out last year with Python support. Just recently they released java support, which enabled <a href="http://brian.brispace.net/2009/04/09/php-on-google-app-engine/">Quercus/PHP</a> to work. Incidentally <a href="http://www.caucho.com/resin-3.0/quercus/">Quercus</a> is much faster than normal php, but I do have an issue (hopefully something I can fix on my end).</p>
<p>The command line has become my friend, as I can't seem to get a project in either Eclipse or Netbeans to play nice with all the web programming languages I'm using. I guess that's good news for when I delve back into scala /lift using maven's command build.</p>
<p>As powerful as some of these technologies are, I can't help but feel that there's no one trying to unify all these web languages into an easy to start/build/deploy package. Beyond the Integrated Development Environment I wrote about previously, there is a need for language developers to see outside of their own "walled garden" of development. It's in our collective best interest to seamlessly bring these languages together into high level packages. The java virtual machine has been leveraged to produce byte code for several languages and is a good example of the direction we can head down. The cost to using the JVM is that specifically optimized local hardware compiled code can still outperform java for processing heavy apps.</p>
<p>It's fascinating looking back at the evolution of programming, from assembly to high level web application environments. We are continually inventing new ways to organize our ideas into formats that computers and the Internet can understand. There's still something to be desired in the experience of first learning new programming syntax. Without stretching my imagination too far, I envision a virtual programming assistant (VPA) tool that aids beginners and masters alike. The huge inefficiency in the design and learning of interfaces will be surprisingly expedient, as the VPA will handle most of the low level work. For star wars fans think of a C3PO (minus the body) focused on programming languages and you'll have a good concept of the functionality of a VPA.</p>
<p>I look forward to the day we can finally say farewell to QWERTY, an inefficient vestigial throwback. The interface to the web and it's windows will shift from mouse and keyboard to voice, optical and neural controls. Simulators and designers will have vast resources at their beck and call to create all manner of inventions.</p>
<h6 class="zemanta-related-title" style="font-size: 1em;">Related articles by Zemanta</h6>
<ul class="zemanta-article-ul">
<li class="zemanta-article-ul-li"><a href="http://themindstorms.blogspot.com/2009/03/java-on-google-app-engine-techcrunch.html">Java on Google App Engine? Some Speculating, But There May Be Some Truth</a> (themindstorms.blogspot.com)</li>
<li class="zemanta-article-ul-li"><a href="http://www.slumpedoverkeyboarddead.com/2009/05/15/grails-and-scala-support-googles-appengine/"> Grails and Scala support Googles AppEngine </a> (slumpedoverkeyboarddead.com)</li>
<li class="zemanta-article-ul-li"><a href="http://www.slideshare.net/sausheong/ruby-and-the-cloud"> Ruby And The Cloud </a> (slideshare.net)</li>
<li class="zemanta-article-ul-li"><a href="http://www.mehmetalierturk.com/2009/04/27/software-development-deployment-with-google-app-engine/"> Software Development &amp; Deployment with Google App Engine </a> (mehmetalierturk.com)</li>
</ul>
<div class="zemanta-pixie" style="margin-top: 10px; height: 15px;"><a class="zemanta-pixie-a" title="Reblog this post [with Zemanta]" href="http://reblog.zemanta.com/zemified/79289e71-492a-45ee-b0e6-c083702cb7bb/"><img class="zemanta-pixie-img" style="border: none; float: right;" src="http://img.zemanta.com/reblog_e.png?x-id=79289e71-492a-45ee-b0e6-c083702cb7bb" alt="Reblog this post [with Zemanta]" /></a><span class="zem-script more-related pretty-attribution"><script src="http://static.zemanta.com/readside/loader.js" type="text/javascript"></script></span></div>
