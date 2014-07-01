---
layout: post
status: publish
published: true
title: Language Agnostic Web Framework and Packages
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9981
wordpress_url: http://www.victusspiritus.com/?p=9981
date: '2012-04-11 04:40:23 -0400'
date_gmt: '2012-04-11 11:40:23 -0400'
categories:
- Uncategorized
tags:
- far out
- coding
- design
comments:
- id: 10667
  author: Paul W. Homer
  author_email: paul_homer@yahoo.ca
  author_url: http://theprogrammersparadox.blogspot.com
  date: '2012-04-11 13:55:00 -0400'
  date_gmt: '2012-04-11 20:55:00 -0400'
  content: "One fun thing I've been able to jam into a couple of (proprietary) frameworks
    is a high degree of 'reuse' enforcement. The idea is to make it easy and 'minimal'
    to create screens, so then the 'screen' code is nearly trivial, and all of the
    mechanics exist below in the framework. Way back, for many screens, everything
    a screen needed was around 200 lines of code. The trick is to abstract away the
    presentation and bind that to something like CSS. So all the user is really specifying
    are the main data elements. Most code can vanish into a puff of implicit handling,
    but if and only if that handling matches the assumptions of a reasonable coder.
    \n\nI did spin it a little, and split the screen handling out from the underlying
    data model. The model I moved to the server (GWT does the front-end) and then
    used Hiberate (with a lot of fiddling) to redo the older OODB paradigms. \n\nPaul."
- id: 10668
  author: Paul W. Homer
  author_email: paul_homer@yahoo.ca
  author_url: http://theprogrammersparadox.blogspot.com
  date: '2012-04-11 13:57:00 -0400'
  date_gmt: '2012-04-11 20:57:00 -0400'
  content: |-
    Someday, if I every get time, I was thinking of just having the coders spec the internal data model, and maybe a little bit of special presentation, and then having the code dynamically generate the screens (and the schema), so that the layout can automatically adapt to different form factors. One big screen on a web page, might render on a phone as two or three screens. That would be a nifty trick.

    Paul.
- id: 10670
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2012-04-16 15:19:00 -0400'
  date_gmt: '2012-04-16 22:19:00 -0400'
  content: |-
    I've think a variant of this is the goal and focus of responsive web design. Well at least the presentation layer.  You're idea sounds like it goes right from data to minimal presentation query

    http://en.wikipedia.org/wiki/Responsive_Web_Design
- id: 10671
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2012-04-16 15:19:00 -0400'
  date_gmt: '2012-04-16 22:19:00 -0400'
  content: "Hey Cool Paul. My email notifier failed that comments had come in. Pardon
    the few day delay in my reading them :D. \n\nI think I'd like to see how you put
    this together, do you have a handy screen cast of it or a public repo link?\n\n"
---
<p>I'm thinking about designing a web framework and packages without a host language. The patterns will be logical descriptions, and pseudo code in a fictional programming language (maybe I'll use <a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/05/26/probe-a-fictional-programming-language-design/">Probe</a>).</p>
<p>The design will consist of pictures, pseudo code blocks, descriptions, and comments. A wiki or github repo with markdown will serve as the best drawing board for this effort. </p>
<p>Any and all participation will be welcome after I construct a rough draft to serve as a skeleton. The design will include fictional fault tolerant persistence as well. I figure if I'm going to fantasize, I might as well do so at the highest level possible with balloon strings down to practical logical constructs. The concepts will be implementable in a variety of host languages, but I'll leave that effort up to folks who are eager to do so.</p>
<p>A design goal is to limit interaction between functional components to strictly defined interfaces. The dream is many loosely coupled simple components which are nearly self documenting.</p>
