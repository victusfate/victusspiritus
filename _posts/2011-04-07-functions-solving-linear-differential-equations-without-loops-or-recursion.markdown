---
layout: post
status: publish
published: true
title: Functions solving linear equations without loops or recursion
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8290
wordpress_url: http://www.victusspiritus.com/?p=8290
date: '2011-04-07 05:56:51 -0400'
date_gmt: '2011-04-07 12:56:51 -0400'
categories:
- Uncategorized
tags:
- math
- coding
- computer science
comments:
- id: 10006
  author: Functions solving linear equations without loops or recursion &#8230; |
    Solve Math &amp; Science Problems - Solveable.com
  author_email: ''
  author_url: http://solveable.com/functions-solving-linear-equations-without-loops-or-recursion/
  date: '2011-05-20 21:10:59 -0400'
  date_gmt: '2011-05-21 04:10:59 -0400'
  content: "[...] equation t&#959 &#965&#1109&#1077 th&#1077 quadratic formula.  See
    th&#1077 original post here: Functions solving linear equations without loops
    &#959r recursion …  Similar Math & Science Problems:Algebra: Linear Equations
    4 : Solving linear equations with [...]"
---
<p>In this morning's post I'll touch on a topic I couldn't immediately wrap my head around. I've run into the subject of Lambda calculus before, but ignored it for three reasons.</p>
<ul>
<li>First because it was usually associated with Scheme and I could never balance parenthesis inducing immediate brain shutdown</li>
<li>Second and more importantly in nearly fifteen years of developing I never required it in practice</li>
<li>And finally even if I did have a need I wouldn't be able to leverage it as a tool in my primary work environment, lambdas and c++ are like oil and water<sup>1</sup></li>
</ul>
<p>The above rationale has since become null and void due to my near fanatic interest in a number of different programming languages and frameworks. I came across a tutorial this morning which walks through a JavaScript implementation of a fixed point combinator.</p>
<h3>Equations and Fixed Points</h3>
<p>Let's begin with an equation and see how it's solution is defined by it's fixed points:<br />
x = x<sup>2</sup> - 2<br />
This example is taken from an<br />
<a href="http://matt.might.net/articles/implementation-of-recursive-fixed-point-y-combinator-in-javascript-for-memoization/">Implementation of fixed point Y Combinator in JavaScript</a>.</p>
<blockquote><p>
Recursion as fixed points</p>
<p>It turns out that students learning algebra are already familiar with recursion and fixed points. They just don’t realize it. Consider an equation like “x = x<sup>2</sup> - 2.” (Programmers might recognize this as a recursive definition, in which x is being defined in terms of itself.)</p>
<p>If asked to solve for the value of x, a student might re-arrange the equation to use the quadratic formula. However, there is another way to express, and even find, the value(s) of x: fixed points.</p>
<p>A fixed point of a function f is an input that is equal to its output; that is x is a fixed point of the function f if x = f(x). Some functions have no fixed points; some have many. The notation Fix(f) denotes the set of fixed points of a function f.</p>
<p>Define the function f such that f(v) = v2 - 2. Then, observe that the original equation may now be re-written as "x = f(x)." In other words, the solutions to the equation are the fixed points of the function f! That is, Fix(f) = {-1,2}--a fact we can verify by seeing that</p>
<p>f(-1) = (-1)<sup>2</sup> - 2 = 1 - 2 = -1,<br />
and:<br />
f(2) = (2)<sup>2</sup> - 2 = 4 - 2 = 2<br />
or by graphing y = x and y = f(x):</p>
<p><a href="{{ site.url }}/assets/2011/04/20110407-085612.jpg"><img src="{{ site.url }}/assets/2011/04/20110407-085612.jpg" alt="" title="20110407-085612.jpg" width="300" height="186" class="aligncenter size-full wp-image-8291" /></a></p>
<p>These are exactly the solutions to x = x<sup>2</sup> - 2 given by Wolfram Alpha.</p>
<p>The insight that powers the upcoming technique is the observation that any time we have a recursive definition of the form “x = f(x),” the meaning of x is going to be defined in terms of fixed points. The trick is to find a way to obtain fixed points when the equation has the form “f = F(f),” in which the value of f is not a number, but an actual function. The Y combinator is that trick.</p>
<p>The Y combinator in theory</p>
<p>In his research on the λ-calculus and combinatory logic, Haskell Curry discovered the “paradoxical” fixed-point combinator known as the Y combinator. The Y combinator takes a functional as input, and it returns the (unique) fixed point of that functional as its output. A functional is a function that takes a function for its input. Therefore, the fixed point of a functional is going to be a function.</p>
<p>Using the concepts of functionals and fixed points, we can eliminate explicit recursion for a function through two steps:</p>
<ul>
<li>Find a functional whose fixed point is the recursive function we seek.</li>
<p></p>
<li>Find the fixed point of a functional without recursion.</li>
</ul>
<p>A simple source transformation takes care of the first step. The Y combinator takes care of the second.</p>
<pre>
Background:

