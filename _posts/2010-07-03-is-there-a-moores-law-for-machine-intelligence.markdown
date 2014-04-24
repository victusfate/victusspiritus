---
layout: post
status: publish
published: true
title: Is there a Moore's Law for Machine Intelligence?
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 4390
wordpress_url: http://www.victusspiritus.com/?p=4390
date: '2010-07-03 03:34:51 -0400'
date_gmt: '2010-07-03 10:34:51 -0400'
categories:
- Uncategorized
tags:
- coding
- probe
- design
- machine intelligence
comments:
- id: 4679
  author: Samuel
  author_email: sam@synapticnulship.com
  author_url: http://synapticnulship.com
  date: '2010-07-04 01:07:34 -0400'
  date_gmt: '2010-07-04 06:07:34 -0400'
  content: 2. As far as the question posed by the title, there cannot be a Moore&#39;s
    Law for Machine Intelligence because intelligence is contextual.   Even a specific
    benchmark is contextual and only measures that one test.  The field of MI and
    a lot of AI may be satisfied with some narrow mathematical test, but that certainly
    won&#39;t impress those of us who are into the broader concept of AI which includes
    artificial organisms living in the same environments that biological organisms
    do.
- id: 4680
  author: Samuel
  author_email: sam@synapticnulship.com
  author_url: http://synapticnulship.com
  date: '2010-07-04 01:02:02 -0400'
  date_gmt: '2010-07-04 06:02:02 -0400'
  content: 1. I like the general concept of Probe. I have been thinking along the
    same lines for about 7 or 8 years myself.  I&#39;m not sure if dynamic/automatic
    interfaces necessarily have to be defined with a new language, but of course that
    could be the human interface for programmers, and that could be a very useful
    language and/or design pattern.  A a coder, I would like to think that everything
    could be coded by a human, at least with higher-level languages, but maybe that
    won&#39;t be efficient for certain types of architectures.
- id: 4682
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-07-04 11:53:10 -0400'
  date_gmt: '2010-07-04 16:53:10 -0400'
  content: Of course people could always dig down into the code and write it themselves.
    And reviewing interfaces would be an important priority for developers even if
    they had tools that were capable enough to guess probable intersections/mappings
    between data and processing pipelines.
- id: 4683
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-07-04 11:57:33 -0400'
  date_gmt: '2010-07-04 16:57:33 -0400'
  content: Artificial life living among us (gathering nourishment, procreating) and
    machine intelligence cover a pretty big spectrum. <br><br>My concern is that with
    the incredible processing power available today, we still can&#39;t properly simulate
    how a mind works. Instead we have focused efforts on super specialized subsystems
    some of which are major hurdles in AI/MI. Checkout IBM&#39;s <a href="http://www.research.ibm.com/deepqa/"
    rel="nofollow">Watson</a> if you haven&#39;t already, the generic Q&A data/language
    search is pretty impressive.
- id: 4704
  author: Leland
  author_email: leland@pickple.com
  author_url: ''
  date: '2010-07-06 08:45:39 -0400'
  date_gmt: '2010-07-06 13:45:39 -0400'
  content: 'I would just like to add, that in fact, there already exists many examples
    of artificial intelligence in our world.<br><br>Believe it or not, the transition
    from a human based to AI based society is already moving far along.<br><br>From
    robots working in a car factory, to the machine that automatically cuts grass
    and cleans kitchens, to the intelligent algorithms that help google sort through
    information, AI is taking over more and more areas of our life.<br><br>Eventually
    we will get to the point that AI has completely taken over things that humans
    don&#39;t want to do. <br><br>Most people think that there will be an "AI revolution"
    or sudden change of some sort, which is easy for us to understand since we are
    hard wired to think in small time frames. But what is really going to happen,
    is a slow transition into strong AI and we will wonder what happened. <br><br>It
    is exactly the same process as cell phones entering our lives. Before cell phones,
    we were perfectly happy, but now, we can&#39;t imagine living our lives without
    a cell phone on us at all times (trust me, i recently lost my cell phone and felt
    this). <br><br>So too with AI... one day we will wake up and realize just how
    much of our society is controlled by AI until eventually they take off by themselves
    while we continue living our lives together, enjoying a paradise of personal achievement
    and meaning.<br><br>Unless some government designs a nano-based self replicating
    AI before countermeasures are developed, which could wipe out the entire human
    civilization in under a week.<br><br>It&#39;s depressing to think how easy it
    is for the human race to destroy itself.<br><br>:'
- id: 4710
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-07-06 13:50:31 -0400'
  date_gmt: '2010-07-06 18:50:31 -0400'
  content: I prefer the future that is a "paradise of personal achievement and meaning"
    ;)<br>But if you can&#39;t resist looking at man&#39;s penchant for self destruction,
    check out <a href="http://www.businessinsider.com/the-world-blowed-up-real-good-2010-7-2"
    rel="nofollow">this video</a>.
