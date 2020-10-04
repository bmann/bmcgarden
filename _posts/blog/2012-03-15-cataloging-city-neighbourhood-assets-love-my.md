---
layout: post
title: Cataloging city neighbourhood assets - Love My Hood
description: A recipe for using Flickr to get citizens cataloging their neighbourhood loves
categories:
- Vancouver
- Open Data
tags:
- Flickr
- hackathon
---
I'm the host at the <a href="http://www.iqmetrix.com">iQmetrix</a> offices today for the <a href="http://opendatahackaton.eventbrite.ca/">Open Data Hackathon</a> put on by <a href="http://twitter.com/jonovision">Jesse Heaslip</a> and company. I'm also a judge at the endy of the day, so I'm mainly hacking on a few things of my own.

<p><a href="http://twitter.com/andreareimer">Andrea Reimer</a> helped pitch the city ideas at the beginning of the day, and will be a judge at the end of the day as well.</p>

<p>One of the ideas contributed by the city was the concept of cataloging a neighbourhood's assets. That is, why do people love living in an area? Is it heritage homes, some cool retail stores, green space, or the proximity of a community center?</p>

<p>In other words, why does someone "Love Their Hood'?</p>

<p>This is the sort of social data that is hidden, and only uncovered by living in an area for a while. The city can use this information to uncover the things and places in a neighbourhood that the residents and visitors care about.</p>

<p>The concept is that people can take a picture of something that people care about in their 'hood, geocode it, and then tag it with "heritage", "retail", "greenspace", etc.</p>

<p>One of the things I suggested was that rathering than building something, to just leverage some existing sources of open data. Since no one decided to run with the idea, here's the concept in leveraging Flickr to accomplish this.</p>

<p>First, Flickr already has an excellent "Places" and geo-coding layer. I'm not sure if all the <a href="http://vancouver.ca/community_profiles/CommunityList.htm">official Vancouver community areas</a> are in Flickr, but you can see an example for <a href="http://www.flickr.com/places/Canada/British+Columbia/Vancouver/Grandview-Woodland">Grandview-Woodland</a> or <a href="http://www.flickr.com/places/Canada/British+Columbia/Vancouver/Downtown">Downtown</a>.</p>

<p>But, just to keep the data as open and re-usable as possible, it's probably best to add a tag for the neighbourhood manually as well.</p>

<p>The last piece is to come up with a list of some common / consistent tags, like those I've mentioned above.</p>

<p>Then, using feeds of searches on Twitter, you can get a list of photos. Flickr makes searches available as both a geoFeed and KML, so it's easy to visualize.</p>

<p>Here's an example search (just containing my photos at the moment) for the "lovemyhood" tag:&nbsp;<a href="http://www.flickr.com/photos/boris/tags/lovemyhood/">http://www.flickr.com/photos/boris/tags/lovemyhood/</a>&nbsp;- that's Max's Deli in the Fairview community.</p>

<p>Want to contribute? Here are the steps in one easy list:</p>

<ol>
	<li>Take a picture of something you care about in your community</li>
	<li>Upload it to Flickr</li>
	<li>Tag it with "lovemyhood", "Vancouver" (your city name), "Grandview-Woodlands" (your neighbourhood community name), and a descriptive tag of what you care about (e.g. "greenspace", "retail")</li>
	<li>Manually geocode the photo if you're using a device that doesn't geocode automatically, and also make sure the photo is under a Creative Commons license that means it can be used. I usually use CC-BY or CC-BY-SA as the "most open" licenses making it easy for individuals and businesses to re-use and share the data.</li>
</ol>

<p>And you're done! I'll leave visualizations and promotion as an excercise for the reader.</p>
