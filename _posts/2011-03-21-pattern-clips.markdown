---
layout: post
status: publish
published: true
title: 'Pattern CLiPS '
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 7998
wordpress_url: http://www.victusspiritus.com/?p=7998
date: '2011-03-21 04:46:57 -0400'
date_gmt: '2011-03-21 11:46:57 -0400'
categories:
- Uncategorized
tags:
- semantic
- coding
- python
comments: []
---
<p><a href="http://www.clips.ua.ac.be/pages/pattern"><img src="http://www.victusspiritus.com/wp-content/uploads/2011/03/pattern_graph1.jpg" alt="" title="pattern_graph1" width="500" height="255" class="aligncenter size-full wp-image-8000" /></a><br />
I came across an intriguing language processing library a few weeks ago, and it's called <a href="http://www.clips.ua.ac.be/pages/pattern">CLiPs</a> which stands for Computational Linguistics and PsychoLinguisitics. When we were working hard on extracting entities from social streams during Victus Media's heyday, I couldn't find anything close to what this library offers. </p>
<blockquote><p>
Pattern is a web mining module for the Python programming language.</p>
<p>It bundles tools for data retrieval (Google + Twitter + Wikipedia API, web spider, HTML DOM parser), text analysis (rule-based shallow parser, WordNet interface, syntactical + semantical n-gram search algorithm, tf-idf + cosine similarity + LSA metrics) and data visualization (graph networks).</p>
<p>The module is bundled with 30+ example scripts.
</p></blockquote>
<p>Props to the <a href="http://www.clips.ua.ac.be/people">team</a> behind the library.</p>
<p>My favorite library feature is the pattern.graph module which performs pretty much what you'd expect from a graph library (path of least surprise) and includes a couple of great network node aspects. </p>
<ul>
<li>Node weight, which is computed by eigenvector centrality (think Google pagerank) and</li>
<li>Node centrality, which is the darling of network hotness, betweeness centrality which is how often a node is part of a shortest path</li>
</ul>
<p><a href="http://rgl.rubyforge.org/rgl/index.html"><img src="http://www.victusspiritus.com/wp-content/uploads/2011/03/rgl_example.jpg" alt="" title="rgl_example" width="230" height="208" class="aligncenter size-full wp-image-8002" /></a><br />
Not long after scanning the documentation I wondered if there was a set of ruby gems or modules that I could quickly take advantage of and integrate into some of my heroku hacks. An alternative is to setup a python server which runs CLiPs^. A few minutes of browsing revealed the Ruby Graph Library (<a href="http://rgl.rubyforge.org/rgl/index.html">RGL</a>). The graph lib is based on Boost Graph Library which is all good in my book (just started heavily using Boost at work).</p>
<p>One missing piece of the puzzle is a great open source natural language processing gem/lib. In our startup we leveraged third party APIs (Zemanta, Alchemy, OpenCalais) and there are a number of gems which do the same but these are all metered solutions*. I'd much prefer a local option so I can tune and grow the algorithms by leveraging various third parties and add a dash of machine learning. I suspect Google will release a compelling product for giving structure to text based on their talents at machine learning and huge corpus of language (entity extraction/graphs). If you know of a great NLP ruby gem, please point me to it, thanks!</p>
<p>Notes:<br />
^= <a href="http://flask.pocoo.org/">Flask</a> on a hosted server, or the Google app engine make good targets. </p>
<p>*=  The prominent semantic tagging tools have a nice free margin but you'll quickly run into problems if you want to process individual messages. I described the API costs and free levels in an <a href="http://www.victusspiritus.com/2010/02/08/each-time-i-get-my-hands-dirty-i-learn/">earlier post</a>.</p>
<blockquote><p>
The past few days I’ve been digging into Open Calais’ API. They have another great semantic tool which we can leverage. The big plus for Calais is there 100k hits per day limit. While debugging our list processing, I’ve already gone beyond the Zemanta API limit of 10k. Alchemy’s Orchestr8 is our goto semantic API, and it gives us 30k hit per day to work with. If necessary we can explore hitting DBPedia directly to identify our own entities from text. Relying on external tools could be more expensive than our limited revenue can practically support. It all depends on how many affiliate sales we can get per API hit. Zemanta’s pricing architecture is $1200/month for 50k hits per day at the time of writing this post. Calais may be our most viable option. Even better than that, in house semantic lookups could be the best long term solution. Lower software and maintenance cost versus API hits, and in theory we could have a massive local database to minimize response time.
</p></blockquote>
