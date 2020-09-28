--- 
layout: post
title: Purple everywhere
created: 1086595601
categories: 
- purple numbers
- Tim Bray
- Personal Publishing
- Web Development
---
<a href="http://www.tbray.org/ongoing/When/200x/2004/05/31/PurpleAgain">ongoing: Purple Pilcrows</a>:
<blockquote>When everyone from Lauren to Aaron Swartz is whining at me to make the #-marks go away, I have to listen. I&#8217;ve adapted Simon Willison&#8217;s brilliant hack, and a couple of remarks are worth making.</blockquote>

<p>These "purple numbers", where individual paragraphs are able to be linked to, is an interesting concept (I've linked to Tim's post because he has pointed to most of the other interesting discussions around this, and because generally I enjoy his "take" on things). But, since anchors aren't actually first class citizens, I would say that a way to link to (and only display) relevant paragraphs is more useful and powerful. This could also be used for <a href="http://www.usemod.com/cgi-bin/mb.pl?TransClusion">TransClusion</a> -- including content from other places locally. An <code>iframe</code> is an ugly way of doing this -- you would likely need some wiki-like framework to make it possible.</p>

<p>So, you need a dynamic system where you can point to an entire article (e.g. <code>/article-name/</code>), and then a way to get just individual paragraphs (e.g. <code>/article-name/p/1</code>). You could probably do ranges of paragraphs this way as well: <code>/article-name/p/1-3</code>.</p>

<p>The more we link, the more we get enmeshed in other people's thoughts and ideas: I think this is a good thing.</p>
<!--break-->
<p>I like the fact that I found out that the paragraph marker (this may or may not look like one in your browser: &#182; ) was called a "pilcrow" from Tim Bray.</p>
