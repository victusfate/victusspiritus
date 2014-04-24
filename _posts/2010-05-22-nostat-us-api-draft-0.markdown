---
layout: post
status: publish
published: true
title: Nostat.us API draft 0
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 3946
wordpress_url: http://www.victusspiritus.com/?p=3946
date: '2010-05-22 08:17:08 -0400'
date_gmt: '2010-05-22 15:17:08 -0400'
categories:
- Uncategorized
tags:
- social web
- victus media
- nostatus
comments:
- id: 4391
  author: Leland
  author_email: leland@pickple.com
  author_url: ''
  date: '2010-05-24 02:30:27 -0400'
  date_gmt: '2010-05-24 07:30:27 -0400'
  content: Thanks for the javascript example Mark. This is super cool and I wonder
    how long it&#39;s going to take for other devs to see how much potential a service
    like this has in the new social web. :)
---
<p><a href="http://nostat.us">Nostat.us</a> is a message first service, where communication is king.</p>
<p>Today I'm taking a crack at documenting a brief api for Nostat.us, <a href="http://victusmedia.com">Victus Media's</a> simple group messaging service. I expect there may be some changes and iterating while we home in on a solid framework. The first steps are important, and we've opted to expose as much of the process as possible while releasing an interesting alternative to other social web options. The examples shown are JavaScript access but any favorite web programming language will do.</p>
<p>authenticate</p>
<p>http://nostat.us/checkpassword/(user)/(password)</p>
<p>send message<br />
$.post("/sendmessage/"+user+"/"+escape(message), function(data){ alert(data.status); window.location.reload();  });</p>
<p>follow user</p>
<p>send message to group<br />
$.post("/sendmessage/"+user+"/"+escape("group:"+group+" "+message));</p>
<p>add subscription to group<br />
$.post("/addsubscription/"+user+"/"+subscription);</p>
<p>Here's an example of <a href="http://pastebin.com/4efsVimH">javascript accessing the Nostat.us api</a> which is active on the Nostat.us site.</p>
<p>Any questions, concerns, or corrections? Don't hesitate to contact us (messel at victusmedia dot com).</p>
