---
layout: post
status: publish
published: true
title: Common Datamining Fallacies
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8999
wordpress_url: http://www.victusspiritus.com/?p=8999
date: '2011-05-23 05:56:45 -0400'
date_gmt: '2011-05-23 12:56:45 -0400'
categories:
- Uncategorized
tags:
- datamining
comments:
- id: 10028
  author: Quora
  author_email: ''
  author_url: http://www.quora.com/What-are-common-datamining-fallacies#ans554994
  date: '2011-05-23 11:20:19 -0400'
  date_gmt: '2011-05-23 18:20:19 -0400'
  content: |-
    <strong>What are common datamining fallacies?...</strong>

    Originally posted at Common Datamining Fallacies. “Our imagination is stretched to the utmost, not, as in fiction, to imagine things which are not really there, but just to comprehend those things which are there.” Richard Feynman, The Character of Phy...
- id: 10055
  author: What are the expected returns of venture fund X? &mdash; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2011/05/28/what-are-the-expected-returns-of-venture-fund-x/
  date: '2011-05-28 04:42:21 -0400'
  date_gmt: '2011-05-28 11:42:21 -0400'
  content: "[...] big data, heuristics, and artificial intelligence&#8217;. &#8220;,
    I agree that there are common fallacies, but I think you&#8217;ll enjoy Jeff Jonas
    counter point and humorous title, &#8220;data beats [...]"
- id: 10160
  author: A Growing Business Is A Smarter Business ~ It Seeks Answers Hidden In Data!
    | MISSIcom ~ The Business Builder&#039;s Help Desk™
  author_email: ''
  author_url: http://www.missi.com/wordpress/index.php/2011/06/16/a-growing-business-is-a-smarter-business-it-seeks-answers-hidden-in-data/
  date: '2011-06-16 18:36:16 -0400'
  date_gmt: '2011-06-17 01:36:16 -0400'
  content: "[...] Common Datamining Fallacies (Victus Spiritus blog) [...]"
