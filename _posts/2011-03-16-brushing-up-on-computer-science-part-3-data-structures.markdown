---
layout: post
status: publish
published: true
title: Brushing Up on Computer Science Part 3, Data Structures
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 7730
wordpress_url: http://www.victusspiritus.com/?p=7730
date: '2011-03-16 05:02:05 -0400'
date_gmt: '2011-03-16 12:02:05 -0400'
categories:
- Uncategorized
tags:
- career counseling
- coding
- computer science
comments:
- id: 9446
  author: Brushing up on Computer Science Part 1, Big O &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/14/brushing-up-on-computer-science-part-1-big-o/
  date: '2011-03-16 05:08:25 -0400'
  date_gmt: '2011-03-16 12:08:25 -0400'
  content: "[...] Data Structures: arrays, lists, trees, hash tables [...]"
- id: 9447
  author: Brushing Up on Computer Science Part 2, Object Oriented Programming (OOP)
    &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/15/brushing-up-on-computer-science-part-2-object-oriented-programming-oop/
  date: '2011-03-16 05:08:41 -0400'
  date_gmt: '2011-03-16 12:08:41 -0400'
  content: "[...] Data Structures: arrays, lists, trees, hash tables [...]"
- id: 9516
  author: Brushing Up on Computer Science Part 4, Algorithms &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/17/brushing-up-on-computer-science-part-4-algorithms/
  date: '2011-03-17 06:36:08 -0400'
  date_gmt: '2011-03-17 13:36:08 -0400'
  content: "[...] Data Structures: arrays, lists, trees, hash tables [...]"
- id: 9541
  author: Brushing up on Computer Science Part 5, Graphs, Networks, and Operating
    Systems &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/17/brushing-up-on-computer-science-part-5-graphs-networks-and-operating-systems/
  date: '2011-03-18 09:15:39 -0400'
  date_gmt: '2011-03-18 16:15:39 -0400'
  content: "[...] Data Structures: arrays, lists, trees, hash tables [...]"
- id: 9560
  author: Charles Lindsay
  author_email: charles.lindsay@gmail.com
  author_url: ''
  date: '2011-03-19 21:49:00 -0400'
  date_gmt: '2011-03-19 21:49:00 -0400'
  content: I believe it's spelled "Linus Torvalds", not "Trovalds"
- id: 9611
  author: Förbered din intervju | Spelutbildningar
  author_email: ''
  author_url: http://www.spelutbildningar.se/2011/03/forbered-din-intervju/
  date: '2011-03-22 10:27:26 -0400'
  date_gmt: '2011-03-22 17:27:26 -0400'
  content: "[...] Intro and Big O 2. Object Oriented Programming 3. Data Structures:
    arrays, lists, trees, hash tables 4. Algorithms (searches, sorts, maths!) 5. Graphs,
    Networks, and Operating [...]"
- id: 9767
  author: Diametrically opposed to demolition derbies, Hash Functions &mdash; Victus
    Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/04/04/diametrically-opposed-to-demolition-derbies-hash-functions/
  date: '2011-04-04 06:58:40 -0400'
  date_gmt: '2011-04-04 13:58:40 -0400'
  content: "[...] Brushing Up on Comp Science, Data Structures [...]"
- id: 9775
  author: Red-black trees | cartesian product
  author_email: ''
  author_url: http://cartesianproduct.wordpress.com/2011/04/05/red-black-trees/
  date: '2011-04-05 14:40:33 -0400'
  date_gmt: '2011-04-05 21:40:33 -0400'
  content: "[...] Brushing Up on Computer Science Part 3, Data Structures (victusspiritus.com)
    [...]"
