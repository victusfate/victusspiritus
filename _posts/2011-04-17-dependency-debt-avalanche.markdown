---
layout: post
status: publish
published: true
title: Dependency Debt Avalanche
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8500
wordpress_url: http://www.victusspiritus.com/?p=8500
date: '2011-04-17 03:22:38 -0400'
date_gmt: '2011-04-17 10:22:38 -0400'
categories:
- Uncategorized
tags:
- coding
- decision making
- design
comments: []
---
<p><a href="{{ site.url }}/assets/2011/04/20110417-062228.jpg"><img class="size-full aligncenter" src="{{ site.url }}/assets/2011/04/20110417-062228.jpg" alt="20110417-062228.jpg" /></a></p>
<p>Fresh features, frameworks and an endless path of external dependencies are forces which conspire to amass towering mountains of technical debt. As this debt piles ever higher we risk catastrophic failure and emergency patches caused by avalanching broken dependencies.</p>
<p>The problem is compounded when active developers create and maintain dozens of such apps for personal and professional reasons. Each and every application has its own idiosyncrasies and versioned dependencies. It's no small miracle that anyone can maintain clean working environments. Fortunately there are excellent system management tools to keep the nest of dependencies organized.</p>
<p>Web development would be a nightmare without environment tools like RVM, PythonBrew, and NVM<sup><a href="#notes">1</a></sup> to keep installations and dependencies clear. For instance, RVM ensures that all gems installed for a given Ruby environment are consistent with the active version they are installed with. And even more than that, rvm helps migrate to new versions of Ruby by installing all gems for the new environment. Unfortunately if you're a Windows Rubyist rvm isn't available to you.</p>
<p>The skilled folks responsible for crafting and maintaining many of the Ruby gems and utilities I rely on take great pains to minimize external requirements. They go through the arduous labor of removing all nonessential dependencies to avoid conflicts, ie two gems both depend on different versions of another gem.</p>
<p>The combination of proper version management utilities along with well designed library tools are potent weapons against the ever threatening avalanche of dependency debt.</p>
<p><a name="notes">Notes</a></p>
<ol>
<li><a href="https://rvm.beginrescueend.com/">rvm</a>, <a href="https://github.com/utahta/pythonbrew">pythonbrew</a>, <a href="http://tjholowaychuk.com/post/524593054/node-version-manager-preview">nvm</a></li>
</ol>
