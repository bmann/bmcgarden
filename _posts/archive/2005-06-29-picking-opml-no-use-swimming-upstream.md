--- 
layout: post
title: "Picking OPML: no use swimming upstream"
created: 1120095289
categories: 
- Personal Publishing
---
<p>Ross is <a href="http://www.bmannconsulting.com/node/1491">thinking OPML</a> with respect to Tucows' new Skydasher product. He's worried if he's making the right decisions:</p>

<blockquote>No use swimming upstream. I just wish that this course had been this clear two years ago when I last had to make this decision - and I pray that the decision is equally smart two years from now when I look back on today.
<cite><a href="http://www.byte.org/blog/_archives/2005/6/29/984158.html">Random Bytes by Ross Rader: Skydasher gets OPML</a></cite>
</blockquote>

<p>Well, we run with the standards (whether proper spec or running code), prior art, and market direction as we can. Me, I still depend on open APIs and interfaces among loosely coupled systems ruling the day.</p>

<p>By the way, if a slogan for RSS is "suck my feed" or "feed me", what's the slogan for OPML? "Play with my hierarchy" doesn't have much of a ring to it. I nicknamed <A href="http://www.scripting.com">Dave Winer's</a> product -- The OPML Editor -- to be called "TOE". So..."play with my toes". I like it :P</p>

<p>Related to the adoption of formats, Tristan Louis left a <a href="http://www.bmannconsulting.com/node/1500#comment-13774">comment</a> pointing to a <a href="http://www.tnl.net/blog/entry/RSS_and_Media:_Can't_we_all_just_get_along?">suggested merge of Yahoo's Media RSS and Apple's iTunes extensions</a>. It's too early to bet on either one, so we have to support both for now.</p>

<p>I keep hearing people complain about different formats. Well, it certainly is an issue from a user perspective, seeing a giant row of "chiclets" pointing to slightly different feeds. But from a dynamic system perspective, it's all sitting in a database anyway, so it's fairly easy to spit out a couple of different kinds of formats.</p>
<!--break-->
<p>Is the answer better auto-detection? i.e. stick it all in the head, and let the requesting application figure it out? Some sort of uber-subscribe protocol? Don't know, we'll just have to make it through these rocky in between times.</p>
