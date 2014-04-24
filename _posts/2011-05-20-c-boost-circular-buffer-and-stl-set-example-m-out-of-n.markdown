---
layout: post
status: publish
published: true
title: M out of N
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8949
wordpress_url: http://www.victusspiritus.com/?p=8949
date: '2011-05-20 04:44:46 -0400'
date_gmt: '2011-05-20 11:44:46 -0400'
categories:
- Uncategorized
tags:
- coding
- c++
- stl
comments: []
---
<h1>c++ boost circular buffer and stl map and set example</h1>
<p>In an effort to become more familiar with boost data structures (as opposed to homebrewed ones), I took a crack at M out of N validator. It checks the last N updates and determines if M passed a certain criteria. Not all members are updated at each interval, and they are identified by an ID pair of two longs. </p>
<p>A friend pointed me to a set implementation, and I happily added a set of members, which include IDs if they ever pass the M out of N test. The sample code includes a brief set of simulated data for testing.</p>
<p><script src="https://gist.github.com/982762.js"> </script></p>
