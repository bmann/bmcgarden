--- 
layout: post
title: "First feature: Silent Auction"
created: 1275890252
categories: 
- Drupal
tags:
- git
- Github
- Features
- silent auction
- exportables
---
<p>
	I finally got around to making a &quot;real&quot; feature rather than just playing around with the functionality.</p>
<p>
	I had left a comment a while back on <a href="http://ruk.ca/content/how-run-a-silent-auction-using-drupal">Peter Rukavina&#39;s post &#39;How to run a silent auction using Drupal&#39;</a> about how this would be perfect as a feature. So, I installed a new site, grabbed the necessary modules, and turned Peter&#39;s description into a silent_auction feature.</p>
<p>
	The code is available from my (also brand new) <a href="http://github.com/bmann/Silent-Auction/">Silent Auction Github repo</a>.</p>
<p>
	This was a very easy process. I&#39;m familiar with Drupal site building, so I point and clicked my way through the content type and manage fields screens as the main component of the project. Peter did a very good job of documenting the steps he took, so it was easy to do.</p>
<p>
	I then added his custom code to the silent_auction.module file to override comment displays. I didn&#39;t quite complete the &quot;amount raised&quot; block - my buggy custom block code needs some help, Github collaborators welcome :P</p>
<p>
	This was also my first experience sitting down and getting into git / <a href="http://github.com">Github</a>. It&#39;s pretty amazing how great the experience of git is when you&#39;re having your hand held by Github.</p>
<p>
	The nice thing to see about features like this is that it supports a builders point of view: a certain way of building something - no user signups / accounts, using comments as bids directly, etc., plus the choice of certain modules to put it together.</p>
<p>
	Node to node relations, making a full module, enabling paypal, requiring user accounts -- all are different ways one COULD choose to build a silent auction feature. If such a silentauction.module were to be built, we&#39;d surely find a simple_silentauction.module not far behind.</p>
<p>
	Features nicely encapsulates a starting point, but with overrides being as easy as changing a few settings, it makes it simple to continue the lego block building tradition of Drupal, as opposed to the much heavier full module or full install profile. Nice!</p>
<p>
	Now, where do I go to bang people over the head to make sure all their contrib modules are exportable&hellip;</p>
<p>
	Useful links:</p>
<ul>
	<li>
		Direct download of silent auction master branch code: http://github.com/bmann/Silent-Auction/tarball/master</li>
	<li>
		<a href="https://community.openatrium.com/documentation-en/node/449">How to Build a New Feature</a> - this has extended information for making an Open Atrium specific feature, but the basics are still there, especially the non-UI methods for making a new feature.</li>
	<li>
		Demo site: http://silentauction.bmannconsulting.com</li>
</ul>
