---
layout: post
status: publish
published: true
title: Regular expressions blues
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 7044
wordpress_url: http://www.victusspiritus.com/?p=7044
date: '2011-02-01 09:24:38 -0500'
date_gmt: '2011-02-01 16:24:38 -0500'
categories:
- Uncategorized
tags:
- coding
- regex
comments:
- id: 8662
  author: Kevin Marshall
  author_email: falicon33@gmail.com
  author_url: http://blog.botfu.com
  date: '2011-02-01 16:57:00 -0500'
  date_gmt: '2011-02-01 16:57:00 -0500'
  content: |-
    The problem is it's basically like saying "French is unreadable" because you don't know French well enough yet.

    Regex is not a simple 'language' to learn, but it *is* very powerful and well worth spending lots of time on...you could probably create a subset of regex that was more 'readable' (and many have) but what you'll give up is lots of power and flexibility.

    But I do feel for you...even after years of working with REGEX, I often make subtle mistakes that take awhile to debug...such is life.
- id: 8674
  author: Kevin C.
  author_email: disqus@kevin.lebleu.info
  author_url: http://www.google.com/profiles/lablua
  date: '2011-02-01 18:43:00 -0500'
  date_gmt: '2011-02-01 18:43:00 -0500'
  content: "A lot of people are intimidated by the poor readability of Regex, and
    I'll admit that even as an expert reading those messes above is tough. One way
    Perl tries to improve on this is the x flag that lets you add whitespace and comments
    to regular expressions. The x flag would allow your re-arrangement into rows,
    though keeping the original symbols.\n\nNone of your translations appear to keep
    the original meaning regarding optional characters.\n\nI do wonder if maybe the
    time has come for a \"Pythonization\" of reg ex - a new more readable, even if
    somewhat more verbose, way to write regular expressions, but retaining all the
    power.\n\nHere is my attempt at a more readable version:\n\nstart_of_line\noptional
    \"(\" \n(3 digits)         # I've retained parens for capture groups\noptional
    \")\"\noptional any of \"- \"   # Using whitespace in quotes here is probably
    not good for readability\n(3 digits)\noptional any of \"- \"\n(4 digits)\nend_of_line\n\nA
    lot more verbose, but a lot more readable I think too... wonder if I should attempt
    the email one.."
