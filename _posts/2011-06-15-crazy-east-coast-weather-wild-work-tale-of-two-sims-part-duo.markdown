---
layout: post
status: publish
published: true
title: Crazy East Coast Weather, Wild Work Tale of Two Sims Part Duo
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9268
wordpress_url: http://www.victusspiritus.com/?p=9268
date: '2011-06-15 04:49:43 -0400'
date_gmt: '2011-06-15 11:49:43 -0400'
categories:
- Uncategorized
tags:
- weather
- coding
- design
comments:
- id: 10237
  author: Hacking the Earth, a Technical Debt Horror Story &mdash; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2011/07/07/hacking-the-earth-a-technical-debt-horror-story/
  date: '2011-07-07 07:32:54 -0400'
  date_gmt: '2011-07-07 14:32:54 -0400'
  content: "[...] For background see A Tale of Two Sims, and it&#8217;s sequel. [...]"
---
<h2>Bizarro World Weather</h2>
<p>Last week I got a chance to go on a solid 21 mile walk that started with 100 degrees of humid heat, and ended with an abysmal thunderstorm and torrential down pour (kinda fun). This morning it's 55F and chilly. I do believe it's likely good ole mother nature forgot what the transition from summer to spring is supposed to be like. Gotta marvel at her unpredictability.</p>
<h2> Hefty Workload</h2>
<p>The <a href="http://www.victusspiritus.com/2011/05/12/a-tale-of-two-simulations/">BIG hybrid sim</a> I've been cranking on since mid March is coming to a head. Everything was flowing into place over the past few weeks after earlier setbacks. I added a flurry of extra services, beloved features, bug fixes, control parameters and the code guts to handle them all along with continual iterative testing. </p>
<p>I spent yesterday morning wrestling with a large slide deck to capture the details of each of the services I worked on in collaboration with a sharp engineer up in Boston, Mikhail Pevzner. I also shamelessly borrowed from his docs on shared components (tip of the hat to Mikhail). We're scheduled to do extensive integration testing sometime in the next week or two out west. Things were going so well I was even contemplating adding a nontrivial feature to enable an autonomous mode and "intelligent" mode switching. But then the predictable visit from Murphy and his god damned Law sent everything spinning sideways.</p>
<p>No, the BIG sim didn't explode in our faces, yet. I suspect that will happen when we're out doing integration testing. A fire drill popped up in my local office for a 24 hour (of work) quick and dirty stimulator (elevate your mind out of the gutter, it's a simulation that feeds into another processing segment). It needs to run in real time and generate reasonable image data. Ok, so far not a problem.</p>
<p>The sim wasn't my primary cause for concern, but the time away from BIG sim was (I could lose some of the nuances of state flow), and more importantly it requires a port of our sim libraries over to Linux. I hacked out a minimal dependency subset yesterday (part of two libraries) so my immediate porting woes are ameliorated (smaller = better). Today I need to crank quickly and efficiently in building and testing the code, then moving it to Linux (cmake!). </p>
<p>With any luck I can return to BIG sim later this week with a clear picture of all it's subtle services and synthesize a superb set of docs. Then I can back out a higher level user doc/wiki with parameter descriptions and designed data flow.</p>
<p>ps: I just dropped my phone while writing this and totally cracked the glass casing. There's $100 down the drain. A little late to pick up a case ;).</p>
