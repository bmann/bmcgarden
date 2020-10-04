---
layout: post
title: "Octopress all the things"
description: "Moving off Posterous and Drupal"
categories:
- Blogging
tags:
- Octopress
- Posterous
- Drupal
---
I need to migrate my [old blog posts off Posterous](http://bmcasides.posterous.com). I need to migrate [my Drupal](http://bmannconsulting.com) off Drupal. All will likely end up here.

Current thinking is that I will run three sites:
<!-- more -->

* __bmannconsulting.com__ - likely to be a simple landing page + a static exported-to-Octopress archive of the current BMC; perhaps hosted on Amazon S3 via rsync
* __blog.bmannconsulting.com__ - runs Octopress, hosted on Heroku (this site); long form posts, project pages, and so on.
* __links.bmannconsulting.com__ - running on Tumblr, high volume links + short commentary

Err… three sites for the main, public "tech" brand of me, which is the 10+ year old bmannconsulting.com domain. I have recently moved [bmann.ca](http://bmann.ca) to Tumblr as well.

I'm going to likely outsource some of the work of moving posts around. I need a Posterous-to-Octopress script. The archive of Drupal posts need to be turned into markdown files as well. Not sure where to put those, might just go onto Github Pages as well.

__Update__: OK, I've got this running nicely. I've got a git checkout out sitting in my Dropbox, meaning I can use [WriteUp](http://bit.ly/writeup-bmann) or [Byword](http://bit.ly/bywordapp-bmann) to create / edit posts on the go. But, I have to be at a computer that has both my Dropbox and the full Ruby stack setup to generate the Octopress files.

So: how do I save updates to Dropbox and then have those updates generated and pushed to Heroku? I'm thinking it involves running another server just to do this and then involve the Dropbox API in some way. Thoughts?

Also, I have a job post on [oDesk to write a Posterous Export](https://www.odesk.com/jobs/Ruby-Script-for-Posterous-Export_%7E%7E2314ad1a303742d2) - if you know anyone that could do this, point them at the listing, or look at [project page](/projects/posterous-export/).

### Update September 2013

This site now runs on [Harp](http://harp.io). See the [colophon](/colophon) for details. _bmann.ca_ (the root domain) is running the [Katana URL shortener](http://links.bmannconsulting.com/link/katana-ready-to-go-heroku-hosted-url-shortener) and [links](http://links.bmannconsulting.com) is running on [Postachio](http://postach.io "Evernote blogging platform").