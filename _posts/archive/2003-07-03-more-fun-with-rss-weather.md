--- 
layout: post
title: More fun with RSS Weather
created: 1057275180
categories: 
- Application
---
I've started tossing some ideas back and forth with <a href="http://laughingmeme.org/archives/000947.html#000947">kellan of Laughing Meme</a> and <a href="http://www.manero.org/weblog/">Tony Collen</a> about RSS feeds for weather information.

The first hurdle seems to be that there is no open XML-based format for weather information. There is one for <a href="http://zowie.metnet.navy.mil/~spawar/JMV-TNG/XML/OMF.html">weather observation</a>, but it's not exactly suited for the consumer end of things -- just basic stuff like city, temperature, conditions, etc. (but of course it gets more complicated than that...).

So, the first goal now has to be to create the XML, then get the data to make the XML (which at this point seems to be screen-scraping one of several government services....my <a href="http://www.bmannconsulting.com/node.php?id=200#379">previous attempt</a> was not looked on kindly by Environment Canada -- hence the Flash monstrosity).

From that XML info, it is relatively simple to transform into whatever you need, including of course an RSS feed. I have a few bits and pieces stored here at my <a href="http://www.bmannconsulting.com/node.php?id=333">RSS Weather</a> node, but if you want to join the conversation, best to head over to the <a href="http://www.quicktopic.com/share?s=DbLb">QuickTopic forum</a>.

<strong>Update</strong>: just changed the QT URL to point to a "shared topics" space instead of the forum.
