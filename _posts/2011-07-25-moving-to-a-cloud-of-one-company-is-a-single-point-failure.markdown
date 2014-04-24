---
layout: post
status: publish
published: true
title: Moving to a Cloud of One (Company) is a Single Point Failure
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9773
wordpress_url: http://www.victusspiritus.com/?p=9773
date: '2011-07-25 06:50:08 -0400'
date_gmt: '2011-07-25 13:50:08 -0400'
categories:
- Uncategorized
tags:
- web/tech
- social web
comments: []
---
<p>Now while the following story by Dylan M. (@ThomasMonopoly) appears to have fabricated several facts (Matt Cutts shares some insight on HackerNews), it's worth revisiting how many digital eggs you put into one basket. My issue is not with the veracity of the events, but in how plausible they are.</p>
<p>The following is the introduction of the letter from Dylan to Google:</p>
<blockquote><p>
Dear Google,</p>
<p>I would like to bring to your attention a few things before I disconnect permanently from all of your services.</p>
<p>On July 15 2011 you turned off my entire Google account. You had absolutely no reason to do this, despite your automated message telling me your system “perceived a violation.” I did not violate any Terms of Service, either Google’s or account specific ToS, and your refusal to provide me with any proof otherwise makes me absolutely certain of this. And I would like to bring to your attention how much damage your carelessness has done.</p>
<p>My Google account was tied to nearly every product Google has developed, meaning that I lost everything in those accounts as well. I was also in the process of consolidating everything into my one Google account.<br />
...<br />
Why anyone would entrust anything to “The Cloud” after what I have gone through is completely beyond my ability to comprehend.<br />
<a href="http://www.twitlonger.com/show/bt2p2o">source</a>
</p></blockquote>
<p>The author (if he is Dylan M.) goes on to describe the enormous dependence they have on Google products including contacts, synched bookmarks, docs, email, and reader, as well as how they migrated companies they worked for towards Google services and convinced friends to create Google accounts.</p>
<p>A worst case scenario is painted about account loss. Well it's not quite a worst case scenario, at least the company doesn't free up that identity for reuse immediately. Imagine having your accounts deleted and someone else legitimately receiving all email intended for your eyes only faster than you can hunt down and change all your contact information on dozens of services. That would suck, and I'm confident Google doesn't re-release identities that quickly. If or when they ever do, it's certainly not instant.</p>
<h2>The Face of Google does damage control on Hacker News</h2>
<p>Matt Cutts is a genuinely nice human being that I think of as the number one PR guy of Google even though that's technically not his job (he wages a war against web spam and promotes search quality). It's difficult not to like his relentlessly positive demeanor<sup><a href="#notes">1</a></sup>. In fact in the years I've been following Matt, the only time I remember even slight frustration in his writing or voice was when he talked with a representative from Bing search over copying Google's results, and even then Matt was pretty calm.</p>
<p>To get a sense of community reactions to account locking, let's turn to HackerNews (Reddit is another great source of feedback):  </p>
<blockquote><p>
<a href="http://news.ycombinator.com/user?id=endersion">endersion</a><br />
1 day ago | link</p>
<p>Regardless of the circumstances surrounding the termination of this individuals account, he still brings to light some very valid concerns.</p>
<p>I'll quote terryb088 from reddit in saying, 'The whole "cloud computing" model that companies like Google are pushing requires that we place good faith in the companies that provide these services. In my opinion good faith runs both ways, and any suspension of services needs to have a channel for dispute and resolution.'</p>
<p>The bottom line is, with so much of our personal information and other material invested in Google and its services, the opportunity to appeal (much less be given a reason for) account termination should always be available. It speaks volumes of Google's attitude towards its users that there is not such an avenue already provided.
</p></blockquote>
<p>the discussion </p>
<blockquote><p>
<a href="http://news.ycombinator.com/user?id=Matt_Cutts">Matt_Cutts</a><br />
2 days ago | link | parent | flag</p>
<p>I talked to the person with this complaint, then looked into it myself. The account was suspended for a violation of our Terms of Service. After digging into the situation, my personal opinion is that Google took appropriate action. I'm sorry that I can't go into more detail.</p>
<div class="i1">
<a href="http://news.ycombinator.com/user?id=jellicle">jellicle</a> 1<br />
day ago | link</p>
<p>Cutts, Google still doesn't understand the problem here.</p>
<p>Let's say I decide I have to break up with my live-in girlfriend, for good and sufficient reason. Perhaps she banged my three best friends, perhaps she literally killed my dog with an axe. Doesn't matter - I have my reasons. I break up with her. I still have to give her back her stuff from my apartment. If I don't do so, I'm committing a separate offense of my own. I lose the moral high ground.</p>
<p>Maybe something has to be worked out - maybe a friend of hers has to come over and get it, maybe I put her shit in boxes out on the porch.</p>
<p>Whatever. I still have to give her back her stuff. The courts agree, public opinion agrees, the police agree. Whatever she did, no matter how egregious the violation, my swiping her stuff is FUCKING FROWNED UPON and is not justified by whatever harm she did to me.</p>
<p>Google demonstrates no knowledge of this legal and social norm. That's what is pissing people off. Implement a system to let people download their data from closed accounts and you can delete accounts with no explanation all day long.</p>
<p>Stealing people's data - regardless of what they did to you - is something that most people consider to be evil. Nobody cares about whether the guy did anything wrong or not. He's seizing the moral high ground from you because you, also, have committed a wrong.
</p></div>
<div class="i2">
<a href="http://news.ycombinator.com/user?id=ptman">ptman</a> 1 day ago | link</p>
<p>Physical objects can only be in one place at a time. Data on the other hand can be backed up while it is still being used by the service. And Google collects information about how to do this for their services in one place: the Data Liberation Front http://www.dataliberation.org/
</p></div>
<div class="i3">
<a href="http://news.ycombinator.com/user?id=cynope">cynope</a> 1 day ago | link</p>
<p>It is not realistic to expect all users to continually make backups of all their Google services.</p>
<p>It is however realistic for Google to solve this by putting a violating account in a "read-only" mode, where you are able to export all you data and not do anything else.
</p></div>
<div class="i4">
<a href="http://news.ycombinator.com/user?id=Orbitrix">Orbitrix</a> 19<br />
hours ago | link</p>
<p>Yes it is realistic to expect all users to continually make backups of their Google services. Maybe google just hasnt made it easy enough yet... but that is what the goal should be.</p>
<p>Allowed access to banned accounts in "Read-only" mode is ripe for abuse by spammers and phishers who could benefit from still being able to access information in the violating accounts. Its the wrong kind of solution to a problem that really comes down to personal responsibility.</p>
<p>I think most people know deep down the responsible thing to do is have backups of all their important data... the cloud is just making people lazy. And providing a "read-only" access to a banned account will only make people lazier and more apathetic about it. "oh.. no worries..Googles got my back" But what happens when Google is hacked, or suffers a natural disaster, or other catastrophic failure? It only serves to make the problem worse. Losing your data, to even a wrongfully banned account, is nobody's fault but your own.</p>
<p>There so many more reasons to backup your data before something bad happens, not after.... thats what we should be promoting
</p></div>
<div class="i5">
<a href="http://news.ycombinator.com/user?id=cynope">cynope</a> 18<br />
hours ago | link</p>
<p>Any improvements in exporting data from a Google Account that will make a daily backup actually doable are welcome. But Google should not place all responsibility in the hands of the users, since this inevitable will result in bad user experiences and therefore bad publicity.</p>
<p>Regarding spammers and phishers, these are users violating the law and they of course have no legitimate claims to their account data.
</p></div>
<div class="i3">
<a href="http://news.ycombinator.com/user?id=josecastillo">josecastillo</a><br />
1 day ago | link</p>
<p>"Users should be able to control the data they store in any of Google's products. Our team's goal is to make it easier to move data in and out."<br />
This philosophy, or at least the "out" part, should apply doubly after someone's account is terminated in this manner. Google has determined that sinning against one service warrants terminating access to other services. That may be justifiable. But sinning against one service should not warrant loss of one's data in other services.
</p></div>
<div class="i4">
<a href="http://news.ycombinator.com/user?id=Locke1689">Locke1689</a><br />
1 day ago | link</p>
<p>No. The ToS applies to all Google services.</p>
</div>
<div class="i5">
<a href="http://news.ycombinator.com/user?id=tarandeep">tarandeep</a><br />
1 day ago | link</p>
<p>https://plus.google.com/u/0/104600580124930283388/posts/QBFa... He has<br />
access to Dashboard #liar
</p></div>
<div class="i6">
<a href="http://news.ycombinator.com/user?id=Locke1689">Locke1689</a><br />
1 day ago | link</p>
<p>4.3     As part of this continuing innovation, you acknowledge and agree that Google may stop (permanently or temporarily) providing the Services (or any features within the Services) to you or to users generally at Google’s sole discretion, without prior notice to you. You may stop using the Services at any time. You do not need to specifically inform Google when you stop using the Services.</p>
<p>4.4     You acknowledge and agree that if Google disables access to your account, you may be prevented from accessing the Services, your account details or any files or other content which is contained in your account. </p>
<p>I have no knowledge of what services he can or can't access, just that it is within Google's purview to remove access to all Google's services.</p>
<p>P.S. This is not Twitter and we don't use hashtags in our posts.<br />
Please act as though you have a semblance of decorum.
</p></div>
<p><a href="http://news.ycombinator.com/item?id=2795465">HackerNews source for both quotes</a>
</p></blockquote>
<p>We can see the divide between folks who believe in access to data after account termination versus those who feel clients should regularly back up everything. As one user of Google's services, if I could regularly backup all the information I create and store with Google's data centers, I'd have far less need of their account services.</p>
<p>I'd much prefer to use Google strictly as an anonymous data filter knowing only an absolute minimum about my true identity and simply providing an agnostic data service (email filtering, search, social dial tone). Right now Google is the centralized keeper of the vast majority if it's users digital identities. This is something a distributed network like the Internet is designed to prevent.</p>
<p>Related Posts:</p>
<ul>
<li><a href="http://www.victusspiritus.com/2011/07/20/anonymity-isnt-allowed-on-google/">Anonymity isn't allowed on Google</a></li>
<li><a href="http://www.victusspiritus.com/2011/07/22/how-much-do-you-rely-on-someone-else-for-your-digital-identity/">How much do you rely on one source for your digital identity</a></li>
<li><a href="http://www.victusspiritus.com/2011/07/23/derek-sivers-dont-punish-everyone-or-why-rules-based-systems-are-flawed/">Don't Punish Everyone, or why rules based systems are flawed</a></li>
</ul>
<p><a href="#notes" id="notes">Notes:</a></p>
<ol>
<li>As an aside, the next time I have need of a super villain for an rpg or story, I'm going to base it on a dark facsimile of Matt Cutts with a sinister side ;)</li>
</ol>
