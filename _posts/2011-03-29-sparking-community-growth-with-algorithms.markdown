---
layout: post
status: publish
published: true
title: Sparking Community Growth with Algorithms
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8133
wordpress_url: http://www.victusspiritus.com/?p=8133
date: '2011-03-29 06:15:45 -0400'
date_gmt: '2011-03-29 13:15:45 -0400'
categories:
- Uncategorized
tags:
- startups
- marketing
- optimal information
- math
- adaptive systems
- estimation
comments: []
---
<p>Today's post is inspired by an entrepreneur's request for relevance signals, metrics, and algorithms for an under served market his team is targeting. I'll generalize the suggestions I sent by email in the hopes that they'll improve from critical review and serve a broader audience. </p>
<p>A common business model for startup efforts is acting as a gravitational hub for previously disconnected communities, and creatively charging a fee for the services rendered. The pattern is to first identify and cultivate community growth, then create the conditions for a market, and finish by slowly ramping up revenue from that market while maximizing growth. Understanding that pattern is neither a necessary nor sufficient condition for success. Timing and good fortune can make or break a business. Do you <a href="http://www.youtube.com/watch?v=u0-oinyjsk0">feel lucky</a>?</p>
<p><I>Warmup Questions</I></p>
<p>I asked a series of questions to help me get a handle on the startup stage and market they are tackling. This is a variation on a standard set of questions I ask whenever I communicate with company founders. These be them*.</p>
<ul>
<li><b>Identify Power Users:</b> How do you plan to identify experts and influencers? This group will form and enforce the community identity as well as provide early growth</li>
<li><b>Monetization:</b> How will you generate revenue and is this in line with client expectations?</li>
<li><b>Know your runway:</b> How are you funding the work now, personal savings, friends and family, investors. How long will it last?</li>
<li><b>Know your market:</b> What market testing have you done to determine the viability of the concept, such as mockup in person walk throughs, manually powered live tests on a site</li>
</ul>
<p>The quality and depth of the answers reveals how the team thinks about the problem and more importantly how much legwork has already been completed. If they're generating revenue from an early prototype or growing obscenely fast the above questions are irrelevant. Let's move on to the questions that the entrepreneur needed answers to.</p>
<p><I>How do you determine what's most relevant to an individual client?</I></p>
<p>There are variety of ways you can determine relevance based on previous engagement by studying analytics and correlation, but the magic comes in cold initialization limited to external social streams, Q&A participation, or alternative shared sources. The questions you're trying to answer are <I>who is this potential client</i> and <i>what information would be most relevant to them now</I>. No known algorithms can act as intelligent agents and understand human personas, but there are companies who specialize in understanding individual tastes and dynamic clusters about those interest graphs (see <a href="http://hunch.com">Hunch</a>).</p>
<p><i>Is Your Market Hot?</i></p>
<p>Will it be shortly? If it's not an opportunistic play in a hot market, what signals have you seen to expect that the idea will spread? From my own experience, no matter how noble or necessary a given business goal is, without a high level of excitement or interest from early market feedback from at least one group of potential clients, you're off target.</p>
<p><i>Market Research Matching</i></p>
<p>If your company mission is to more deeply involve people of underrepresented communities, yet your marketing research has been limited to well represented test groups, you've got a mismatch. There's no clear connection between the early test group and the market that you've identified and are working to serve.</p>
<p>This statement may sound harsh to someone close to a project, but it helps frame a new market. Appropriate early research gives shape and plausible initialization to the clusters and topics from which relevance connections will be discovered.</p>
<p><i>Relevance Metrics within Data</i></p>
<p>The methods for identifying relevance are closely related to organization of clients and topics according to specific feature sets. Features may be binary, numeric, geolocation, textual, or anything else you can cook up. Numeric feature vectors are the most practical to work with, so refining other information into numeric representation is advised. </p>
<p>Simple clustering algorithms (kmeans) require a distance metric between the feature vectors. Statistical modes represent the means and covariances within training data. Variations in that cluster identify boundaries of interest (3 sigma soft boundary for Gaussian distributions, convex hull containers for hard boundaries). </p>
<p>Cold starting relevance scores can be thought of as a apriori probability of a new topic feature vector belonging to a certain set (classification). Without any other information or assumptions a uniform probability of cluster membership is a good initial guess.</p>
<p><i>Important signals</i></p>
<p>Social ties between consumers are stronger signals for purchase behavior, but this weighting doesn't hold for all topic and action types, ie my parents and friends all have diverse favorite foods. Neighborhoods are important for hyper local issues. Wealth, education, political ties, state vs private jobs vs small business owners, all identify topical relevance to individual clients. </p>
<p>Perhaps one of the largest effects on relevance will be influencers. Who are your clients listening to? Those who passionately describe specific issues with a story which resonates with specific groups, or across groups, will inspire interest and action.</p>
<p><I>Measurements Refine Relevance</I></p>
<p>Analytics are fresh data gathered after an initial guess. When applied they bridge interesting topics with enthusiastic clients. Click action, time on page, and ultimately purchase actions are the most powerful signals you can leverage for rapidly identifying relevance to groups. Apple is shifting it's business towards greater design and production of mobile and tablet devices and iOS based on the huge positive purchase actions of their customers.</p>
<p><I>Dynamic Groups and Clusters</I></p>
<p>Groups are dynamic constructs. They may be redefined for each category or topic. Community interests and actions may align within a given category (tech, food, photography, lolcats), but diverge overall. Careful identification of these categories will improve relevance for your user base.</p>
<p>Machine learning techniques can improve relevance over time if the problem is well defined. From the <a href="http://en.wikipedia.org/wiki/Machine_learning">wikipedia page</a></p>
<blockquote><p>
"A major focus of machine learning research is to automatically learn to recognize complex patterns and make intelligent decisions based on data; the difficulty lies in the fact that the set of all possible behaviors given all possible inputs is too large to be covered by the<br />
set of observed examples (training data). Hence the learner must generalize from the given examples, so as to be able to produce a useful output in new cases."
</p></blockquote>
<p>A simple example is object tracking where the Kalman filter is an optimal linear estimator. You have a number of measurements with random errors, line of sight biases, in conjunction with physical models. Given a collection of measurements we can construct the most probable tracks for objects (object state). The more measurements you have, the greater the reduction in uncertainty. The same goes for classification algorithms of feature vectors (the quadratic classifier being one example), and other estimation algorithms.</p>
<p>Notes:<br />
*= "These be them." This is the kind of campy writing you can get away with as a blogger.</p>
