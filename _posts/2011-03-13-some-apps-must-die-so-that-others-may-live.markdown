---
layout: post
status: publish
published: true
title: Some apps must die, so that others may live
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 7635
wordpress_url: http://www.victusspiritus.com/?p=7635
date: '2011-03-13 04:56:31 -0400'
date_gmt: '2011-03-13 11:56:31 -0400'
categories:
- Uncategorized
tags:
- coding
- decision making
- design
comments: []
---
<p style="text-align: center;"><a href="http://listicles.com/media/10-illustrated-versions-of-evolution/"><img class="aligncenter size-full wp-image-7644" title="evolution" src="{{ site.url }}/assets/2011/03/evolution1.jpg" alt="" width="512" height="384" /></a></p>
<p>Do you like weekend web hacking projects? If like myself, you share a fondness for mid afternoon mini apps that automate and filter away some nagging pain point, you'll grow a backlog of tools rather quickly. The more apps you code, the greater the chance that one or more of them will fail due to any number of issues. Beyond failure, the apps may greatly benefit from changes to their architecture.</p>
<p>The following list details a number of reasons why apps may fail or deserve some refreshing, refactoring, or rearchitecting.</p>
<ol>
<li><b>Deployment/Hosting:</b> Are appengine jvm issues intolerable for your ruby apps, consider Heroku. Who has better deals and service slicehost, Engineyard or Rackspace? Amazon's Elastic Beanstalk is flexible but requires war file app deployment. Perhaps a host setting changed, or a new release is out</li>
<li><b>APIs</b> are moving targets. Versions, deprecation and no longer supported happen fast on the wild web</li>
<li><b>Language or DSL updates:</b> You're running 1.0.1 but you want to add or refactor a sweet feature from 1.1</li>
<li><b>Framework updates:</b> the framework you built 3 of your favorite hacks in has upgraded 63 times since you last revisited it. Do you make the plunge and adopt all the bug fixes and speedups (or slowdowns) into your apps. This alone tempts me to consider rolling my own code even when other tools exist, just to avoid incompatibility issues down the road</li>
<li><b>Server replacement:</b> Your models and database are spot on but your server always felt like bolt on asynchronous (event machine/tornado), should you make the switch to node.js</li>
<li><b>Front end replacement:</b> You built up your front end with MOO tools but want to swap to jQuery. Your templating engine is slow and painful, gut it and replace it with one of a million others.</li>
<li><b>Database upgrades or Replacement:</b> Should you update your query language or data layer to a faster more capable backend? What about swapping out the database for a completely different persistence layer that may be a better fit (flavors of nosql vs SQL)</li>
</ol>
<p>As you can see there are plenty of reasons why your apps may fail or deserve an overhaul. But the decision to maintain many apps is not to be taken lightly. Each weekend+ hack you choose to upkeep will take a toll on your ability to construct new applications. In a shiny world of rainbows and unicorns (creepy) maintenance would be free, but you and I don't live there. Some apps must die, so that others may live.</p>
