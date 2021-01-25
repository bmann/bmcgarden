---
layout: post
date: '2019-05-19T20:00:14.667Z'
title: Run your own WebMentions
tags: IndieWeb Heroku opensource WebMention
slug: run-your-own-web-mentions
categories: Commons
comments: true
---
I’m continuing down the road of adding Deploy to Heroku support to various apps, and using my site as a test case for [[IndieWeb]] stuff. I went down the rabbit hole today because [infominer was looking at the Jekyll IndieWeb template](https://github.com/infominer33/indieweb), and I found @voxpelli’s WebMention’s server at [voxpelli/webpage-webmentions](https://github.com/voxpelli/webpage-webmentions).

I forked it [bmann/webpage-webmentions](https://github.com/bmann/webpage-webmentions) and got Deploy to Heroku working by just adding an `app.json`.
<!-- more -->
This post is going to be for testing receiving webmentions. More writing / documentation to follow.