---
<p>"Our imagination is stretched to the utmost, not, as in fiction, to imagine things which are not really there, but just to comprehend those things which are there."<br />
<i>Richard Feynman, The Character of Physical Law (1965)</I></p>
<p>You don't need terabytes of structured information to begin seeking patterns in data, but <a href="http://jeffjonas.typepad.com/jeff_jonas/2011/04/data-beats-math.html">it helps</a>. Today's post discusses pattern identification in data sets, in particular it explores common fallacies which are rampant in the field of datamining.</p>
<h2>Experimenter's Bias</h2>
<p>The aspiration of data scientists is to banish false assumptions which conceal true patterns. Each collection of data has a story to tell, and it is our charge and duty to best extract each set's essential character. </p>
<p>It is human nature to embellish these stories and identify presumed patterns, even without sufficient supporting evidence (<a href="http://en.m.wikipedia.org/wiki/Experimenter's_bias">experimenter's bias</a>). In short, measurements tend to yield what it is predicted, because we just hate to be wrong, and because we are perpetually short on time and funding. </p>
<p>It is only when we remove the rosy glasses of presumption, that we can begin to see what was always hidden in plain sight. The challenge is to do so independent of demands for intermediate progress in never-ending efforts to obtain bridge financing.</p>
<h2>Higher Complexity Models are unfairly preferred</h2>
<p>"We are to admit no more causes of natural things than such as are both true and sufficient to explain their appearances" <i>Isaac Newton</I></p>
<p><a href="http://en.wikipedia.org/wiki/Occam's_razor">Occam's Razor</a> is overused but the underlying principle is sound. It's a fundamental assumption that for the most part nature is conservative, and models should strive to limit the addition of dependencies. Additional degrees of freedom can always fit lower dimensional problems, but they require balancing with a penalty for each such degree introduced. Another way of looking at this is an extreme case: if I allow my parameter space to grow to the size of my data set, I can "predict" it perfectly.</p>
<p>A particular heuristic I refer back to handles the presence of additional degrees of freedom and is based on the <a href="http://en.m.wikipedia.org/wiki/Likelihood-ratio_test">Likelihood-ratio</a> test (note that this example falls for another fallacy noted below unless used with caution). It was a balanced multiple harmonic chain fitting algorithm  which fit sinusoids of varying frequency and amplitude to measured signals. For each additional sinusoid allowed, the final residuals score is penalized by the log of the total number of signals scaled by the parameter size.  That way if you were just fitting noise better the algorithm wouldn't tend towards higher dimension solutions.</p>
<h2>Drawing conclusions from drummed up data</h2>
<p>One of the many temptations for data scientists is to fill in missing gaps in data. Interpolation is acceptable in smooth spaces, therefore functions which map data into smooth spaces are preferred. Problems arise when we are too casual with interpolations in noisy or spiky data, or even worse when we extrapolate far outside of the boundaries of a collection. Methods such as mirror wrap interpolation or zero padding exist to make filter outputs smoother near boundaries, but they should be used with caution.</p>
<h2>Stats aren't magic, and the world isn't Gaussian</h2>
<p>Although a beautiful theorem and appropriate to a wide variety of problems, the <a href="http://en.m.wikipedia.org/wiki/Occam's_razor">central limit theorem</a> is likely the most damaging and misused theorem in the field of estimation. There are uncountably many novel noise sources and data distributions, and yet the first assumption many analysts make is that the combination of errors in measurements or features is normal. They then proceed to apply a range of statistical measures based on Gaussian distributions, <a href="http://en.wikipedia.org/wiki/Expectation-maximization_algorithm">Expectation-maximization</a>, optimal predictors which are designed to reduce Gaussian noise, Quadratic Classifiers, etc.</p>
<p>These aren't necessarily valueless computations, in fact they may be good enough to get you in the ballpark of relatively reasonable conclusions. But using tools blindly like Quadratic Classifiers or Expectation-maximization without making an effort to understand the underlying data and noise distributions is akin to firing blind into a crowded room in hopes of hitting a bulls eye in the dark. A Pearson's Chi-Squared goodness of fit will help reveal whether a data distribution is consistent with a known density function. I've been guilty of this assumption when reviewing novel collects more times than I can remember (poor memory).</p>
<h2>Additional Reading:</h2>
<p>The following is a fun infographic on datamining I came across recently (<a href="http://chem-eng.utoronto.ca/~datamining/dmc/data_mining_map.htm">source</a>).<br />
<a href="http://chem-eng.utoronto.ca/~datamining/dmc/data_mining_map.htm"><img src="http://www.victusspiritus.com/wp-content/uploads/2011/05/DM_map_explain_1.png" alt="" title="DM_map_explain_1" width="613" height="486" class="aligncenter size-full wp-image-9008" /></a><br />
<a href="http://chem-eng.utoronto.ca/~datamining/dmc/data_mining_map.htm"><img src="http://www.victusspiritus.com/wp-content/uploads/2011/05/DataMining.png" alt="" title="DataMining" width="157" height="48" class="alignleft size-full wp-image-9011" /></a><br />
<a href="http://chem-eng.utoronto.ca/~datamining/dmc/data_mining_map.htm"><img src="http://www.victusspiritus.com/wp-content/uploads/2011/05/DM_map_predict_1.png" alt="" title="DM_map_predict_1" width="696" height="713" class="aligncenter size-full wp-image-9013" /></a></p>
<p>Ilya Grigorik writes one of my favorite technical blogs, he's got a knack for explaining complex problems in comprehensible chunks. I've been working on varied estimation and pattern matching problems for ~15 years, yet I always pick up some novel tricks or new ways of looking at pattern matching problems from visiting. </p>
<ul>
<li><a href="http://www.igvita.com/2011/04/20/intuition-data-driven-machine-learning/">Intuition and Data Driven Machine Learning</a></li>
<li><a href="http://www.igvita.com/2009/09/01/collaborative-filtering-with-ensembles/">Collaborative Filtering</a></li>
<li><a href="http://www.igvita.com/2008/01/07/support-vector-machines-svm-in-ruby/">Support Vector Machines</a></li>
<li><a href="http://www.igvita.com/2007/04/16/decision-tree-learning-in-ruby/">Decision Tree Learning</a></li>
<li><a href="http://www.igvita.com/2007/01/15/svd-recommendation-system-in-ruby/">SVD recommendation system in ruby</a></li>
</ul>
<p>Other fun datamining reading:</p>
<ul>
<li><a href="http://jeffjonas.typepad.com/jeff_jonas/2011/04/data-beats-math.html">Data beats math</a> by Jeff Jonas</li>
<li><a href="http://blog.jteam.nl/2009/12/09/mahout-taste-part-one-introduction/">Mahout taste part 1</a></li>
<li><a href="http://ssc.io/deploying-a-massively-scalable-recommender-system-with-apache-mahout/">Deploying a massively scalable recommended system with Apache Mahout</a></li>
<li><a href="http://creativemachines.cornell.edu/eureqa">Eureqa</a> is a software tool for detecting equations and hidden mathematical relationships in your data</li>
</ul>
