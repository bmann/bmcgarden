--- 
layout: post
title: Break your news feed to easily lose readers
created: 1086016814
categories: 
- CMS
- Drupal
- Personal Publishing
- Web Development
---
<blockquote>
<p>It's not the first time I see this, so here is just one advice you may consider to avoid losing those of your readers who will not care following your moving feeds: <a href="http://www.w3.org/Provider/Style/URI">Cool URIs don't change</a>! Changing the URL of a news feed is strictly equivalent to changing the URL of your home page, since the feed URL is actually the site entry point for its subscribers. Would you break your home page like this just because you've changed your content management system? No one in their sane mind would accept that a CMS breaks a home page like this, so why accept it for a news feed? OsOpinion could have changed their backend without changing the feed URL.
<cite><a href="http://www.padawan.info/web/how_to_lose_readers_1.html">padawan.info: How to lose readers (1)</a></cite>
</blockquote>

<p>They could have also just re-directed their newsfeed to the new address.</p>

<p>Little known Drupal feature #1: if you use the built in aggregator, when it goes out to check a feed and finds it has been re-directed, the new feed link will automatically be copied into the database.</p>
