--- 
layout: post
title: Developer's notebook
created: 1065547140
categories: 
- Drupal
---
Dave was getting mad that <a href="http://www.bmannconsulting.com/image">images</a> were being included in the <a href="http://www.bmannconsulting.com/tracker">recent items</a> page -- since I was often posting multiple images to go with one story, it was hard to see where the actual story was.

The tracker.module doesn't have configuration options for this (yet -- I've added a <a href="http://drupal.org/node/view/3532">feature request</a>), so I just added a quick hack which skips adding the item if it is of type "Image".
<!--break-->
I actually had to implement this <a href="http://www.phenomenalsolutions.com">for work</a> -- we're going to experiment with using our blogs (the ones that are part of <a href="http://www.bmannconsulting.com/node/add/blog" title="Create your own blog entry">every user account on Drupal</a>) as a type of internal log. We already have a couple of different ways of sharing information, including email and <a href="http://www.phpcollab.com">PHPCollab</a>, but it seems like there is a need for the kind of transient stuff that blogs seem to be good at: snippets of text, interesting web sites, applications, statistics, etc. Of course, this is private stuff, so we don't want it out in the open...hence, filtering new blog items from the tracker page.
