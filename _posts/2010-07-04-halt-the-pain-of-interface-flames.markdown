---
layout: post
status: publish
published: true
title: Halt the Pain of Interface Flames
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 4421
wordpress_url: http://www.victusspiritus.com/?p=4421
date: '2010-07-04 05:52:14 -0400'
date_gmt: '2010-07-04 12:52:14 -0400'
categories:
- Uncategorized
tags:
- coding
- design
comments:
- id: 4686
  author: Mayson
  author_email: maysonl@gmail.com
  author_url: ''
  date: '2010-07-05 00:33:29 -0400'
  date_gmt: '2010-07-05 05:33:29 -0400'
  content: 'Speaking of interface flames: dump those popups from the bottom of your
    site, they&#39;re annoying - very annoying, and they probably drive more people
    away than they attract.'
- id: 4687
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-07-05 02:01:07 -0400'
  date_gmt: '2010-07-05 07:01:07 -0400'
  content: I thought the translate in place was a nice touch, but agree that it&#39;s
    less than pleasing.
- id: 6216
  author: Cheers, where everybody knows your name &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/07/09/cheers-where-everybody-knows-your-name/
  date: '2010-10-02 02:54:54 -0400'
  date_gmt: '2010-10-02 09:54:54 -0400'
  content: "[...] to tell a friend about the site because we know it, and it solves
    a problem (good marketing). Familiarity has a cognitive effect where we&#8217;re
    much more likely to [...]"
- id: 7897
  author: The Cleaner, leverage obsessions to bring order to a chaotic universe &raquo;
    Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/12/20/the-cleaner-leverage-obsessions-to-bring-order-to-a-chaotic-universe/
  date: '2010-12-20 06:52:50 -0500'
  date_gmt: '2010-12-20 13:52:50 -0500'
  content: "[...] scientists have researched the effect of biases on decision making.
    One of the biggies is the familiarity bias commonly referred to as Maslow&#8217;s
    Hammer. Each time we encounter a novel problem we attempt to [...]"
- id: 8007
  author: Entrepreneurship !== Management &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/01/04/entrepreneurship-management/
  date: '2011-01-04 06:41:09 -0500'
  date_gmt: '2011-01-04 13:41:09 -0500'
  content: "[...] is such a thing as taking a pattern too far, and Maslow&#8217;s
    Hammer captures the cognitive pitfall of doing so. Not all (maybe not even most)
    startups benefit from a [...]"
---
<p><a href="{{ site.url }}/assets/2010/07/l_1066_1040_9FDFBA96-BAA1-47B3-843A-3F408FCE327F.jpeg"><img src="{{ site.url }}/assets/2010/07/l_1066_1040_9FDFBA96-BAA1-47B3-843A-3F408FCE327F.jpeg" alt="" class="alignnone size-full" width="500" height="400" /></a></p>
<blockquote><p>
"you are trying to keep the pain of dealing with these ill-fitting interfaces from spreading throughout your system"
</p></blockquote>
<p>Today's riff is inspired by Russ Olsen's comment above, taken from his wonderful book <a href="http://designpatternsinruby.com/">Design Patterns in Ruby</a>.</p>
<h2>Great work now leads to more work later</h2>
<p>If you build an incredible app or lib, folks will be writing interfaces^ to it for a long time. APIs are powerful when they have grown stable enough to become a reliable part of (information) infrastructure. But along the development cycle, builders are continually challenged to construct new interfaces for specific data formats*, or port the existing software to new platforms. In fact, the more useful the tool, the more this interface work will be desired or needed.</p>
<h2>Maslow's Hammer</h2>
<p>When it comes to software design, a common description of utilities is that they represent tangible tools. Developers of each framework work hard to abstract the essence of what their tool does by minimizing assumptions about data that it processes. Often they succeed so well that their tool can be used in many situations that it wasn't originally intended for, yielding both positive and negative consequences (there's more than one way to do it).</p>
<p>Now consider the effect of a common <a href="http://victusfate.github.io/victusspiritus/uncategorized/2009/07/19/can-awareness-of-our-biases-clear-our-vision/">cognitive bias</a> on the process of software design. The exposure effect is to favor an option based on one's familiarity with it. More specifically <a href="http://en.m.wikipedia.org/wiki/Law_of_the_instrument?wasRedirected=true">the law of instrument</a> captures this decision making pitfall:</p>
<blockquote><p>
The concept known as the law of the instrument, Maslow's hammer, or a golden hammer is an over-reliance on a familiar tool; as Abraham Maslow said in 1966, "It is tempting, if the only tool you have is a hammer, to treat everything as if it were a nail."
</p></blockquote>
<p>If like myself, you are digging deeply into web development from an application perspective, it's tempting to continually reuse the same framework whether it's Zend php, Python/Django, or Ruby on Rails.  In practice this leads to heavier, more bloated interfaces which can confuse new users as well as hinder your own reuse. Packaged along with familiar structures (generally a benefit) a framework may have an ever growing variety of plugins**. Unwieldy complexity is the byproduct of years of tool reuse without periodic consideration and careful code refactoring.</p>
<p>Notes:</p>
<p>^= I've got <a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/06/27/analogy-and-machine-intelligence/">interfaces</a> on my <a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/07/03/is-there-a-moores-law-for-machine-intelligence/">mind</a> this week while learning about the differences between datamapper and active record (models), the google app engine and more general platforms, and Rails and Sinatra.</p>
<p>*= better to get third parties to port their data to an accepted standard</p>
<p>**= As much as I enjoy Wordpress plugins, they are highly susceptible to breakage with every core framework upgrade</p>
