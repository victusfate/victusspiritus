---
layout: post
status: publish
published: true
title: 'Robust Statistics Suppress Anomalies at the Cost of Concealing Emerging Trends '
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 4864
wordpress_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/08/12/robust-statistics-suppress-anomalies-at-the-cost-of-concealing-emerging-trends/
date: '2010-08-12 06:22:02 -0400'
date_gmt: '2010-08-12 13:22:02 -0400'
categories:
- Uncategorized
tags:
- social web
- far out
- math
- estimation
- influence
comments: []
---
<h2><a href="http://silvertonconsulting.com/blog/2010/03/23/spc-results-iops-vs-capacity-chart-of-the-month/"><img class="aligncenter wp-image-4867" title="Clusters" src="{{ site.url }}/assets/2010/08/Clusters1.jpg" alt="" width="500" height="350" /></a>The Source of Anomalies</h2>
<p>Real data sets are plagued by the disruptive presence of artifacts. Spike like responses can result from any number of electronic, physical, or social phenomena. Digital gain can change dramatically with temperature or <a class="zem_slink" title="Quantum tunnelling" rel="wikipedia" href="http://en.wikipedia.org/wiki/Quantum_tunnelling">electron tunneling</a>. Physical effects like unpredictable radiation bursts (solar activity), flash weather, and geometric specular points and glint (peak surface reflection) all contribute to edge data. Social spikes occur when a novel message virally spreads from a few sources to saturation levels in a short period of time.</p>
<h2>Edge Points Dominate Statistical Representations</h2>
<p>Much of research is spent improving models and reducing the impact of anomalous measurements. If special care isn't taken to minimize the impact of spikes, iterative estimates based on models will divert from true state. System models completely break down in the presence of severe artifacts.</p>
<p>Note that if you're interested in identifying spikes, ameliorating their impact on distributions will only help them stand out. Most estimation techniques have predictable degradation  with the number and size of artifacts. Take for example the mean of 4 numbers. Given the points [4,4,4,100] it's easy for us to see that the point 100 stands out as an anomaly. The mean without that value is 4 but with it the mean is 28. The variance is 0 without the outlier, and quite large with it**.</p>
<h2>A Different Way of Looking at Data</h2>
<p>Another statistical representation is available which is less susceptible to outliers, namely <a class="zem_slink" title="Robust statistics" rel="wikipedia" href="http://en.wikipedia.org/wiki/Robust_statistics">Robust Statistics</a>. Instead of characterizing  data sets with means and variances^, the set of data is represented by a median, and the median of the absolute median deviations. These measures are insensitive to outliers which can dominate standard sample estimates. For the example above 4,4,4,100 the median is 4 (it's also the mode). The median absolute deviations are 0,0,0,96. The median of these deviations is 0. So if the point 100 were truly and anomaly, applying robust statistics allows us to characterize the rest of the data fairly well.</p>
<h2>What about Anomalies that are a Signal of Systematic Change?</h2>
<p>While the occasional spike can ruin a good estimate (or a tire) a significant presence of outliers is something most geeks want to know about, understand, and characterize.</p>
<p>One of the examples I mentioned earlier was social spikes. Studying networks and messages for these types of spikes can be highly lucrative when optimizing broadcast efficiency.</p>
<p>Examples or Hypothesized Conditional Social Sharing Patterns:</p>
<ul>
<li>A great many hackers make git repo commits late at night</li>
<li>People may be more likely to share an interesting article at certain times of the day (pre-work or lunchtime)</li>
<li>Video and image sharing may dominate late night activity based on folks winding down</li>
<li>Stimulating articles may have greater attention saturation in the early morning</li>
<li>An intriguing app released at SXSW gives the early adopting conference goers something new to talk about</li>
</ul>
<p>Specific topics have a stronger viral coefficient based on their content, location, day, time, and the early audience of their release.</p>
<p>The onset of network spikes is of critical importance. Conditionally weighting the factors that contribute to communication avalanches helps us model and understand them. In this case we want to pay particular attention to the onset of message storms. Estimation techniques which are insensitive to early spikes conceal emerging trends with their steady performance until they catastrophically break down. The normalized measurement of traffic would be like a delta function when looked through the eyes of robust statistics. Understanding attention and influence will require careful analysis of both content and environment (location, day, time, early points of contact).</p>
<h2>Multiple Estimation Models</h2>
<p>A series of models may aid in understanding emerging trends. A first order application of robust statistics will clearly pick up early outliers but not characterize their distribution. A secondary (or tertiary, etc) estimation model can begin characterizing outliers and separate them to avoid catastrophic failure for the first model.  As the number of system models increase the <a class="zem_slink" title="Degrees of freedom (statistics)" rel="wikipedia" href="http://en.wikipedia.org/wiki/Degrees_of_freedom_%28statistics%29">degrees of freedom</a> are extended. A balancing pressure which penalizes the presence of secondary models is required to remove redundant models when no longer necessary.</p>
<p>Notes:<br />
*= Least Squares is an estimation technique that minimizes the sum squared error. Alternative estimates may be L1 Norm which work with absolute values much like Robust Statistics (equivalent?)</p>
<p>^= Means and variances (overall or by cluster for multimodal data) are ideal for Gaussian distributions which are common in many signal processing applications</p>
<p>**=  variance of 4,4,4,100 is 1728 or  2304 depending on whether you normalize by N or N-1. 1/3 or 1/4 of (24*24 + 24*24 + 24*24 + 72*72). By definition it's N-1 but for most large data sets the difference is negligible.</p>
<div class="zemanta-pixie" style="margin-top: 10px; height: 15px;"><a class="zemanta-pixie-a" title="Enhanced by Zemanta" href="http://www.zemanta.com/"><img class="zemanta-pixie-img" style="border: none; float: right;" src="http://img.zemanta.com/zemified_e.png?x-id=b2d0cea0-8acf-4730-9f37-f28b7346f2fa" alt="Enhanced by Zemanta" /></a><span class="zem-script more-related pretty-attribution"><script src="http://static.zemanta.com/readside/loader.js" type="text/javascript"></script></span></div>
