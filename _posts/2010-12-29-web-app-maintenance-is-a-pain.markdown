---
layout: post
status: publish
published: true
title: 'Web App Maintenance is a Pain '
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 6461
wordpress_url: http://www.victusspiritus.com/?p=6461
date: '2010-12-29 05:44:04 -0500'
date_gmt: '2010-12-29 12:44:04 -0500'
categories:
- Uncategorized
tags:
- web/tech
- coding
comments: []
---
<p>I'm familiar with maintaining libraries at my day job which a few team members rely on. Over the years our libraries grow, new libraries form, new development environments are pushed out, all driving our tools to diverge without regular synchronization and source management. </p>
<p>Besides changing requirements, delivered data formats are subject to change, often between deliveries from the same organization. The exceptions are the few cases where standards have emerged from practical usage, or we generate the data ourselves. </p>
<p>Web applications and utilities share some similarities with stand alone code maintenance. Protocols change over time to updated variations, and there's an expectation for tools to support legacy formats for some time. One big advantage of web apps over stand alone deliveries, there are accepted standards in place for delivering data (http, json). Over time these standards work their way into many offline applications, but there are optimizations gained from using specialized binary formats*.</p>
<p>An issue with web app maintenance is ensuring that all of the connections to external apps and services are up to date. Many web apps are the product of startups which are subject to talent grabs and shutting down (services die). Big companies are guilty of pulling the plug on acquired startups which can't be made profitable.</p>
<p>Even when all the interconnected services remain healthy, they are likely to iterate on interfaces by rapidly accepting and creating new standards. A look at twitter's API has seen it shift from basic anonymous hits, to credential login, to Oauth as an option, to Oauth only. And in the past year their streaming API is being pushed as the new standard, but myself <a href="http://blog.superfeedr.com/not-a-license/">and others</a> wonder why not pubsubhubbub? Now expand this interconnection with a dozen web services and you can see how maintaining apps and utilities can be a growing problem.</p>
<p>Any of the dependent tools that your app leverages can and will recieve security and bug fixes that you'll want to take advantage of. The more popular the utility, the more likely that bugs have been baked out by developers, as long as the maintainers refuse to allow feature creep to dominate the tool's design.</p>
<p>Another source of web app maintenance is changing hosts. Moving from Engine Yard to Heroku to Rackspace to Amazon will take resources, and move through the hosting trade and cost space. In addition hosts may update how you access and use them. Heroku is moving away from default gem support to requiring developers to bundle the necessary gems with their app to avoids conflicts (gem versions).</p>
<p>Notes:<br />
*= when I think of specialized binary forms compared to more XML friendly data standards the Function Miner comes to mind. This tool searched through a version of the PDB (protein database) in seconds as opposed to minutes or hours by <I>binarizing</I> the database and utilizing quaternions to super impose structure. </p>
<p>Another example is CouchDB's always HTTP interface compared to MongoDBs specific binary I/O. Mongo can handle certain batch queries and manipulations faster than Couch from what I've read (haven't benchmarked them side by side).</p>
