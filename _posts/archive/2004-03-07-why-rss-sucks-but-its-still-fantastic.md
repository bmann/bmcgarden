--- 
layout: post
title: Why RSS sucks, but it's still fantastic
created: 1078647900
categories: 
- Personal Publishing
- Web Development
---
<p>I guess I've had this thought for a while, ever since I was doing some troubleshooting of <a href="http://www.opensourcexperts.com">OpenSourceXperts</a> RSS feeds. <a href="http://www.davidgalbraith.org/archives/000619.html">David Galbraith</a> talks about it in conjunction with Amazon's new <a href="http://www.amazon.com/exec/obidos/subst/xs/syndicate.html/002-3131536-1614449">RSS listings</a> for products.</p>

<p>The basic problem is that RSS was designed to syndicate a specific sort of data -- basically news and weblogs. Which is great! That is how I can pull in the <a href="http://www.bmannconsulting.com/import/bundle/29">feeds from my friends</a> and display them on my site, and how I can aggregate info from lots of different news sources, and how I can get all the newest info without having to visit hundreds or even thousands of websites one at a time.</p>

<p>But what if, like Amazon, you want to display the price of your products?</p>
<!--break-->
<p>There is no "price" field in the default, plain jane RSS format. So you have no choice but to throw it in with some other info. But price is metadata. It gets more interesting if we can get access to it as a separate field: we can sort by price, we can filter to show "all books under $20", etc.</p>

<p>I say don't worry about it. For everyday use, sites like Amazon will produce RSS feeds that put whatever they want to display for everyone straight into the description field. Anyone that needs/wants more access can parse the "raw XML".</p>

<p>OpenSourceXperts had the same issue: they had all this information about service providers, like their location, their specialties, and their company logos. So they used RSS2.0 and stuck in a bunch of custom fields. Perfectly fine and legal, but completely invisible to all standard RSS readers. I encouraged them to produce "standard" feeds that included everything in the description field that they wanted visible by default, with the custom field available for people that wanted to do parsing on their end.</p>

<p>It's this kind of misunderstanding and wrangling over formats that is holding back further development. To non-developers, non-web experts, it's hard enough to get excited about RSS, aggregation, and personal publishing: let's produce more examples of "cool stuff we can do", more education and evangelism about what some of this new stuff can do.</p>
