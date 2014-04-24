---
layout: post
status: publish
published: true
title: Cheers, where everybody knows your name
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 4465
wordpress_url: http://www.victusspiritus.com/2010/07/09/cheers-where-everybody-knows-your-name/
date: '2010-07-09 07:31:49 -0400'
date_gmt: '2010-07-09 14:31:49 -0400'
categories:
- Uncategorized
tags:
- marketing
- web/tech
- design
comments: []
---
<h2>You Win When Visitors Memorize Your Domain</h2>
<p>How many domains do you know by memory?  For me this number may be higher than average, and I see every one of these domains as a brilliant success in web design. We type the domain into the browser because we recognize a specific function associated with a site. The site serves a clear purpose in our mind.</p>
<p>Memorized domains not only have us visiting regularly, but we're more likely to tell a friend about the site because we know it, and it solves a problem (good marketing). <a href="http://www.victusspiritus.com/2010/07/04/halt-the-pain-of-interface-flames/">Familiarity</a> has a cognitive effect where we're much more likely to return. </p>
<h2>Routes as Symbols</h2>
<p>If we're knowledgeable of a site's routing scheme it has even greater utility. Now no matter where we're browsing, we can leverage the web documents as a command line database to specific destinations. In addition the routes act as <a href="http://www.victusspiritus.com/2009/12/10/bread-crumb-navigation/">breadcrumbs</a> which enable rapid <i>up and down</i> route searching of web pages.</p>
<p>Essentially the routes act as symbols in our mind for surfacing detailed information. So in a moment I can bring up what far out topics I've written about: <a href="http://www.victusspiritus.com/tag/far-out">http://www.victusspiritus.com/tag/far-out</a>. In this case wordpress has a built in route for tags (post topics). Note how spaces are mapped into dashes or - in the URL. Alternatively I can revisit my startup posts <a href="http://www.victusspiritus.com/tag/startups">http://www.victusspiritus.com/tag/startups</a>. It's times like these where I wish I named my blog me.me ;). Tab completion for URL routes is already enabled in certain browsers which magnifies this utility. Powerful browsers can cache often visited sites, or have access to site maps.</p>
<h2>Cluttered Multi-Function Domains are Bad</h2>
<p>You're creating artificial marketing barriers if your domain is cluttered with too many products or utilities. While visitors are likely to commit a handful of swiss army knives to memory (Google, Facebook, Twitter) you're site has to start super focused and do one thing incredibly well before branching out. Personally, I prefer the ongoing dedication of Google's landing page to Twitter's information creep social portal. Facebook's user home page has become pretty terrifying but began much simpler. Visitors are less likely to commit a swiss army knife they aren't familiar with to memory. As designers we have to be able to answer: <i>What can our site offer better than the everyone else who matters?</I></p>
<h2>Thoughts about routes</h2>
<p>I've got a loose image of a handful of routes that if accepted would act as a proxy command line to the web. Routes are subject to how you wish to represent data to visitors and can just as easily be an API to other services. Just replace www.yourdomain with api.yourdomain and slap on a trailing extension (.XML,.atom, .json) to specify the data format. <a href="http://apiwiki.twitter.com/Twitter-API-Documentation">Twitter</a> has done a good job of implementing this and gave me the idea.</p>
<ul>
<li>
/users/user_name
</li>
<li>
/tag/tag_name
</li>
<li>
/object_type/object_name
</li>
<li>
/year/month/day/time?
</li>
<li>
/location/lla/lat/lon/alt/<br />
/location/xyz/x/y/z/ (ecf)
</li>
<li>
/orientation/heading/elevation/rotation
</li>
</ul>
<p>For dedicated sites, the route design is made more effective through customization for rapid data access. After the domain you can shortcut directly to an instance of one the dynamic route object pages. This works great for a site like twitter, users need only type in the route /user_name to bring up a known page. Note that this shortcut method works with the standard routes I suggested above (just need a collision handler or reserved object names).</p>
