---
layout: post
date: '2019-05-21T10:00:14.667Z'
title: Model T IndieWeb
tags: IndieWeb Heroku opensource
categories: Commons
comments: true
---
Continuing the discussion of how IndieWeb needs to evolve in order to see adoption.

<!-- more -->

[Chris Aldrich responds to my question "What does a Model T assembly line look like for IndieWeb?"](https://boffosocko.com/2019/05/21/scale-and-scope-jim-luke/#Boris%20is%20asking%20a%20problematic%20question%20not%20remembering%20early%20issues%20with%20the%20Model%20T,%20which%20Jim%20Luke%20reminds%20us%20of%20in%20his%20article:) by first asserting that that's what Twitter and Facebook already are.

So I guess I'll need to explain what I meant by asking that. No, I don't think "Model T Assembly Line" equals Facebook. And one large MicroBlog instance isn't it, either.

How does an end user -- I'll call this person a tinkerer, because you're going to at least need to copy and paste some tech instructions -- deploy a site for just them, that works out of the box? And, where is the list of different "just works" solutions that they can choose from?

> The answer to Boris is that the IndieWeb has been working on the scope problem first knowing that once the interoperable kinks between systems can be worked out to a reasonable level that scale will be the easy part of the problem. Obviously micro.blog has been able to productize IndieWeb principles (with several thousands of users) and still work relatively flawlessly with a huge number of other platforms.  There have been tremendous strides towards shoehorning IndieWeb principles into major CMSes like WordPress (~500+ active users currently) and Drupal (~50+ active users) not to mention several dozens of others including Known, Perch, Craft CMS, Hugo, Kirby, etc., etc.

Plugins to existing systems are great! But: in many cases, the base system has a high technical complexity. I personally wouldn't feel comfortable telling people to run their own WordPress or Drupal instances -- you need hosting experience and security maintenance. So right away that's a relatively high cost.

I've spent quite some time looking at this stuff, especially just recently. I just [added a PR to Pelle Wessman @voxpelli's webmentions server](https://github.com/voxpelli/webpage-webmentions/pull/106) so that it can be one-click "Deployed to Heroku". Pelle wants to go further and have it work in "single user mode", but for now anyone can host their own webmentions server.

Known is the best of the bunch that Chris lists, in terms of being fully integrated and setup out of the box. Except I think you still need to setup [Bridgy](https://brid.gy/) separately? Bridgy seems to do everything that people actually need in terms of communicating with today's social media world, so I don't understand why that functionality isn't baked in to more systems? I originally got Known working on Heroku shortly after it launched (notice a theme?) and it's on my list to set it up this way again.

This "Deploy to Heroku" modality (or [Zeit](https://zeit.co/) or other serverless style) is a simpler, turn key model for both developers and end users. Especially for distributed systems, we can't think in a mode of old school LAMP stack systems where the "user" is hand updating the operating system layer. Even Docker deploys just sort

I want to see distributed systems where users are hosting from mobile phones to Raspberry Pis, and every mode in between. IndieWeb has the right spirit for this, and absolutely needs to work on protocols and interoperability, but it also has an issue where a lot of this code is simply stale.

So: how do we encourage more Manton's and Pelle's to build Model-Ts that are one-click-deploy simple for both tinkerers and other developers?