Lambda:
λv.e == function (v) { return e ; }

Y(F) = F(Y(F))
function Y(F) {
    return F(Y(F)) ;
}

Y(F) = F(λ x.(Y(F))(x))

function Y(F) {
    return F(function (x) {
        return (Y(F))(x) ;
    });
}


http://www.ucombinator.org/, recursive dependency on Y removed
Y = (λh.λF.F(λ x.((h(h))(F))(x))) (λh.λF.F(λ x.((h(h))(F))(x)))

The code below is executable in javascript

// A "functional" is just a function that takes
// another function as input.  
// The Y combinator finds the fixed point
// of the "functional" passed in as an argument.
// Thus, the Y combinator satisfies the property:
//     Y(F) = F(Y(F))
// Note that Y does not reference itself:

var Y = function(F) {
    return (function(x) {
        return F(function(y) {
            return (x(x))(y);
        });
    })(function(x) {
        return F(function(y) {
            return (x(x))(y);
        });
    });
};

// (In fact, all functions above are anonymous!)
// FactGen is the functional whose fixed point is
// factorial.
// That is, if you pass the factorial function to
// FactGen, you get back the factorial function.
// Since the Y combinator returns the fixed point
// of a functional, applying the Y combinator to
// FactGen returns the factorial function!
// Note that FactGen does not reference itself:

var FactGen = function(fact) {
    return (function(n) {
        return ((n === 0) ? 1 : (n * fact(n - 1)));
    });
};


document.getElementById("result2").innerHTML =
    (Y(FactGen))(6);
</pre>
</blockquote>
<h3><a href="http://stackoverflow.com/questions/93526/what-is-a-y-combinator">What is a Y Combinator?</a></h3>
<p><a href="http://mvanier.livejournal.com/2897.html">Mike Vanier's post</a> is the top rated answer from every coder's ally StackOverflow, and his lengthy post is a self proclaimed expansion of chapter 9 from<br />
the <a href="http://www.amazon.com/Little-Schemer-Daniel-P-Friedman/dp/0262560992/ref=pd_bbs_sr_1?ie=UTF8&s=books&qid=1217491595&sr=8-1">Little Schemer</a>.</p>
<blockquote><p>
What the Y combinator is and what it does</p>
<p>The Y combinator is a higher-order function. It takes a single argument, which is a function that isn't recursive. It returns a version of the function which is recursive. We will walk through this process of generating recursive functions from non-recursive ones using Y in great detail below, but that's the basic idea.<br />
More generally, Y gives us a way to get recursion in a programming language that supports first-class functions but that doesn't have recursion built in to it. So what Y shows us is that such a language already allows us to define recursive functions, even though the language definition itself says nothing about recursion. This is a Beautiful Thing: it shows us that functional programming alone can allow us to do things that we would never expect to be able to do (and it's not the only example of this).
</p></blockquote>
<p>In the section following this quote Mike defines and describes related topics sucks as Lazy Evaluation, Combinators, functions as data, etc. </p>
<p>This post is something I'll refer back to as I'll need at least a few rereads of the linked examples, and time to get my hands dirty with with the code before I feel more comfortable with the topic. At this point I'm a little confused, but the lambda calculus that's used to remove the recursive dependency appears to bear similarity to algebraic manipulation before factoring in mathematics.</p>
<p>Other Y Combinator Implementations:</p>
<ul>
<li><a href="http://www.eecs.harvard.edu/~cduan/technical/ruby/ycombinator.shtml">Y Combinator in Ruby Autovivification</a></li>
<p></p>
<li><a href="http://blog.jcoglan.com/2008/01/10/deriving-the-y-combinator/">Deriving the Y Combinator</a> (JavaScript)</li>
<p></p>
<li><a href="http://siddhi.blogspot.com/2007/08/y-combinator-in-python.html">Y Combinator in Python</a></li>
</ul>
<p><b>Notes:</b></p>
<ol>
<li>C++ was my dominant programming environment up until two years ago. Learning, using, and thinking in a variety of other languages has opened my world to the natural beauty of code</li>
</ol>
