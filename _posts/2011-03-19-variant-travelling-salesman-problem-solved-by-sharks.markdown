---
layout: post
status: publish
published: true
title: Variant Travelling Salesman Problem solved by Sharks
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 7947
wordpress_url: http://www.victusspiritus.com/?p=7947
date: '2011-03-19 06:39:34 -0400'
date_gmt: '2011-03-19 13:39:34 -0400'
categories:
- Uncategorized
tags:
- evolution
- far out
- cogsci
comments:
- id: 9864
  author: Circuits, Shortest Paths, and Capitalism &mdash; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/04/26/circuits-shortest-paths-and-capitalism/
  date: '2011-04-26 06:28:34 -0400'
  date_gmt: '2011-04-26 13:28:34 -0400'
  content: "[...] few weeks back I mentioned a well known resource minimization problem
    called the Traveling Salesman, and a far out [...]"
---
<p style="text-align: center;"><a href="{{ site.url }}/assets/2011/03/pool_shark.jpg"><img class="aligncenter size-full wp-image-7952" title="pool_shark" src="{{ site.url }}/assets/2011/03/pool_shark.jpg" alt="" width="525" height="420" /></a></p>
<p>The product of thinking about computer science problems with every spare moment over a week has left me with a a terrible sense of humor and an undeniable need to make ludicrous analogies, this post is the latter. </p>
<p>The <a href="http://en.wikipedia.org/wiki/Travelling_salesman_problem">Travelling Salesman Problem</a> or TSP for abbreviation junkies is a well known problem in computer science (or sales). Given a list of cities and locations, one must find the shortest path that visits all cities <strong>exactly once</strong>.  What's up with that exactly once clause? I don't know about you, but I find that to be an awkward restriction for a travelling salesman. You're going to want to loop back and revisit towns you unloaded your wares in earlier unless  you're selling miracle elixirs or IPO shares. Shall we rename the travelling salesman, the travelling charlatan?</p>
<p>The complexity of the problem comes into play because the number of potential paths grows as a factorial of the number of cities and paths. Simple heuristics like locally finding the nearest neighbor are easily proven to fail to find the global minimum and may diverge far from the ideal solution.</p>
<p><i>A different travelling salesman problem</i></p>
<p>What if the salesman doesn't know where each of the cities are? What if some cities have no interest in buying or become ghost towns before the salesman arrives? What if the salesman needs to make enough sales to cover living expenses at each city? Would you agree that the problem has become even more challenging? Now the salesman has limited reach, and may end up at destinations without eager customers. I thought about this type of problem from a more realistic salesman perspective, as I've had my fill of theory this week. The final piece of the <del>puzzle</del> madness pie came when I thought to replace the salesman with another species, in particular a shark. My inspiration, life finds solution to intractable problems every day.</p>
<p><i>Jump the shark</i><br />
<a href="{{ site.url }}/assets/2011/03/FailWhaleJumpsTheShark.jpg"><img src="{{ site.url }}/assets/2011/03/FailWhaleJumpsTheShark.jpg" alt="" title="FailWhaleJumpsTheShark" width="500" height="490" class="aligncenter size-full wp-image-7957" /></a></p>
<p>A shark may find its meals far and few between. If the shark fails to find it's next meal before it's energy runs out, it faces a grim fate. Now we have dynamic locations with available food (4D x,y,z,T), dynamic reach as the shark can swim only so far, and an ongoing motivation to continue searching out meals in order to survive (hunger). I'm curious what genetically coded strategies in the shark's mind enable it to efficiently seek out nourishment, and how may we mimic fragments of those algorithms.</p>
<p>Let's begin the investigation by seeking patterns in how a shark may find its prey. It's known that sharks have an uncanny sense of smell for blood in the water, and this can guide them to find prey over long distances. But what tactics do sharks take when lacking observations?<br />
<a href="http://www.sciencenews.org/view/generic/id/60106/title/Sharks_use_math_to_hunt"><img src="{{ site.url }}/assets/2011/03/Walk_this_way_.jpeg" alt="" title="Walk_this_way_" width="445" height="458" class="aligncenter size-full wp-image-7960" /></a><br />
The above image and the following excerpt are from a science news article, <a href="http://www.sciencenews.org/view/generic/id/60106/title/Sharks_use_math_to_hunt">"Sharks use math to hunt"</a>.<br />
</a></p>
<blockquote><p>
A new study suggests that some sharks and other marine predators can follow strict mathematical strategies when foraging for dinner. The work, reported online June 9 in Nature, is the latest aiming to show whether animals sometimes move in a pattern called a Lévy walk.</p>
<p>Unlike random motion — in which animals take similar-sized steps in any direction, like a drunk stumbling around — <a href="http://en.wikipedia.org/wiki/L%C3%A9vy_flight">Lévy walks</a> are punctuated by rare, long forays in any direction. Draw a Lévy walk on a graph, and its squiggly pattern echoes a fractal, the mathematical phenomenon whose shape remains similar no matter the viewing scale.</p>
<p>“Living organisms, when allowed to make freely willed decisions, seem to end up obeying some kind of mathematical law,” says Gandhimohan Viswanathan, a theoretical physicist at the Federal University of Alagoas in Maceió, Brazil, who was not involved in the study.</p>
<p>Biologists had long thought that animal foraging was dominated by random walks. But in 1996 a team led by Viswanathan reported that wandering albatrosses, fitted with radio-tracking devices, made the occasional long flight that is the hallmark of a Lévy pattern.</p>
<p>Soon, biologists were reporting Lévy behavior in everything from deer to bumblebees and speculating how it might drive human migrations or the spread of genetically engineered crops. But many of those studies were flawed, says David Sims, a researcher at the Marine Biological Association of the United Kingdom in Plymouth. “Patchy data could mean you think you have a Lévy flight when you haven’t,” he says. And in 2007, researchers debunked the original 1996 albatross paper by noting that many of the reported “Lévy walks” — in which the birds’ transmitters remained dry, supposedly during extended flight — actually were birds resting on their nests.</p>
<p>Now, however, Sims and his colleagues say they have firm evidence for Lévy behavior in 14 species of open-ocean marine predators, including tuna, swordfish, marlin and sharks (although not great whites). The key is the sheer amount of data, on depth and location, gathered by electronic tags, says Sims. His group collected more than 12 million data points describing how the animals swam in the ocean over 5,700 days.
</p></blockquote>
<p>I've mangled the Travelling Salesman Problem, and gone off on a tangent about how sharks statistically roam for food. But there may be a shred of hope in counting on living organisms to solve computationally intractable problems like the TSP. While doing a little leg work early this morning, I came across an intriguing section of the <a href="http://en.wikipedia.org/wiki/Travelling_salesman_problem#Ant_colony_optimization">TSP Wikipedia page</a>. Marco Dorigo, outlined a heuristic method of solving the problem by simulating ant colonies (Ant Colony System or ACS). This field of study is called <a href="http://en.wikipedia.org/wiki/Ant_colony_optimization">ant colony optimization</a> and it has produced near-optimal solutions to the TSP.<br />
<a href="http://en.wikipedia.org/wiki/Ant_colony_optimization"><img src="{{ site.url }}/assets/2011/03/600px-Aco_TSP.svg_.png" alt="" title="600px-Aco_TSP.svg" width="500" height="200" class="aligncenter size-full wp-image-7970" /></a></p>
<blockquote><p>
It models behavior observed in real ants to find short paths between food sources and their nest, an emergent behaviour resulting from each ant's preference to follow trail pheromones deposited by other ants.</p>
<p>ACS sends out a large number of virtual ant agents to explore many possible routes on the map. Each ant probabilistically chooses the next city to visit based on a heuristic combining the distance to the city and the amount of virtual pheromone deposited on the edge to the city. The ants explore, depositing pheromone on each edge that they cross, until they have all completed a tour. At this point the ant which completed the shortest tour deposits virtual pheromone along its complete tour route (global trail updating). The amount of pheromone deposited is inversely proportional to the tour length: the shorter the tour, the more it deposits.
</p></blockquote>
