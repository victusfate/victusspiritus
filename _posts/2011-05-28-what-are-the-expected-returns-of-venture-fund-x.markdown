---
layout: post
status: publish
published: true
title: What are the expected returns of venture fund X?
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9080
wordpress_url: http://www.victusspiritus.com/?p=9080
date: '2011-05-28 04:42:11 -0400'
date_gmt: '2011-05-28 11:42:11 -0400'
categories:
- Uncategorized
tags:
- math
- finance
- optimization
comments: []
---
<h2>Estimation Theory's relation to knowledge of Statistical Distributions</h2>
<p>This story begins with a comment from <a href="http://disqus.com/sigmaalgebra/">sigmaalgebra</a>, an anonymous mathematician and <a href="http://www.avc.com/a_vc/2011/05/some-thoughts-on-investorrank.html#comment-212664010">avc regular</a>. I appreciated Sigma's explanation of theory enough to reproduce it here, because the discussion gets to the heart of estimation theory and it's relationship with knowledge about statistical distributions.</p>
<h2>The Question: What is the performance (expected returns) of venture fund X?</h2>
<blockquote><p>
<strong>Sir sigmaalgebra</strong><br />
Okay, we are an LP; there is venture firm A; and we want to evaluate their performance.</p>
<p>What we want to know is, broadly, how much money can firm A make for us over, say, the next 10 years.</p>
<p>Let that amount of money be X. Then with really meager assumptions, X is a real valued random variable with expectation, finite expectation, and finite variance. In just what all this means, there are succinct, elegant, and profound details in, say,</p>
<p>Jacques Neveu, 'Mathematical Foundations of the Calculus of Probability', Holden-Day, San Francisco.</p>
<p>Note that I didn't claim that all the details were easy reading.</p>
<p>Well, we know that we can't know the actual value of X now. So, we settle for estimating the expectation of X, that is, E[X]. For fine details on the expectation E[X], Neveu is excellent.</p>
<p>Why the expectation? Because in the long run in practice, from the (weak or strong) law of large numbers, also in Neveu, that is what we will see. So, we settle for the expectation.</p>
<p>Note: If we want to consider utility functions, then we let X be the 'utility' we want and maximize its expectation.</p>
<p>So, how are we to estimate E[X]?</p>
<p>Well, if we can get a 'sample', say, for some positive integer n, random variables Y(1), Y(2), ..., Y(n), that are independent and have the same distribution as X (full details in Neveu), then we can take the average</p>
<p>Z = ( Y(1) + Y(2) + ... + Y(n) ) / n</p>
<p>and use real random variable Z as our estimator of E[X].</p>
<p>Okay, just why would we want to use Z instead of some 'ranking', etc.? That is, just why is Z the 'estimator' we want?</p>
<p>First, Z is 'unbiased', that is, E[Z] = E[X]. That is, in the long run, Z will give us the right answer instead of something off to one side.</p>
<p>Second, among unbiased estimators, Z is the most accurate, that is, has the least variance. Details are in, say, the classic:</p>
<p>Paul R. Halmos, "The Theory of Unbiased Estimation", 'Annals of Mathematical Statistics', Volume 17, Number 1, pages 34-43, 1946.</p>
<p>So, with Z we get the world's only minimum variance, unbiased estimator.</p>
<p>And that's why we use Z and why we use averages of past data, and some assumptions, to estimate future returns.</p>
<p>And that's why we don't take seriously 'heuristics' such as ad hoc ranks.</p>
<p>And that's why we don't like results that come from just 'algorithms' without some solid reasons to take the calculations seriously.</p>
<p>And that's why we laugh at much of 'data mining, machine learning, big data, heuristics, and artificial intelligence'.</p>
<p>And that's why we want some solid reasons for any data analysis we do and not just some intuitive suggestions.</p>
<p>And that's why math with theorems and proofs is so powerful.</p>
<p>And, Mr. P. Thiel, that's some of why we go to college.</p>
<p>Thus endith the first lecture in Data Handling 101.
</p></blockquote>
<p>My response was to bring up the common fallacies of datamining, and also to discuss the limitation of estimation theory on unknown distributions. I also wanted to point sigmaalgebra at a recent find I happened upon by Jeff Jonas in support of more data over more complex statistical apparatuses.</p>
<blockquote><p>
<b>Me</b><br />
1) Unbiased estimators depend on an underlying assumption about statistical distributions. If you're model is off, your optimization is as well. Also there are a number of documented cases where L1 (absolute value) outperforms L2 (least squares) which much of the classical theory relies on.</p>
<p>2) "And that's why we laugh at much of 'data mining, machine learning, big data, heuristics, and artificial intelligence'. ", I agree that there are common <a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/05/23/common-datamining-fallacies/">fallacies</a>, but I think you'll enjoy <a href="http://jeffjonas.typepad.com/jeff_jonas/2011/04/data-beats-math.html">Jeff Jonas'</a> counter point and humorous title, "data beats math". </p>
<p>Mr. Jonas' findings:</p>
<p>"My gripe, if any, is that way too many people are chipping away at hard problems and making no material gains in decades (e.g., entity extraction and classification) … when what they actually need is more data. Not more of same data, by the way. No, they more likely need orthogonal data – data from a different sensor sharing some of the same domain, entities and features (e.g., name and driver’s license number)."
</p></blockquote>
<p>This morning I awoke to an in depth reply and schooling in linear algebra, which brought back fond memories of subspace theory in graduate school with Professor Zemanian. The central limit theorem crept in (justified but based on another assumption), as well as a practical statement describing statistical assumptions. In particular Sigma made it clear that the set of variables Y share the distribution of the fund in question X.</p>
<blockquote><p>
<b>Sir SigmaAlgebra</b><br />
Mark,</p>
<p>For your:</p>
<p>"Unbiased estimators depend on an underlying assumption about statistical distributions."</p>
<p>but on this I assumed merely that</p>
<p>"random variables Y(1), Y(2), ..., Y(n), ... have the same distribution as X"</p>
<p>and that is sufficient.</p>
<p>Or, for algebraic details, which are easy enough, since, for i = 1, 2, ..., n, each Y(i) has the same distribution as X, we have that E[Y(i)] = E[X]. Then from our estimator</p>
<p>Z = ( Y(1) + Y(2) + ... + Y(n) ) / n</p>
<p>using that expectation is linear (Neveu), we have:</p>
<p>E[Z] = E[( Y(1) + Y(2) + ... + Y(n) ) / n]</p>
<p>= ( E[Y(1)] + E[Y(2)] + ... + E[Y(n)] ) / n</p>
<p>= ( E[X] + E[X] + ... + E[X] ) / n</p>
<p>= ( n E[X] ) / n</p>
<p>= E[X]</p>
<p>so that</p>
<p>E[Z] = E[X]</p>
<p>as desired.</p>
<p>The minimum variance part from the Halmos paper is tricky to see but, still, makes only meager assumptions about the distribution of the data.</p>
<p>For your:</p>
<p>"Also there are a number of documented where cases L1 (absolute value) outperforms L2 (least squares) which much of the classical theory relies on."</p>
<p>Note: In L^1 and L^2, etc., the L abbreviates H. Lebesgue. He was an E. Borel student about 100 years ago and redid the integration in calculus. One result was 'measure theory' which via Kolmogorov became the foundations of 'modern probability' as in Neveu.</p>
<p>L^1, L^2 are 'norms', essentially definitions of distance, on 'vector spaces'. In the case of a random variable such as X, the L^1 norm is</p>
<p>|| X ||_1 = E[ |X| ]</p>
<p>On the left, the double vertical bars are common norm notation (in D. Knuth's TeX they look better). On the right, the single vertical bars are just absolute value. Here I borrow from TeX and let _1 denote a subscript.</p>
<p>The set of all X with finite L^1 forms a vector space. It turns out, as in Neveu, it's 'complete' and, hence, a Banach space. 'Complete' is much as in the real numbers, that is, for a sequence that appears to converge, there is something there for it to converge to. The rationals are not complete because rationals can converge to, e.g., pi which is not a rational. One joke is, "Calculus is the elementary properties of the completeness property of the real number system."</p>
<p>For the L^2 norm of X, that is</p>
<p>|| X ||_2 = E[ X^2 ]^(1/2)</p>
<p>Similarly the set of all X with finite L^2 forms a vector space. It turns out (Neveu again), it's 'complete' and, hence, a Banach space.</p>
<p>But also important is, for this vector space, we can define the 'inner product'</p>
<p>(X,Y) = E[ XY ]</p>
<p>Then the norm is just from the inner product:</p>
<p>|| X ||_2 = (X,X)^(1/2)</p>
<p>With this inner product, we have a Hilbert space, which is a good thing because we can do projections.</p>
<p>Completeness for the random variables under the L^1 and L^2 norms is a bit amazing.</p>
<p>It appears that Hilbert space is an abstraction of several important examples from the 19th and 20th centuries, especially Fourier theory, various orthogonal polynomials, spherical harmonics, various parts of differential equations, etc. So, get to do the derivations once, just from the axioms, and apply them many times.</p>
<p>Apparently Hilbert space was a von Neumann idea; there's a claim that once he had to explain what he meant to Hilbert!</p>
<p>Back to our estimator Z: When we have n samples, let's call our estimator Z(n). Then, as n grows large, we would like Z(n) to be a better estimator of E[X].</p>
<p>Well, in the L^2 norm, our error squared is:</p>
<p>|| Z(n) - E[X] ||_2^2 = E[ (Z(n) - E[X])^2 ]</p>
<p>= E[ (Z(n) - E[Z(n)])^2 ]</p>
<p>= Var( Z(n) )</p>
<p>or the variance of Z(n). Such math looks MUCH better in TeX!</p>
<p>But from the definition of Z(n) and our assumptions and our use of Y(1), Y(2), ..., Y(n),</p>
<p>Var( Z(n) ) = Var( ( Y(1) + Y(2) + ... + Y(n) ) / n )</p>
<p>= ( 1/n^2 ) Var( ( Y(1) + Y(2) + ... + Y(n) ) )</p>
<p>= ( 1/n^2 ) Var( Y(1) ) n</p>
<p>= Var( Z(1) ) / n</p>
<p>So, as n grows, our error</p>
<p>|| Z(n) - E[X] ||_2 = Std( Z(1) ) / n^(1/2)</p>
<p>where Std is the standard deviation, that is, the square root of the variance.</p>
<p>So for large n, our L^2 error converges to 0. So, our estimator Z(n) converges to E[X] in the L^2 norm. Then (Neveu) some subsequence of our sequence Z(n) must converge to E[X] with probability 1, that is, 'almost surely', and that's the best we can hope for. In practice, or with more analysis or assumptions, Z(n) will converge to E[X} almost surely without the issue of subsequences.</p>
<p>For practice, convergence in L^2 is good enough to take to the bank.</p>
<p>If we were to work with L^1 instead, then things would be more difficult. Also we might end up estimating the median of X and, thus, have a biased estimator of the expectation of X.</p>
<p>Also, we can know more than just that Z(n) converges to E[X}; in addition we can find 'confidence' intervals. From the sum of the Y(i) and the central limit theorem, for n over a few dozen, the distribution of Z(n) will be close to Gaussian. So, we can use a t-test to get a confidence interval. If we want to be still more careful, then there are some simple, somewhat 'computer intensive', 'distribution-free' (where we make no assumptions about the distribution of X) methods for getting a confidence interval on our estimate.</p>
<p>On the value of 'big data', that's questionable. I would recommend being careful about what we know about the data we seek and use. The criterion of "orthogonal" is not so good; likely he meant independent.</p>
<p>One warning about 'big data' is in our:</p>
<p>|| Z(n) - E[X] ||_2 = Std( Z(1) ) / n^(1/2)</p>
<p>So if we multiply n by 100, then we divide the right side by the square root of 100, that is, 10 and, thus, get just one more significant digit of accuracy in our estimate. So, getting three significant digits is common; getting four is usually a strain; getting eight or more is nearly absurd.</p>
<p>Commonly getting three significant digits is so easy that struggling with 'big data' to get, say, six significant digits is not worth the effort.</p>
<p>One of the problems in practice, e.g., in 'data mining' and 'machine learning', is just 'fitting models'. There can be some value there, but there are also some serious pitfalls: E.g., for some positive integer n and for numerical data (x(i), y(i)), for i = 1, 2, ..., n, if the x(i) are distinct then we can just write down a polynomial p of degree n-1 so that, for all i, p(x(i)) = y(i). This is called Lagrange interpolation and has a richly deserved reputation for just absurd results. Fit? Yes. Useful? No! For something less absurd, can also use various splines, least-squares splines, and for functions of several variables. Still, getting 'causality', 'meaning', or good predictions from such efforts is not easy.</p>
<p>My estimator of the coveted E[X] was from samples Y(i), but the thread assumed some additional data about first rounds and follow on rounds. So, with this additional data, might a more accurate estimate be possible? In principle, yes.</p>
<p>One approach, the most powerful possible in the L^2 sense given sufficient data, is just old cross tabulation. That is, and an easy exercise starting with Neveu, if we have some data Y and want to estimate X, then we can take the conditional expectation of X given Y, that is, E[X|Y]. Then there is some function f so that E[X|Y} = f(Y), and this function f minimizes</p>
<p>|| X - f(Y) ||_2</p>
<p>Well, cross tabulation can be used to give an estimation of a discrete approximation to f.</p>
<p>Another approach, that can work with less data, is to assume a 'model' with some parameters and then determine the parameters by fitting to the available real data. Pursuing this direction is beyond the scope of this post now!</p>
<p>This would be, what, a Q&A session after the first lecture in Data Handling 101?</p>
<p>Neveu? An elegant, powerful, crown jewel of civilization.
</p></blockquote>
<p>I found an hour this morning to carefully read through and think about Sigma's reply:</p>
<blockquote><p>
<b>Me</b><br />
Thank you for the in depth reply and review of subspace theory. Your careful description brought back fond memories of graduate school, and your passion for the subject is obvious.</p>
<p>Let's focus on a couple of assumptions that appear minor but could lead to surprise and unexpected results.</p>
<p>"random variables Y(1), Y(2), ..., Y(n), ... have the same distribution as X"</p>
<p><strike>Do you believe</strike> Would you wager that there is a distribution for X that bounds the behavior of the venture fund in question? Even if there is such a distribution and X is historically well behaved how do you account for <a href="http://en.wikipedia.org/wiki/Black_swan_theory">singularities</a>?</p>
<p>----------------------------------------------------------------------</p>
<p>Also in this step:</p>
<p>|| Z(n) - E[X] ||_2^2 = E[ (Z(n) - E[X])^2 ]<br />
= E[ (Z(n) - E[Z(n)])^2 ]<br />
= Var( Z(n) )</p>
<p>you replace E[X] with sequence Z(n) in order to later describe how Z(n) converges to E[X] for large n. </p>
<p>|| Z(n) - E[X] ||_2 = Std( Z(1) ) / n^(1/2)</p>
<p>That appears to be using the result of the derivation to prove the derivation.</p>
<p>----------------------------------------------------------------------</p>
<p>With regards to the central limit theorem:<br />
"From the sum of the Y(i) and the central limit theorem, for n over a few dozen, the distribution of Z(n) will be close to Gaussian."</p>
<p>With this statement are you pegging E[X] as Gaussian? That can't be correct. Once you assume E[X] is Gaussian you're working on a different problem, and no longer trying to predict an individual venture fund's returns. Are you stating Fred and the team at USV are properly characterized by a Gaussian random variable :)? Of course you could fit a Gaussian curve through their portfolio returns, but doing so doesn't make company returns adhere to the distribution. Fred has described fund performance as a power law curve in the past here.</p>
<p>----------------------------------------------------------------------</p>
<p>On big data: (I wish I could annotate your comment to split off better side discussions). The limitation you describe on significant digits is predicated on your model: ||Z(n) - E[X]||_2 = Std( Z(1) ) / n^(1/2). What Jeff described was by using simpler models and more data he achieved better results than by applying more complex models to far less data.</p>
<p>Is there a large difference between model fitting (agreed there are good and poor techniques), and assumed distributions? I could represent unknown spaces of measured data with a placeholder distribution that describes local region behavior instead of generating presumed values (splines/interpolation/least squares). </p>
<p>I didn't have time to dig in and understand your mention of cross tabulation, but the relationship has me interested E[X|Y] = f(Y) where f minimizes || X - f(Y) ||_2. The best estimator for current fund performance should weight previous performance, I just don't know how that would look (environment and macro economic trends impact performance as much as the selection of the investors).</p>
<p>I've relied on Taylor series expansions a number of times in Physics while chasing dominant relationships. I feel comfortable pursuing dominant relationships with limited parameter spaces. Allow parameter number to grow and your fits keep on improving (always penalize additional degrees of freedom when scoring).
</p></blockquote>