- id: 8678
  author: Kevin C.
  author_email: disqus@kevin.lebleu.info
  author_url: http://www.google.com/profiles/lablua
  date: '2011-02-01 19:44:00 -0500'
  date_gmt: '2011-02-01 19:44:00 -0500'
  content: "That email regex is actually somewhat poorly written... there are a lot
    of cases where it writes like <code>/X|[YZ]|[a-z]/</code> when it could say <code>/[XYZa-z]/</code>.
    I've preserved such oddities exactly below. I also put a pretty printed version
    of it at https://gist.github.com/806489 that I needed to make to translate to
    below.\n\n{\ncase_insensitive flag\nbegin_of_line\n(\n  (\n    once_or_more (any
    between \"a\" and \"z\" or digit or any of \"!#$%&amp;'*+-/=?^_`{|}~\" or any
    between \"u00A0\" and \"uD7FF\", \"uF900\" and \"uFDCF\", \"uFDF0\" and \"uFFEF\")\n
    \   zero_or_more ( \".\" once_or_more (any between \"a\" and \"z\" or digit or
    any of \"!#$%&amp;'*+-/=?^_`{|}~\" or any between \"u00A0\" and \"uD7FF\", \"uF900\"
    and \"uFDCF\", \"uFDF0\" and \"uFFEF\") )\n  )\n  or\n  (\n    zero_or_more (\n
    \     (double_quote)\n      optional (\n          optional ( zero_or_more (space
    or tab) (cr lf) )\n          once_or_more (space or tab)\n      )\n      (\n        ([x01-x08x0bx0cx0e-x1fx7f]
    or \"x21\" or [x23-x5b] or [x5d-x7e] or [u00A0-uD7FFuF900-uFDCFuFDF0-uFFEF])\n
    \       or \n        ( \"\\\" ([x01-x09x0bx0cx0d-x7f] or [u00A0-uD7FFuF900-uFDCFuFDF0-uFFEF])
    )\n      )\n    )\n    optional (\n      optional (zero_or_more (space or tab)
    (cr lf))\n      one_or_more (space or tab)\n    )\n    (double_quote)\n  )\n)\n\"@\"\nonce_or_more
    (\n  (\n    (any between \"a\" and \"z\" or digit or any between \"u00A0\" and
    \"uD7FF\", \"uF900\" and \"uFDCF\", \"uFDF0\" and \"uFFEF\")\n    or\n    (\n
    \     (any between \"a\" and \"z\" or digit or any between \"u00A0\" and \"uD7FF\",
    \"uF900\" and \"uFDCF\", \"uFDF0\" and \"uFFEF\")\n      zero_or_more (any between
    \"a\" and \"z\" or digit or \"-\" or \".\" or \"_\" or \"~\" or any between \"u00A0\"
    and \"uD7FF\", \"uF900\" and \"uFDCF\", \"uFDF0\" and \"uFFEF\")\n      (any between
    \"a\" and \"z\" or digit or any between \"u00A0\" and \"uD7FF\", \"uF900\" and
    \"uFDCF\", \"uFDF0\" and \"uFFEF\")\n    )\n  )\n  \".\"\n)\n(\n  (any between
    \"a\" and \"z\" or any between \"u00A0\" and \"uD7FF\", \"uF900\" and \"uFDCF\",
    \"uFDF0\" and \"uFFEF\")\n  or\n  (\n    (any between \"a\" and \"z\" or any between
    \"u00A0\" and \"uD7FF\", \"uF900\" and \"uFDCF\", \"uFDF0\" and \"uFFEF\")\n    zero_or_more
    (any between \"a\" and \"z\" or digit or \"-\" or \".\" or \"_\" or \"~\" or any
    between \"u00A0\" and \"uD7FF\", \"uF900\" and \"uFDCF\", \"uFDF0\" and \"uFFEF\")\n
    \   (any between \"a\" and \"z\" or any between \"u00A0\" and \"uD7FF\", \"uF900\"
    and \"uFDCF\", \"uFDF0\" and \"uFFEF\")\n  )\n)\noptional \".\"\nend_of_line\n}\n\nSummary
    of proposed new reg ex language:\n\n* New regex quantifiers are prefixes instead
    of postfixes\n\n\n\tNew regex\t\tOld regex\n\t(\t\t\t(\n\t)\t\t\t)\n\t\"literal\"\t\tliteral\n\t\"\\\"\t\t\t\\\n\t#
    Comment to end of line\n\tany between \"X\" and \"Y\"\t[X-Y]\n\tany of \"XYZ\"\t\t[XYZ]\n\tbegin_of_line\t\t^\n\tcr\t\t\tx0d\tr\n\tdouble_quote\t\tx22\t\"\n\tend_of_line\t\t$\n\tdigit\t\t\td\n\tdigits\t\t\td\n\tlf\t\t\tx0a\tn\n\tonce_or_more\t\t+\n\toptional\t\t?\n\tspace\t\t\tx20\n\ttab\t\t\tx09\tt\n\tzero_or_more\t\t*\n\nProbably
    should add some easy way to define a new term within an expression.\n\nSo far
    everything I've come up with above would allow for automatic translation between
    plain regular expressions and this new fangled readable syntax."
- id: 8694
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-02-01 21:29:00 -0500'
  date_gmt: '2011-02-01 21:29:00 -0500'
  content: "I've only written a dozen or so regex's between Ruby and Javascript, and
    each time it feels like I'm starting from scratch. One of these days... :D. \n\nGood
    to know it gets better later."
- id: 8721
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-02-02 00:08:00 -0500'
  date_gmt: '2011-02-02 00:08:00 -0500'
  content: "This is an amazing translation. Thank you Kevin. It'll take me some time
    to work through theses expressions in detail. But by the end I'll be much more
    comfortable with regexes by the time\r\nI'm done. Don't suppose you have a blog
    to prop this up on for me to link back to and post around? It's worth starting
    one for (wordpress, blogger, etc)."
- id: 8792
  author: Tyler
  author_email: tjgillies@gmail.com
  author_url: http://www.pdxbrain.com
  date: '2011-02-02 09:53:00 -0500'
  date_gmt: '2011-02-02 09:53:00 -0500'
  content: |-
    http://txt2re.com/

    awesome site that matches predetermined string and then gives you a regex to match similar patterns
- id: 8797
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-02-02 12:19:00 -0500'
  date_gmt: '2011-02-02 12:19:00 -0500'
  content: woohoo, I can return to blissfully forgetting about regex patterns. If
    my regex density (number of regular expressions/week) goes over a threshold I'll
    eventually learn the syntax. Thanks!
---
<p><i>Or why I hate regular expressions, they're not designed for readability</i></p>
<p>Early this morning I caught up on a recent <a href="http://thechangelog.com/post/3028809528/happy-js-form-ishappy-lightweight-extensible-form-valida">changelog</a> covering <a href="https://github.com/andyet/Happy.js">Happy.js</a>, a lightweight form validation plugin. My first reaction, <i>nifty</i>. I can use a handy form validator for web app inputs. As I was skimming through the example validation functions the REGEX reached out the page and slapped me in the face. It was only then that I realized how unintuitive regular expressions are.</p>
<p>I can handle this regex for phone numbers, while it takes a little familiarity to follow at least it fits in a pre tag:</p>
<pre>
/^\(?(\d{3})\)?[\- ]?(\d{3})[\- ]?(\d{4})$/.test(val)
</pre>
<p>Then came this beast for email validation, go ahead keep on scrolling right...<br />
<script src="https://gist.github.com/805713.js?file=email%20validator%20from%20happy.js"></script></p>
<p>What I'd prefer is an expressive syntax that fits with patterns as I think of them. So for a phone number validation it would be #(###)###-#### where # specifies a singlet digit number, or an equivalent abbreviated form  #({3}#){3}#-{4}#. Same for email *@*.EXTs where * is any character sequence and EXTs specifies a user defined list of acceptable extensions. Explicit character matches can be done by adding the characters i.e. *@gmail.com for all gmail addresses. Of course this syntax will need an escape character for reserved symbols and the standard case insensitive flag or global versus first match replacement (i and g flags for regular expressions). Unfortunately it appears all I've done is reinvent another flavor of regular expression.</p>
<p>Another tactic may aid in simplifying the syntax appearance, rearranging the validation string into rows.<br />
#<br />
({3}#))<br />
{3}#<br />
-<br />
{4}#<br />
Not exactly a thing of beauty. I don't  have any more time at the moment, but I'd like to revisit the problems with easy regular expression reading.</p>