---
<p>"The difference between a bad programmer and a good one is whether he considers his code or his data structures more important. Bad programmers worry about the code. Good programmers worry about data structures and their relationships"<br />
<a href="http://lwn.net/Articles/193245/">Linus Torvalds</a></p></blockquote>
<p>In this third chapter overviewing computer science the thrill ride continues. I'll peak into the mind of madness, and give form to the chaos of raw information. Structured data empowers developers to move beyond the troublesome issues of I/O and manipulation, and frees their minds to consider the flow of data between well understood containers.<br />
<a href="{{ site.url }}/assets/2011/03/DataStructures.png"><img src="{{ site.url }}/assets/2011/03/DataStructures.png" alt="" title="DataStructures" width="500" height="400" class="aligncenter size-full wp-image-7768" /></a></p>
<ol>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/14/brushing-up-on-computer-science-part-1-big-o/">Intro and Big O</a></li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/15/brushing-up-on-computer-science-part-2-object-oriented-programming-oop/">Object Oriented Programming</a></li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/16/brushing-up-on-computer-science-part-3-data-structures/">Data Structures</a>: arrays, lists, trees, hash tables</li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/17/brushing-up-on-computer-science-part-4-algorithms/">Algorithms</a> (searches, sorts, maths!)</li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/17/brushing-up-on-computer-science-part-5-graphs-networks-and-operating-systems/">Graphs, Networks, and Operating Systems</a></li>
</ol>
<h2>Basic Variable Types or Primitives</h2>
<p><a href="{{ site.url }}/assets/2011/03/datatype.png"><img src="{{ site.url }}/assets/2011/03/datatype.png" alt="" title="datatype" width="532" height="386" class="aligncenter size-full wp-image-7766" /></a><br />
Primitives are basic building blocks which have known size and known persistence (just beware of endianess or the byte order). The primitive types are similar between java and c/c++ and include: simple 8 bit/1 byte chars, booleans (usually 1 byte), 2 byte shorts, 4 byte integers (and pointers in c/c++),  8 byte long integers (long longs in c++), 4 floating point (<a href="http://en.wikipedia.org/wiki/IEEE_754-2008">IEEE</a>), and 8 byte double precision floating point types. The collection of these primitive types allow optimized execution balanced with storage size.</p>
<h2>Collections (not the repo man)</h2>
<p><a href="{{ site.url }}/assets/2011/03/Screen-Shot-2014-04-10-at-3.42.32-AM.png"><img src="{{ site.url }}/assets/2011/03/Screen-Shot-2014-04-10-at-3.42.32-AM.png" alt="data types" width="839" height="248" class="aligncenter size-full wp-image-10061" /></a><br />
The trade offs between choices of data structures are based on space, search, insertion and deletion times. I'll mention big O values for a selection of operations but I don't have a full table of those handy (if you know of a great image/table please let me know).</p>
<ul>
<li><a href="http://en.wikipedia.org/wiki/Array_data_structure">Arrays</a>: Arrays are collections of elements accessed by an index. They are generally implemented with a contiguous block of memory. Access time of a known index is O(1), search is O(n), search of an ordered array O(log n). Insertion and deletion mid array can be expensive.</li>
<li><a href="http://en.wikipedia.org/wiki/Linked_list">Linked Lists</a>: are a sequence of nodes which contain an element and a link to the next node. Access time usually requires walking the list and is O(n). Various forms of lists exist including but not limited to circular (end node points to first node), singly (single link element per node), doubly (links forward and backward), and multiply (links to more than 2 nodes) linked lists.</li>
<li><a href="http://en.wikipedia.org/wiki/Associative_array">Hash, Lookup Table, Map, or Associative Array</a>: Instead of using an index like a basic array, Hashes use a key to lookup elements. Lookups, insertion and deletion are O(1) when using <a href="http://en.m.wikipedia.org/wiki/Hash_table">hash tables</a> in memory (the table maps the key to an index). Maps have O(logn) lookups and insertions.</li>
<li><a href="http://en.wikipedia.org/wiki/Tree_(data_structure)">Tree</a>: Trees can be thought of as multi-branch structures which begin at a root node and extend to reach all nodes. <a href="http://en.wikipedia.org/wiki/Self-balancing_binary_search_tree">Self balancing binary trees</a> are one of the implementations used to provide hash lookup tables above. When Hashes grow beyond memory <a href="http://en.wikipedia.org/wiki/B-tree">B-trees</a> are used. Balanced binary trees have O(log n) for search, insert or deletion.</li>
</ul>
<h2>Examples of Data Structures</h2>
<p><a href="http://couchdb.apache.org/"><img class="aligncenter size-full wp-image-4996" title="relax" src="{{ site.url }}/assets/2010/08/relax.gif" alt="" width="176" height="160" /></a><br />
<em>Case Study: <a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/09/04/first-impressions-of-sitting-a-web-app-on-couchdb/">CouchDB</a> BTree Storage</em></p>
<p>Internal storage is JSON data in a <a href="http://guide.couchdb.org/editions/1/en/btree.html">B-Tree</a> structure. This framework enables O(log N) speed lookups, insertions and deletions. The following diagram, from the definitive guide eventual consistency section, shows how a view request is handled:</p>
<p><a href="http://guide.couchdb.org/editions/1/en/consistency.html#key"><img class="aligncenter size-full wp-image-5072" title="GetRequest" src="{{ site.url }}/assets/2010/09/GetRequest.png" alt="" width="578" height="442" /></a></p>
<p>An important restriction that feeds directly into CouchDB's ability to scale, documents are accessible <a href="http://guide.couchdb.org/editions/1/en/consistency.html#key">only by key</a>, and rely on multi-version concurrency control to manage concurrent access (no locking).</p>
<p style="text-align: center;"><a href="http://guide.couchdb.org/editions/1/en/consistency.html#key"><img class="aligncenter size-full wp-image-5073" title="NoLocking" src="{{ site.url }}/assets/2010/09/NoLocking.png" alt="" width="636" height="209" /></a></p>
<p><em>STL and Boost Data Structures</em><br />
<a href="{{ site.url }}/assets/2011/03/STLDataStructures.png"><img src="{{ site.url }}/assets/2011/03/STLDataStructures.png" alt="" title="STLDataStructures" width="550" height="525" class="aligncenter size-full wp-image-7735" /></a><br />
STL and Boost are libraries which support many advanced data types for c++. Before STL was heavily adopted as a standard, my coworkers and I developed our own basic data structures (arrays, lists, vectors, matrices, etc) using templates. The good news is, they're much easier to step into when something goes wrong :).</p>
<ul>
<li><a href="http://www.sgi.com/tech/stl/">STL documentation</a> (my colleagues in Tucson pointed me here)</li>
<li><a href="http://www.boost.org/doc/libs/?view=category_Data">Boost documentation</a></li>
<li><a href="http://stackoverflow.com/questions/222658/multiset-map-and-hash-map-complexity/222674#222674">Great answer on big O for a handful of STL containers</a></li>
</ul>
<p><i>Red Black Tree (sorted has interface in Ruby)</i></p>
<p>The Ruby implementation of the <a href="http://rbtree.rubyforge.org/">RBTree</a> is a sorted associative collection.</p>
<blockquote><p>
RBTree is a sorted associative collection that is implemented with Red-Black Tree. The elements of RBTree are ordered and its interface is the almost same as Hash, so simply you can consider RBTree sorted Hash.</p>
<p>Red-Black Tree is a kind of binary tree that automatically balances by itself when a node is inserted or deleted. Thus the complexity for insert, search and delete is O(log N) in expected and worst case. On the other hand the complexity of Hash is O(1). Because Hash is unordered the data structure is more effective than Red-Black Tree as an associative collection.</p></blockquote>
