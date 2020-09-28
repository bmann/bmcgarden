--- 
layout: post
title: On TrackBack, and Why You Should Smoke Refer Instead
created: 1055459220
categories: 
- Web Development
---
I read <a href="http://daringfireball.net/2003/06/take_your_trackbacks_and_dangle.html">this article at Daring Fireball</a> and was convinced that TrackBack is the devil's spawn. Thinking about it more, I'm not so sure.

There were a couple of tools mentioned that let you do TrackBack-like functions using referrer information, such as <a href="http://www.textism.com/tools/refer/">Refer</a>, or <a href="http://ranchero.com/php/rollingreferers/">Rolling Referer</a> from the creator of NetNewsWire.

In the meantime, <a href="http://daringfireball.net/2003/06/trackback_addenda.html">John Gruber</a> posted an "addenda" which goes into more detail about good/bad uses for TrackBack.

Referrer logs seem to be the better choice. They don't rely on changing the behaviour or installations of people at disparate remote sites, and they are there for you to use already. A referrer-based system will catch people that link as well as people that are purposefully trying to comment/TrackBack.

Of course, it's interesting to note that Drupal/this site automatically show up in the referrer logs for everyone that I have subscribed to. Which means that I often see links in <strong>my</strong> referrer logs from what are obviously people scanning through their logs (because the source URL has something like <a href="http://awstats.sourceforge.net">awstats</a> in it).

In closing, don't let <a href="http://diveintomark.org/public/2003/06/matrix-prank.html">the platypus get you</a>.
