---
layout: post
title: "The New Hack Stack"
description: "Shared hosting sucks, LAMP is waning, new projects start on PaaS with Python, Ruby, or Node"
categories:
- Web Development
tags:
- LAMP
- Github
- PaaS
- Ruby
- Python
- Rails
- Flask
- Node.js
- web hosting
- git
---

In the past, the starter stack for web programming was <acronym title="Linux, Apache, MySQL, and Perl/PHP/Python">LAMP.</acronym> The 'P' originally stood for Perl, and then became mainly PHP.

Today, with $5/month shared web hosting and thousands of PHP-based scripts & applications, this success is hard to argue with.

But the truth is, managing even a shared hosting account is hard, never mind an entire VPS. You need to know the OS, the web server, the language, and the database.

Revision control? Especially because of PHP's ease of deployment and editing, revision control is an advanced topic. This leads to things like "just edit it on the server", lack of updates, and even lack of upstream contributions.

So what do we teach beginners? what is the stack we should be promoting to web makers?

I think the new hack stack is already here. Git, Ruby or Node, and a PaaS for hosting.
<!-- more -->

## Revision control as best practice

Git - and more specifically, the social community around GitHub - teaches both revision control, working together on code, and the concept of contributing back.

Rather than teaching revision control as an advanced topic, we should teach it as a best practice from day one. Part of the kata of code should be your own local commits. this also means you have a built in safety net from 'wrecking' or 'screwing up' your code that causes anxiety for beginners.

The availability of graphical clients for Git that are highly visual and actually quite friendly to use is another bonus. Even Windows users now have a great option in the [GitHub for Windows client](http://windows.github.com/).

## Ruby and Node are the new 'P'

I am singling out Ruby and Node as beginner choices for several reasons.

One is clearly momentum. Ruby, and more specifically, the Rails framework, has gained huge mindshare and usage. Node has also been getting lots of mindshare, although the use of JavaScript and the evented model takes some getting used to.

Both Ruby and Node have strong package / library management. Finding and installing various features into your app is easy and fun.

Setting aside the install / setup of your initial environment, both do a great job of running locally. And this is built into the frameworks, and not a matter of configuring 2 or 3 other servers to get your code working.

### Why not Python?

Python might rightly take its place as the third member in the middle of the stack. But my feeling is that it doesn't have the same 'beginner mind' community as do Ruby and Node. This is likely because Python is an older language and has much broader application than being focused on web programming.

I think this is easily fixable with some blog posts, tutorials, and evangelism. Perhaps something the Django community could focus on.

## The Power of PaaS

The different platforms often tout auto-scaling or various other performance-related features. but ease of deployment and no configuration required is what makes them perfect for beginners.

I remember having a [Twitter discussion with Anil Dash](http://www.exquisitetweets.com/tweets?eids=mu7TPZom7M.mu74IKsZQy.mu76XdSsXR.mu8icylqym.mu8FPSPG7F.mu8O33Cj2y.mu8M5Z6qqH), trying to explain that I thought that focusing on PaaS as the beginner option was a better choice than the pain of shared hosting. Specifically, my main point was:

<blockquote class="twitter-tweet" data-lang="en" author="@bmann">
	<p lang="en" dir="ltr">…the mythical non-technical user who installs on shared hosting will usually get their fingers burned</p>&mdash; Boris Mann (@bmann) <a href="https://twitter.com/bmann/status/167025460759371776">February 7, 2012</a>
</blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

I, personally, have now completely moved away from running any servers whatsoever. This could be seen as a downside – I can't install arbitrary bits of scripts. But, I __can__ deploy self-contained chunks of code / services as separate apps, which is arguably a better practice in any case.

I've had great experiences with [Nodejitsu](http://nodejitsu.com/) and [Heroku](http://heroku.com). With something like AppFog supporting even PHP apps (they've got a [JumpStart program](http://blog.appfog.com/announcing-express-jumpstarts/)), the benefits of PaaS can be applied to those apps which would have required shared hosting or a VPS in the past.

## Hacking for beginners

The new hack stack makes it incredibly easy for beginners to get started to write their own custom apps. There are easier ways to get a CMS-powered website up and running, but for writing code with custom functionality from scratch, it's hard to beat the killer combos of GitHub, Node or Rails, and a PaaS to host it publicly.