---
<p><a href="http://www.ieee.org/portal/site/sscs/menuitem.f07ee9e3b2a01d06bb9305765bac26c8/index.jsp?&amp;pName=sscs_level1_article&amp;TheCat=6010&amp;path=sscs/06Sept&amp;file=Halfhill.xml"><img class="size-full wp-image-4392" title="moores_law" src="http://www.victusspiritus.com/wp-content/uploads/2010/07/moores_law.jpg" alt="" width="500" height="500"/></a></p>
<h2>High Level Programming Implementations Speed Up</h2>
<p style="text-align: left;">As I've read about the development and evolution of Rubinius and JRuby (and Duby/Surinx) it's become clear that these language implementations are getting faster. The pinnacle of modern computational speed is C and the assembly it compiles down to, with a close second being java byte code (memory permitting). But the implementation speed of C comes packaged with additional code complexity and verboseness. With advanced techniques like the application of the low level virtual machine (<a href="http://en.wikipedia.org/wiki/Low_Level_Virtual_Machine">LLVM</a>) and just in time (or ahead of time) compiling, sharp developers are converging on a balance between <a href="http://www.victusspiritus.com/2010/04/20/instant-utility-optimal-execution-syntactic-sugar/">optimal performance</a> and <a href="http://www.victusspiritus.com/2010/04/03/ideal-coding-easy-to-pickup-yet-abundant-in-function/">ease of use</a> along with readability.</p>
<h2 style="text-align: left;">Will it ever be fast enough to think?</h2>
<p>Extrapolating the advance of high level languages hits a barrier at the realm of interpretation and analogy, an ability thus far unique to sentient beings. There's no clear path forward for <a href="http://www.victusspiritus.com/2010/06/27/analogy-and-machine-intelligence/">machine intelligence</a> to mimic human problem solving ability. The dependence on software for carefully described and perfectly matched interfaces is where processing and intelligence diverge. It's easy to forget how much outside (relevant) information we bring to bear on novel problems and data translations. Moving these often tedious transformations into the realm of machine operations would be a huge break through in productivity.</p>
<h2>Probe, let's slow down the code even more</h2>
<p>The motivation behind <a href="http://www.victusspiritus.com/tag/probe/">Probe</a> is a language which allows interfaces to be sloppy or ill defined, yet continue to function. Perhaps the interfaces wouldn't operate quite as we'd expect or would function sub-optimally at first, but they'd be refined through iterations. The language* will work out similarities in data structures and look for patterns to construct bridges (adaptors) between new data and existing algorithms. Developers may guide the language instead of coding every specific contingency instruction. The language will be powerful enough to abstract a common minimal cross section between two similar data collections and functional code. Instead of relying on absolute descriptions for variables and methods (identical names, taxonomies), the language will leverage a probabilistic pattern matching of data features, both before and after processing. The statistical features of input and output data can be checked for consistency with training data, just like we do sanity checks on processed results.</p>
<p>In order to achieve this high level of utility a large set of semantic data will be required in addition to sufficient training data. We humans have a breadth of external experience we bring to problems. The language will require a notion of objects and their relation to each other as well as the human language used to describe features. It may be more practical if custom versions of the language are trained to cope with specialized disciplines and industries.</p>
<p>Notes:</p>
<p>*= Probe as I envision it is really different than formal programming languages. It's a language with a built in machine intelligence application, or smart interface guessing engine.</p>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 1304px; width: 1px; height: 1px; overflow-x: hidden; overflow-y: hidden;"><a href="http://www.victusspiritus.com/tag/probe/">http://www.victusspiritus.com/tag/probe/</a>�</div>
<h6 class="zemanta-related-title" style="font-size: 1em;">Related articles by Zemanta</h6>
<ul class="zemanta-article-ul">
<li class="zemanta-article-ul-li"><a href="http://www.victusspiritus.com/2010/06/27/analogy-and-machine-intelligence/">Analogy and Machine Intelligence</a> (victusspiritus.com)</li>
<li class="zemanta-article-ul-li"><a href="http://www.victusspiritus.com/2010/04/01/unorthodox-optimization/">Unorthodox Optimization</a> (victusspiritus.com)</li>
<li class="zemanta-article-ul-li"><a href="http://www.technologyreview.com/blog/guest/25339/?ref=rss">Blog - How the Apple II Taught Programmers To Economize</a> (technologyreview.com)</li>
<li class="zemanta-article-ul-li"><a href="http://parveenkaler.com/2010/06/30/could-ruby-be-apples-language-and-api-future-3/">Could Ruby be Apple's language and API future?</a> (parveenkaler.com)</li>
</ul>
<div class="zemanta-pixie" style="margin-top: 10px; height: 15px;"><a class="zemanta-pixie-a" title="Enhanced by Zemanta" href="http://www.zemanta.com/"><img class="zemanta-pixie-img" style="border: none; float: right;" src="http://img.zemanta.com/zemified_e.png?x-id=11ede336-88de-47cc-b86d-1d1b7925515a" alt="Enhanced by Zemanta" /></a><span class="zem-script more-related pretty-attribution"><script src="http://static.zemanta.com/readside/loader.js" type="text/javascript"></script></span></div>
