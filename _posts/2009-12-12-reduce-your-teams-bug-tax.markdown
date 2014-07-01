---
layout: post
status: publish
published: true
title: Reduce Your (team's) Bug Tax
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 2490
wordpress_url: http://victusfate.github.io/victusspiritus/uncategorized/2009/12/12/reduce-your-teams-bug-tax/
date: '2009-12-12 07:46:32 -0500'
date_gmt: '2009-12-12 14:46:32 -0500'
categories:
- Uncategorized
tags:
- software
- coding
- decision making
- design
comments:
- id: 2077
  author: Tyler Gillies
  author_email: None
  author_url: http://twitter.com/tylergillies
  date: '2009-12-13 02:21:44 -0500'
  date_gmt: '2009-12-13 07:21:44 -0500'
  content: diggin the new theme, sorry but your other one was killin me ;)
- id: 2080
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2009-12-13 07:51:52 -0500'
  date_gmt: '2009-12-13 12:51:52 -0500'
  content: Don&#39;t be sorry, the theme is the wrapper the package and message is
    what I&#39;m most concerned with. Glad you enjoy it. <br>I need to work out why
    the right widgets aren&#39;t controllable (no off button). <br><br>I was so impressed
    with netvibes/wasabi that I thought it was time to make my blog more user controlled.
    I found an awesome theme switcher but it kept knocking my sidebars empty due to
    naming/framework differences.
- id: 2140
  author: Tyler Gillies
  author_email: None
  author_url: http://twitter.com/tylergillies
  date: '2009-12-13 09:21:44 -0500'
  date_gmt: '2009-12-13 14:21:44 -0500'
  content: diggin the new theme, sorry but your other one was killin me ;)
- id: 2141
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2009-12-13 14:51:52 -0500'
  date_gmt: '2009-12-13 19:51:52 -0500'
  content: Don&#39;t be sorry, the theme is the wrapper the package and message is
    what I&#39;m most concerned with. Glad you enjoy it. <br>I need to work out why
    the right widgets aren&#39;t controllable (no off button). <br><br>I was so impressed
    with netvibes/wasabi that I thought it was time to make my blog more user controlled.
    I found an awesome theme switcher but it kept knocking my sidebars empty due to
    naming/framework differences.
---
<h2>What's Bug Tax</h2>
<p>The bug tax is a form of friction that increases with the pace of development. For each new feature added, your software gains a number of new bugs. Minimizing the time your team spends bug chasing results in greater productivity, and coincidentally more time to add new features (which introduces more bugs). Good job, you just made yourself more work.</p>
<p>There is a well known question software developers face. Is additional utility worth the complexity and cost in debugging or redesigning existing structure? It sits at the forefront of every serious designer's mind, and when increased functionality is favored too much we call it feature creep.  This concept transcends software design and is evident in just about any project design (my blog layout is a perfect example of feature creep with information overload).</p>
<p>These bugs are introduced by state complexity and the limitations of individual developers to hold entire applications, all dependent libraries, and there interactions in mind simultaneously. On my best day I can keep two large applications and many of their nuances in mind, add a third and everything falls apart. In fact if I'm <a href="http://victusfate.github.io/victusspiritus/uncategorized/2009/07/18/autopilot-for-our-brain-allows-multitasking-efficiency/">working on just one</a>, I'm much more productive. Let's review state complexity briefly.</p>
<h2>Exponential Network Interaction Growth</h2>
<p>Say I have one type of data structure and two possible states (on or off). The state complexity of a single structure is nice and simple (size 2).  Scaling that structure is a matter of geometric growth (<a href="http://en.m.wikipedia.org/wiki/Exponential_growth?wasRedirected=true">wiki reference</a>). Add N more instances of that structure and I've added two to the N possible states to be concerned with (this is how numbers are described with binary data). Now introduce one additional interaction or state and expand the number of total states many fold (an additional base state causes system expansion to 3 to the Nth power unique states).</p>
<h2>Why it's not that bad</h2>
<p>In practice this is not always as terribly complicated as it sounds. If you have high confidence in your design's current functionality, adding linear increases to complexity doesn't "break the bank" unless you are already at a resource ceiling. Resource limitations of bandwidth, acceptable delay, computer memory, and the most important developer neural ram ;). You can buy more hardware, but each developer's mind is memory limited. New team additions require familiarization with the project, and this is an ongoing and predictable cost.</p>
<p>If you are working with solid software developers, they'll have intense practical heuristics which help pair down massive complexity to manageable levels. If your team rigorously tests software, the bug is almost certainly in the latest software addition. But it's also possible that the latest features reveal existing defects or design limitations.</p>
<h2>When is an Additional Feature Worth the Bug Tax?</h2>
<p>According to one of my favorite coding authors, who has extraordinary enthusiasm for startups, <a href="http://www.paulgraham.com/wealth.html">Paul Graham suggests (in Wealth)</a> that the best path for a startup project is the steepest ascent (which reminds me of <a href="http://en.wikipedia.org/wiki/Conjugate_gradient_method">conjugate gradients</a>).</p>
<blockquote><p>Use difficulty as a guide not just in selecting the overall aim of your company, but also at decision points along the way. At Viaweb one of our rules of thumb was run upstairs. Suppose you are a little, nimble guy being chased by a big, fat, bully. You open a door and find yourself in a staircase. Do you go up or down? I say up. The bully can probably run downstairs as fast as you can. Going upstairs his bulk will be more of a disadvantage. Running upstairs is hard for you but even harder for him.</p></blockquote>
<p>Now it's time I get back to debugging at  <a href="http://victusmedia.com">Victus Media</a>. We introduced some bugs while fixing others last night.</p>
<p>Related Links:</p>
<ul>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2009/08/07/protect-your-peace-of-mind-construct-an-optimal-workspace/">Protect Your Peace of Mind, Construct an Optimal Workspace</a></li>
<li><a href="http://www.joelonsoftware.com/articles/BionicOffice.html">Bionic Office</a> by Joel Spolsky</li>
</ul>
