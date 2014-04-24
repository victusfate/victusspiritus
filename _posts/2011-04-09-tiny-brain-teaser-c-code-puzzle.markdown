---
layout: post
status: publish
published: true
title: Tiny brain teaser C code puzzle
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8355
wordpress_url: http://www.victusspiritus.com/?p=8355
date: '2011-04-09 02:17:24 -0400'
date_gmt: '2011-04-09 09:17:24 -0400'
categories:
- Uncategorized
tags:
- coding
- puzzle
comments:
- id: 9788
  author: Mystery Poster
  author_email: lkrawczyk@live.com
  author_url: ''
  date: '2011-04-09 10:11:00 -0400'
  date_gmt: '2011-04-09 10:11:00 -0400'
  content: I am node* reverse(node* first).
- id: 9790
  author: Bijo
  author_email: bijo@bijo.com
  author_url: ''
  date: '2011-04-09 15:15:00 -0400'
  date_gmt: '2011-04-09 15:15:00 -0400'
  content: list reverse
- id: 9792
  author: Thomas Luce
  author_email: ''
  author_url: http://twitter.com/thomas_luce
  date: '2011-04-09 17:33:00 -0400'
  date_gmt: '2011-04-09 17:33:00 -0400'
  content: List reverse. If you wanted to be really clever you could get rid of the
    need for a temp variable by xoring the parts you want to switch around with each
    other twice.
- id: 9793
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-04-09 17:59:00 -0400'
  date_gmt: '2011-04-09 17:59:00 -0400'
  content: Fancy :).
- id: 9794
  author: ''
  author_email: hellovetica@gmail.com
  author_url: ''
  date: '2011-04-10 01:36:00 -0400'
  date_gmt: '2011-04-10 01:36:00 -0400'
  content: A reverse sort.
- id: 9799
  author: kst
  author_email: kst@mib.org
  author_url: ''
  date: '2011-04-10 08:47:00 -0400'
  date_gmt: '2011-04-10 08:47:00 -0400'
  content: |-
    For certain values of "fancy".  The "^" operator doesn't apply to pointers, only to integers, and conversion between pointers and integers is implementation-defined.  It's entirely possible, on some systems, that you could generate an invalid intermediate value that could cause your program to crash -- or that you could just quietly generate bad results.

    Even if the xor trick works, it's one more thing you have to consider as a possible cause of that mysterious sporadic  bug that shows up six months later.

    Just use the temporary.
- id: 9888
  author: ''
  author_email: peternakah@gmail.com
  author_url: ''
  date: '2011-05-03 19:24:00 -0400'
  date_gmt: '2011-05-03 19:24:00 -0400'
  content: |
    I'd like code up more puzzles, varying complexity, and hint levels. This may have been a little too easy for a first go. But I was acquisitive even non coding types could acumen their way through it. The pointers present an issue to that group though.
---
<p>Today's post is a simple morning mystery function. What am I?<br />
(beware spoilers in the comments)</p>
<pre rel='puzzle' class='prettyprint'>
typedef struct node {
  /* data struct */
  struct node *next;
} node;

node* mystery(node* first) {
  node * prev=NULL;
  node * temp=NULL;
  node * cur=first;

  while (cur != NULL) {
    temp = cur->next;
    cur->next = prev;
    prev = cur;
    cur = temp;
  }
  return prev;
}
</pre>
<p>Thanks for error catching from redditors.</p>
<p><b>*update*:</b> GoldyOrNugget has a functional programming <a href="http://www.reddit.com/r/programming/comments/gm36g/tiny_brain_teaser_c_code_puzzle/c1ok2tm">python example</a> which you can work through. </p>
<pre rel='python_puzzle' class='prettyprint'>
def magic_function(*fs):
  return lambda x: reduce(lambda a,b: b(a), (fs+x)[::-1])
</pre>
