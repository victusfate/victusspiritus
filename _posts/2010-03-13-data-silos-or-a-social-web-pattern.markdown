---
layout: post
status: publish
published: true
title: Data Silos or a Social Web Pattern
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 3287
wordpress_url: http://www.victusspiritus.com/?p=3287
date: '2010-03-13 06:35:31 -0500'
date_gmt: '2010-03-13 13:35:31 -0500'
categories:
- Uncategorized
tags:
- social web
- social design
- open design
- design
comments:
- id: 3325
  author: Dave Pinsen
  author_email: impossibledistances@yahoo.com
  author_url: http://steamcatapult.com/
  date: '2010-03-14 06:13:09 -0400'
  date_gmt: '2010-03-14 11:13:09 -0400'
  content: Never apologize for a short post, Mark. Some of the best things written
    have been relatively short.
- id: 3328
  author: Tyler from Everyone Loves Tea
  author_email: tjgillies@gmail.com
  author_url: http://www.everyonelovestea.com
  date: '2010-03-14 09:04:08 -0400'
  date_gmt: '2010-03-14 14:04:08 -0400'
  content: Great post as always. I dig the picture
- id: 3331
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-03-14 16:09:49 -0400'
  date_gmt: '2010-03-14 21:09:49 -0400'
  content: You got me restarted on this whole distributed web, open data/standards
    kick. I had pushed it out of my head for a time while learning how to introduce
    spooky bugs into web apps :)
- id: 3332
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-03-14 16:06:59 -0400'
  date_gmt: '2010-03-14 21:06:59 -0400'
  content: Sure thing, it just felt a little flat after rereading it. I enjoy digging
    in with at least some effort to learn, document, and gather links to related info/people
- id: 3334
  author: Tyler from Everyone Loves Tea
  author_email: tjgillies@gmail.com
  author_url: http://www.everyonelovestea.com
  date: '2010-03-14 16:45:53 -0400'
  date_gmt: '2010-03-14 21:45:53 -0400'
  content: It&#39;s where the world is going, so why not get there first?
- id: 3335
  author: Dave Pinsen
  author_email: impossibledistances@yahoo.com
  author_url: http://steamcatapult.com/
  date: '2010-03-14 16:46:32 -0400'
  date_gmt: '2010-03-14 21:46:32 -0400'
  content: I&#39;ve gotten that flat feeling before. Know what you mean.
- id: 4329
  author: Personal Social Gardens that Live in the Browser
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/05/16/personal-social-gardens-that-live-in-the-browser/
  date: '2010-05-16 08:20:40 -0400'
  date_gmt: '2010-05-16 15:20:40 -0400'
  content: "[...] Data Silos or a Social Web Pattern [...]"
---
<p><a href="http://bjay70.deviantart.com/art/Silo-Sunrise-HDR-138379561"><img class="alignnone size-full" src="{{ site.url }}/assets/2010/03/l_1280_640_FD2CF59F-9819-4BDF-B527-613F6A563E38.jpeg" alt="" /></a></p>
<p><em>Pardon the brevity of yesterday's post, my cylinders were running on a foggy four hours of sleep so I kept it short. This one has more heft :)</em></p>
<p>The biggest examples of social data silos today are Facebook and to a lesser extent Twitter. Social media platforms create business value from large user membership, attention, social link sharing, and the healthy ecosystems of apps that improve user and network value. While Facebook and Twitter support methods for exporting data, they have limited access and closed formats (I can't hack a new twitter API, their data is closed). Social silos write their own rules for how to access and potentially move their data. It's all good, they created the infrastructure and software, so why shouldn't they control the faucet to their data stores?</p>
<p>Savy users have known for a while that there's a data portable way of accomplishing nearly everything with a distributed open social web (<a href="http://groups.google.com/group/open-web-discuss/browse_thread/thread/288c846cc484a3c4">search is tricky</a>) . The hard part is <a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/03/08/open-web-protocols-and-discussion-groups/">setting standards</a> to enhance interoperability. The idea is to shape user social data so that it natively has the ability to migrate to any servers who support open standards. The standards provide a common language between (self hosted) social hubs. This natural extension of the net is becoming the defacto social web. With high likelihood Facebook, Twitter, and other portals will follow suit but not until they have to (distributed monetization takes some work). The social web has already lead to a diversity of social communities where users converse with folks on other networks without worrying about which service is most popular today (non roach motel/data silos). As technology advances, it approaches <a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/01/29/the-ideal-computer-converges-on-invisible/">invisible</a>. At any time users are free to walk away without losing links to friends or business contacts (speaking of which, its time I move my gmail and phone contacts into an open format I maintain and copy, and maybe my gmail data too).</p>
<p>If you think of Google as just another silo, you're partially right. I should be able to easily migrate my email from gmail (I haven't tried). And <a class="zem_slink" title="Orkut" rel="homepage" href="http://www.orkut.com">Orkut</a> is an older social network popular in Brazil isn't built on open standards, but <a href="http://www.google.com/buzz/dclinton/KuXDg9P8Q8z/Jesse-Stay-A-few-points-of-clarification-to-your">DeWitt Clinton</a> and his colleagues are working hard to make all our Buzz social data portable (many of the standards Buzz is built on are part of something we're working on at Victus Media, which I'll cover below).</p>
<h2>The Push/Pull of Streams &amp; Feeds</h2>
<p>There's a mad scientist cooking up something wonderful at Victus Media, and it's not me. Well I'm cooking up stuff too but it's not as awesome (front end, link tagging stuff). Tyler the chief Hacknical Wizard of VM, has concocted a master plan of great vision. I assisted in design, as we hashed the idea out Thursday, but the architecting is his responsibility. We decided we both want to move away from a limited service format (twitter tool) to a web service and we have a groovy way to do so.</p>
<p>To accomplish this while maintaining relevance is no small feat. An example of relevance lost from mixing social feeds is the @ symbol. In Twitter it maps directly to a user account, but that user may be someone else on Buzz (they use email as a unique identifier). Fortunate for us, semantic entities are service agnostic so we can link information and people among many services. Also certain services have dedicated functionality so we'll use a meta tag (bit string) to activate other functions on our side. One example is link scraping from microblogs and semantic tagging those urls. Another example is using oembed to show mini video clips from sites like YouTube. I believe <a href="http://www.disqus.com">Disqus</a> has implemented something like this in their comments. I'll try to convince Tyler to writeup a guest post on the push/pull architecture he's building (woman getting angry at my ignoring her). We may even open source the feed juggling if it makes sense.</p>
<h6 class="zemanta-related-title" style="font-size: 1em;">Related articles by Zemanta</h6>
<ul class="zemanta-article-ul">
<li class="zemanta-article-ul-li"><a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/03/09/the-user-service-bargain-social-web-services/">The User Service Bargain, Social Web Services</a> (victusspiritus.com)</li>
<li class="zemanta-article-ul-li"><a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/03/03/centralized-versus-distributed-web/">Centralized versus Distributed Web</a> (victusspiritus.com)</li>
</ul>

