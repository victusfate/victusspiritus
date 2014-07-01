---
layout: post
status: publish
published: true
title: A Tale of Two Simulations
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8777
wordpress_url: http://www.victusspiritus.com/?p=8777
date: '2011-05-12 10:46:54 -0400'
date_gmt: '2011-05-12 17:46:54 -0400'
categories:
- Uncategorized
tags:
- coding
- design
- c++
comments:
- id: 9949
  author: Idknow
  author_email: idknow@gmail.com
  author_url: ''
  date: '2011-05-12 20:02:00 -0400'
  date_gmt: '2011-05-12 20:02:00 -0400'
  content: |
    instead of a shoehorn, use a exacto knife; come on; why are you fightin crap that doesnt want to play nice?  stop compromising!
- id: 9968
  author: Keith Strickland
  author_email: ''
  author_url: http://twitter.com/keithstrickland
  date: '2011-05-15 21:07:00 -0400'
  date_gmt: '2011-05-15 21:07:00 -0400'
  content: Not sure if this is appropriate for your situation, but have you considered
    using a simulation integration/communication framework like HLA? It can be a bit
    of a pain to get up and running but would save you having to combine the two frameworks
    directly. There is an open source implementation available at http://www.porticoproject.org..
- id: 9969
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-05-15 21:34:00 -0400'
  date_gmt: '2011-05-15 21:34:00 -0400'
  content: Thanks, that's an appropriate suggestion given the task at hand. They considered
    using HLA for communication but went with a simpler model. I believe the overhead
    of setting up and running in HLA mode is the reason the team didn't consider it
    for the work I'm currently doing.
- id: 10151
  author: Crazy East Coast Weather, Wild Work Tale of Two Sims Part Duo &mdash; Victus
    Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/06/15/crazy-east-coast-weather-wild-work-tale-of-two-sims-part-duo/
  date: '2011-06-15 04:50:46 -0400'
  date_gmt: '2011-06-15 11:50:46 -0400'
  content: "[...] BIG hybrid sim I&#8217;ve been cranking on since mid March is coming
    to a head. Everything was flowing into place [...]"
- id: 10238
  author: Hacking the Earth, a Technical Debt Horror Story &mdash; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/07/07/hacking-the-earth-a-technical-debt-horror-story/
  date: '2011-07-07 19:55:54 -0400'
  date_gmt: '2011-07-08 02:55:54 -0400'
  content: "[...] background see A Tale of Two Sims, and it&#8217;s [...]"
---
<h1>Poisoned by Pointers</h1>
<p>The past few days at work I've been wrestling with an unruly<sup><a href="#notes">1</a></sup> interface which bridges two simulation frameworks. At the interface boundary, our local libraries have been pruned down to a few dozen hierarchical object pointers in nested objects, coupled with nontrivial initialization of state of each object. The sim I'm integrating with is characterized as a mini-soa<sup><a href="#notes">2</a></sup> which leverages a modified adevs event simulator as a driver and communication hub. With a rapidly approaching deadline I have taken to coding all sorts of hacks<sup><a href="#notes">3</a></sup> that I never would have implemented on calmer days. Alas, the calm days are far fewer than the hectic ones with little hope of change.</p>
<h1>Pesky Polymorphism</h1>
<p>The architectures I'm connecting are both highly flexible and extensible. Most of the models, objects and services are polymorphic, ie you could replace a FixedPlatform, with a MovingPlatform and still call either of their Platform::Position() methods from a base class pointer. </p>
<p>But neither of these large frameworks are amenable to integration. Their interfaces and internal data structures diverge enough that sharing inheritance from joint parents would be disastrous. It's like mixing oil and water, and I'm working to squeeze my models into the gap between their surfaces.</p>
<p>The irony is that the underlying data and physics is common to both simulations by design. They both emulate physical and geometric constraints. Once I get past the individual implementations and relative calculations both frameworks are bound by gravity, object position, velocity, acceleration and orientation. </p>
<p>The major differences between the design of the two code bases is how data is treated. In one framework state is separated from model and service functionality by a strict interface, while in the other objects often have local state information to support encapsulated transformations. Each has its advantages and limitations, but they certainly don't flow well together. </p>
<p><a href="#notes" id="notes">Notes:</a></p>
<ol>
<li>by unruly I mean slightly more complicated than I'd prefer. The software I'm working with is flexible, it's just that neither architecture is amenable to integration with other frameworks</li>
<li>mini-soa stands for mini <a href="http://en.wikipedia.org/wiki/Service-oriented_architecture">service oriented architecture</a>, as it lacks the automated service registration that a full soa has. The <a href="http://www.ornl.gov/~1qn/adevs/index.html">adevs simulator</a> is well documented but has been modified heavily by the group I'm working with</li>
<li>The sins I've committed this week include but are not limited to mutable members modified in const calls, static globals, flag based initialization logic instead of moving code to constructors, initializing from truth, and shoving references to truth into measurement data. Every single good habit has been tossed carelessly to the wind to get the code up and running. </li>
</ol>
