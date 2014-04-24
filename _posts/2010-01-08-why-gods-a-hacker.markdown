---
layout: post
status: publish
published: true
title: Why God's a Hacker
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 2688
wordpress_url: http://www.victusspiritus.com/2010/01/08/why-gods-a-hacker/
date: '2010-01-08 10:01:36 -0500'
date_gmt: '2010-01-08 17:01:36 -0500'
categories:
- Uncategorized
tags:
- inspiration
- far out
- coding
- genetics
- information theory
- complex systems
- life
comments:
- id: 2617
  author: Nature Trumps the Laws of Man in the Long Run &raquo; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2010/01/14/nature-trumps-the-laws-of-man-in-the-long-run/
  date: '2010-01-14 07:46:07 -0500'
  date_gmt: '2010-01-14 14:46:07 -0500'
  content: "[...] complex adaptive systems are an excellent model to describe nature,
    because they govern our most fundamental building blocks. Is it too fantastic
    to believe that Nature is itself an adaptive system?   Share and [...]"
- id: 3006
  author: Each Day Begins with a Miracle &raquo; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2010/02/19/each-day-begins-with-a-miracle/
  date: '2010-02-19 05:47:49 -0500'
  date_gmt: '2010-02-19 12:47:49 -0500'
  content: "[...] DNA codes have evolved over hundreds of millions years. The miracle
    of our life code is that is has growing information capacity. Billions of cells
    all work in unison to grow and sustain our bodies. Our bodies are miraculous [...]"
- id: 6763
  author: Kevin Kelly&#8217;s new book, &#8220;What Technology Wants&#8221; is Alive
    &raquo; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2010/10/14/kevin-kellys-new-book-what-technology-wants-is-alive/
  date: '2010-10-14 16:44:09 -0400'
  date_gmt: '2010-10-14 23:44:09 -0400'
  content: "[...] Extropy post triggered one my personal favorite blog posts here,
    Why God&#8217;s a Hacker where I struggle to identify the information capacity
    of life&#8217;s coding [...]"
