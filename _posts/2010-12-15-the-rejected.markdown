---
layout: post
status: publish
published: true
title: The Rejected
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 6259
wordpress_url: http://www.victusspiritus.com/?p=6259
date: '2010-12-15 08:25:06 -0500'
date_gmt: '2010-12-15 15:25:06 -0500'
categories:
- Uncategorized
tags:
- startups
- career counseling
- coding
comments:
- id: 7841
  author: ''
  author_email: joe.siewert@gmail.com
  author_url: http://www.joesiewert.com
  date: '2010-12-15 17:16:00 -0500'
  date_gmt: '2010-12-15 17:16:00 -0500'
  content: I hadn't seen that video in a long time.  Still hilarious.  Completly agree
    with your post.  Despite hearing about how startups can't fill all their openings,
    it seems fiercly competitive to even get your foot in the door at one.
---
<p><a href="http://www.youtube.com/watch?v=PJYxCSXjhLI"><img src="http://www.victusspiritus.com/wp-content/uploads/2010/12/Rejected.jpg" alt="" title="Rejected" width="300" height="240" class="aligncenter size-full wp-image-6261" /></a><br />
<I>The Tech Scene heats up in NYC, but leaves most applicants out in the Cold</I></p>
<p>Big tech companies are fiercely competing for talent, primarily experienced veterans. Angel and seed funding for tech startups in the NY metro area has also intensified over the past year, leading to more small companies seeking first through fiftieth employees.</p>
<p>The trend for tech company growth is happening throughout the nation, from startup capitals like Silicon Valley, NY, and Boston to smaller tech hubs like Boulder and Portland. There simply aren't enough experienced engineers to go around. Likewise many startups are getting angel and seed funding as more investors scramble to gain ownership of nascent businesses.</p>
<p>Yet rabid investors and competitive hiring aren't changing the nature of the job or startup market. The vast majority of applicants to attractive positions in startups or BigCos are rejected. Graduating from a top school used to be enough of an edge to scale the HR barrier and land that first technical interview, but graduates have become a commodity. Fail to give the <I>approved</I> answer and your application goes into the reject bin. </p>
<p>Advanced network programming and architectures can be learned on the job, through open source contributions, or with self guided projects outside of the classroom. There are more web docs and screen casts in your preferred language for your favorite framework than you have time to study. In addition code bases are changing so rapidly that interfaces and frameworks you learn today drastically evolve in just a few months. If the frameworks are not adapting to the shifting technology landscape^ they face obsolescence against attractive alternatives. Fortunately there's a big push in modern programming languages towards more human readable forms. Structure, syntax, and relationships go a long way to abstracting away details of complex object hierarchies**.</p>
<p>Specialization plus years of experience are on just about every job description. Job seekers which don't have several years of professionally scaling and optimizing relational (SQL) or document databases (Mongo, Redis, and Couch), or designing front end user interfaces for large successful sites need not apply. There are difficulties for even sharp companies which offer unique sample problems* on their job application landing pages, with no known optimal solution. A little research shows a handful of the best heuristic answers and I'm confident the folks in charge of hiring don't want urls to open source git repos.</p>
<p>I'll wrap up on a lighter note. Here's a blast from the past and my favorite rejection, the Rejected videos by Don Hertzfeldt that the post image was taken from. </p>
<p>http://www.youtube.com/watch?v=PJYxCSXjhLI</p>
<blockquote><p>
Notes:<br />
*= I enjoy the challenging thought and implementation puzzles that people come up. Dropbox has a fun one with algorithm and code for squeezing as many rectangles into a container as possible (2d packing)</p>
<p>^= changing protocols (oauth, http, pubhubsubbub) require periodic interface updates. Utilizing cutting edge cloud services and hosts require knowledge of both their interface, features and limitations (read/write access times on virtual systems). For example datastore on the google app engine requires background processes to perform migrations, and disk access on shared file systems can be a <a href="https://github.com/blog/493-github-is-moving-to-rackspace">serious bottleneck</a> and rationale for running on bare metal physical systems.</p>
<p>** = ruby, python, perl and JavaScript are amazing glue languages. On the other end of the spectrum you'll have trouble beating c, c++, .net or jvm languages for <a href="http://shootout.alioth.debian.org/">execution speed</a>. If you read some of my older method parameter lists in c++ you're likely to pull out some hair. They are bloated and chock full of line noise:</p>
<p>virtual LibCreatedObject * MyEyes( const LibArray< LibObjectType *> &my_list) const</p>
<p>Compare this to more elegant alternatives:</p>
<p>my_eyes(my_list)</p>
<p>or</p>
<p>function my_eyes(my_list)</p>
<p>or for folks that are against polluting global namespace</p>
<p>var my_eyes = function(my_list)</p>
<p>where my_list has been declared earlier and object_types have been added to it. This looser organization requires more careful checking, but it's shocking how much line noise is removed and a blessing in how it makes the act of coding more enjoyable.</p>
<p>Static type systems require rigid attention to class definitions, while dynamic languages focus more on methods and interfaces.
</p></blockquote>