---
<h2>(with a wild coding language)</h2>
<p><a href="http://en.m.wikipedia.org/wiki/Introduction_to_genetics"><img class="aligncenter size-full wp-image-2690" title="File-ADN_animation" src="http://www.victusspiritus.com/wp-content/uploads/2010/01/File-ADN_animation1.gif" alt="" width="181" height="313" /></a></p>
<p>This is my first attempt at understanding the complexity of information within human DNA. I'll attempt to compare it to ways we describe technology (bits). Later I'll show how a direct measure may be like trying to describe irrational numbers with extra decimals (wrong way to think about it). To start, I'll be focusing on an estimate of biological information within the human genome, which may then be readily compared to technological storage.</p>
<h2>I have yet to see a single section of code (software) that can replicate the storage (info compression) of DNA structurally</h2>
<p>Technology is catching up (learning/converging?) fast though. <em>Honest disclaimer:</em> There's going to be wild handwaving, and back of the envelope calculations. If you'd prefer a scientific analysis on this topic you'll be dissappointed. What I sacrifice in rigor I hope to replace with accessibility to laymen like myself (basic bio background only, and an over active imagination).</p>
<p>This is one of those thought riffs where I wish I had full knowledge of my fiancé Michelle's molecular biology background. If she ever does read this post, I'm sure she'll be shaking her head sadly ;). For a quick and dirty background, I'm happy to refer you to a <a href="http://en.m.wikipedia.org/wiki/Introduction_to_genetics">beginner's guide to genetics</a>.</p>
<p><strong>Kansas is going bye bye, so buckle up and prepare for a wild yet intellectually lazy ride to grasp at the very patterns of life!</strong></p>
<p>As a "far out" frame of reference and inspiration, I look to <a href="http://www.kk.org/thetechnium/archives/2009/08/extropy.php">Kevin Kelly's larger envelope of calculations</a>. His extropy chapter is a lengthy read, and I've included a relevant snippet at the end of the post. Kevin's estimation of Extropy is spectacular in it's imaginative benchmarks. Mr. Kelly's writing is like a type of human programming. He gets thousands of folks excited, and we all dig into tiny fragments of his bold ideas. Alas, if only web programming was so. (github?)</p>
<p>For this discussion, I'll be focusing on the information contained within one human DNA strand (nucleic DNA, excluding mitochondrial, and other forms). Even in this single information storage mechanism, there is incredible complexity, and I'm certain my approximations will suffer due to a lack of complete knowledge of gene regulatory networks (more on that later).</p>
<p>I liken DNA's compression to a form of metaprogramming where earlier proteins and constructs beget greater complexity in the network (differentiation, feedback, competing construction/replication, fractal growth). Evolution makes all this possible with each generation, with gravity towards reoccurring emergent realizations (senses, nervous systems, etc). These are zones of stability in chaos theory.</p>
<h2>How many bits are in a strand of human DNA?</h2>
<p>Let's first identify the total number of base pairs and active protein coding genes. The wiki on the <a href="http://en.m.wikipedia.org/wiki/Human_genome?wasRedirected=true">human genome</a> was very helpful in providing these figures, which are good enough to generate ballpark estimates.</p>
<blockquote><p>The human genome is the genome of Homo sapiens, which is stored on 23 chromosome pairs. Twenty-two of these are autosomal chromosome pairs, while the remaining pair is sex-determining. The haploid human genome occupies a total of just over 3 billion DNA base pairs. The Human Genome Project (HGP) produced a reference sequence of the euchromatic human genome, which is used worldwide in biomedical sciences.</p>
<p>The haploid human genome contains ca. 23,000 protein-coding genes, far fewer than had been expected before its sequencing.[1][2][3] In fact, only about 1.5% of the genome codes for proteins, while the rest consists of non-coding RNA genes, regulatory sequences, introns, and (controversially named) "junk" DNA.[4]</p></blockquote>
<p>Consider the language nature uses  yields a 2bits*3e9, 6 gigabits or ~750 mega bytes assuming unrestricted combinations (there are restrictions). The human genome is one subset of this upper bound on possibilities.</p>
<p>To begin I've found some quick calculations done by <a href="http://www.thinkgene.com/how-much-data-is-a-human-genome/">Andrew Yates</a> (thanks Andrew) that show the number to be under 735 mega bytes. After sharing his caluculations, I'll discuss what components I believe increase the information content far greater than this data estimate.</p>
<blockquote><p>How much data IS a human genome?</p>
<p>2 bits per base (4 bases = 22)<br />
3,080.4 Mb per human genome [1]<br />
700 MB per CD-ROM<br />
(1 human genome) *<br />
(3,080,400,000 bases / 1 human genome) *<br />
(2 bits / 1 base) *<br />
(1 byte / 8 bits) *<br />
(1 MB / 1,048,576 bytes) =<br />
734.4 MB per uncompressed human genome. Easily enough to fit on a 700 MB with basic file compression like gzip.</p></blockquote>
<p>A plausible and defendable estimate of genomic raw data and it backs up my first wag at bio data.</p>
<p>After some reading I came across another intrepid soul attempting to bound the depth of genomic data. <a href="http://everything2.com/title/How+many+bits+are+in+the+human+genome%253F">The Alchemist suggests variations</a> which greatly increase the complexity.</p>
<blockquote><p>This question has a simple answer and a complicated one. The calculation starts like this : 3 billion base pairs - each of which can be one of four (A,C,G,T). So biology uses base 4 not base two - the result is around the 6 billion bit mark and comparable to the space on a hard drive.<br />
However, this is where the analogy with computers breaks down. The genome's 'bits' can be further modified by methylation and acetylation. Considering only methyl groups, this means that each base can take on eight, not four, possible forms. Although this would seem to double the amount of information it doesn't work like that. Such meta-data is used for various other purposes, like chromatin assembly. Simply put, this is a little like data archiving or compression - although the reality is much more complex.</p></blockquote>
<p>A keen commenter Brazil adds additional qualifying information:</p>
<blockquote><p>The Alchemist used a very good metaphor by comparing the genome with a hard drive, however it goes actually much further: how much of the information actually resides on the disk, and how much of it is in the drive mechanics, electronics and firmware?<br />
Recent research results suggest that a significant part of the information that makes our bodies work the way they do is not contained in the DNA itself, but rather in the metabolism of the cells that contain it, which is is not only necessary to interpret the information, but actually modifies it and offers "added value" (like, for example, the cache in a hard drive).</p></blockquote>
<p>Brazil is getting the cruxt of the information. In the simple estimate, there is no mention of active genes, which would at first appear to greatly reduce the complexity of the genome. We have 1.5% active basepairs, so this would imply only 11 megabytes of information using Andrew's framework.</p>
<p>Hold on a moment. There are 23,000 active gene sites. Each gene can interact and influence other genes in the network. Instead of thinking about the human genome as bits of data, it is more fitting to think of DNA as a dynamic library for generating genes. These genes code for proteins which feedback and allow for construction of new genes (similar to metaprogramming).</p>
<p>In order to get a feel for the information in the human genome we should consider the complexity of our gene regulatory network. For that I turned to <a href="http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.8.5380&rep=rep1&type=pdf">a paper on modelling gene regulatory networks</a> by Shoudan Liang, Stefanie Fuhrman, and Roland Somogyi.</p>
<p>In it there is a reference to Shannon's information where maximal entropy (information) occurs when elements in the system are equiprobable. Each gene is represented by a binary state, either it's on or off. So the total possible number of states are 2<sup>23,000</sup> (23k bit vector) coded genes, if they're all zero none are actively coded, all 1 and they're all on. But the states progress over time, are a function of previous state, and external conditions. We require a different model to frame information within DNA.</p>
<p>The measure of information within <a href="http://en.m.wikipedia.org/wiki/Complex_adaptive_system">a complex adaptive system</a>, a form of <a href="http://en.m.wikipedia.org/wiki/Complex_system?wasRedirected=true">complex system</a>, is limited only by the total number of realizations possible. <a href="http://en.m.wikipedia.org/wiki/John_Henry_Holland">John Holland</a> describes complex adaptive systems:</p>
<blockquote><p>A Complex Adaptive System (CAS) is a dynamic network of many agents (which may represent cells, species, individuals, firms, nations) acting in parallel, constantly acting and reacting to what the other agents are doing. The control of a CAS tends to be highly dispersed and decentralized. If there is to be any coherent behavior in the system, it has to arise from competition and cooperation among the agents themselves. The overall behavior of the system is the result of a huge number of decisions made every moment by many individual agents.[1]<br />
A CAS behaves/evolves according to three key principles: order is emergent as opposed to predetermined (c.f. Neural Networks), the system's history is irreversible, and the system's future is often unpredictable. The basic building blocks of the CAS are agents. Agents scan their environment and develop schema representing interpretive and action rules. These schema are subject to change and evolution.[2]</p></blockquote>
<p>Over time (generations) the human genome can increase in complexity. The upper bound of information within an evolving gene regulatory network is therefore unknown. Said another way, even if we quantize the bits in our DNA today, there is no direct measure of information potential for the systems future information. Perhaps it's better to characterize the rate of increase of DNA information per generation?</p>
<p>Given the above charlatan's analysis, although I'm agnostic: I now believe nature, evolution or God is most certainly a Hacker.</p>
<p>References:</p>
<ul>
<li><a href="http://en.m.wikipedia.org/wiki/Introduction_to_genetics">Beginner's guide to genetics</a></li>
<li><a href="http://en.m.wikipedia.org/wiki/Human_genome?wasRedirected=true">Human genome wiki</a></li>
<li><a href="http://en.m.wikipedia.org/wiki/Human_chromosome">Human chromosome</a></li>
<li> <a href="http://en.m.wikipedia.org/wiki/DNA?wasRedirected=true">DNA</a></li>
<li> <a href="http://en.m.wikipedia.org/wiki/Genetic_code?wasRedirected=true">genetic code</a></li>
<li> <a href="http://en.m.wikipedia.org/wiki/Gene_regulatory_network?wasRedirected=true">Gene regulatory networks</a></li>
</ul>
<p>An excerpt from <a href="http://www.kk.org/thetechnium/archives/2009/08/extropy.php">Kevin Kelly's Extropy</a>.</p>
<blockquote><p>This is more clearly seen at the extreme. The difference between four bottles of amino acids on a laboratory self and the four amino acids arrayed in your chromosomes lies in the additional structure, or ordering, those atoms get from participating in the spirals of your replicating DNA. Same atoms, more order. Those atoms of amino acids acquire yet another level of structure and order when their cellular host undergoes evolution. As organisms evolve, the informational code their atoms carry is manipulated, processed, and reordered. In addition to genetic information, the atoms now convey adaptive information. Over time, the same atoms can be promoted to new levels of order. Perhaps their one cell home joins another cell to become multicellular — that demands the informational architecture for a larger organism as well as a cell. Further transitions in evolution — the aggregation into tissues and organs, the acquisition of sex, the creation of social groups — continue to elevate the order and increase the structure of the information flowing through those same atoms.</p></blockquote>
<p>Later Kevin stretches farther than I expected:</p>
<blockquote><p>For four billion years evolution has been accumulating knowledge in its library of genes. You can learn a lot in four billion years. Every one of the 30 million or so unique species of life on the planet today is an unbroken informational thread that traces back to the very first cell. That thread (DNA) learns something new each generation, and adds that hard-won knowledge to its code.  Geneticist Motoo Kimura estimates that the total genetic information accumulated since the Cambrian explosion 500 million years ago is 10 megabytes per genetic lineage.  Now multiply the unique information held by every individual organism by all the organisms alive in the world today and you get an astronomically large treasure.  Imagine the Noah's Ark that would be needed to carry the genetic payload of every organism on earth (seeds, eggs, spores, sperms). One study estimated the earth harbored 10^30 single-cell microbes. A typical microbe, like a yeast, produces one one-bit mutation per generation, which means one bit of unique information for every organism alive. Simply counting the microbes alone (about 50% of the biomass), the biosphere contains 10^30 bits, or 10^29 bytes, or 10,000 yottabyes of genetic information. That's a lot.</p>
<p>And that is only the biological information. The technium is awash in its own ocean of information. Measured by the amount of digital storage in use, the technium today contains 487 exabytes (10^20) of information, many orders smaller than nature's total, but growing. Technology expands data by 66% per year, overwhelming the growth rates of any natural source.  Compared to other planets in the neighborhood, or to the dumb material drifting in space beyond, a thick blanket of learning and self-organized information surround this orb.</p></blockquote>
<h6 class="zemanta-related-title" style="font-size: 1em;">Related articles by Zemanta</h6>
<ul class="zemanta-article-ul">
<li class="zemanta-article-ul-li"><a href="http://arstechnica.com/science/guides/2009/09/a-brief-guide-to-dna-sequencing.ars?utm_source=rss&utm_medium=rss&utm_campaign=rss">A brief guide to DNA sequencing</a> (arstechnica.com)</li>
<li class="zemanta-article-ul-li"><a href="http://www.wired.com/wiredscience/2009/10/beyond-the-genome/">Beyond the Genome</a> (wired.com)</li>
<li class="zemanta-article-ul-li"><a href="http://www.blisstree.com/geneticsandhealth/get-your-dna-sequenced-for-200k-less/">Get Your DNA Sequenced for $200K Less!</a> (blisstree.com)</li>
<li class="zemanta-article-ul-li"><a href="http://www.nlm.nih.gov/medlineplus/news/fullstory_90939.html">Some Parts of Human Genome Get Lost</a> (nlm.nih.gov)</li>
<li class="zemanta-article-ul-li"><a href="http://r.zemanta.com/?u=http%3A//www.healthzone.ca/health/newsfeatures/article/707250---junk-dna-yields-gold-in-genome-map-to-help-fight-disease&a=8363365&rid=6ee52f0f-d0c8-418a-8800-ddb7293b2e71&e=7274ab7746cf54809eb2a71d49aedc62">'Junk DNA' yields gold in genome map to help fight disease</a> (healthzone.ca)</li>
<li class="zemanta-article-ul-li"><a href="http://arstechnica.com/science/news/2009/11/complete-genomics-produces-a-cheapwell-5000human-genome.ars?utm_source=rss&utm_medium=rss&utm_campaign=rss">Complete Genomics produces a cheap - well, $5,000 - human genome</a> (arstechnica.com)</li>
</ul>
<div class="zemanta-pixie" style="margin-top: 10px; height: 15px;"><a class="zemanta-pixie-a" title="Reblog this post [with Zemanta]" href="http://reblog.zemanta.com/zemified/6ee52f0f-d0c8-418a-8800-ddb7293b2e71/"><img class="zemanta-pixie-img" style="border: none; float: right;" src="http://img.zemanta.com/reblog_e.png?x-id=6ee52f0f-d0c8-418a-8800-ddb7293b2e71" alt="Reblog this post [with Zemanta]" /></a><span class="zem-script more-related pretty-attribution"><script src="http://static.zemanta.com/readside/loader.js" type="text/javascript"></script></span></div>
