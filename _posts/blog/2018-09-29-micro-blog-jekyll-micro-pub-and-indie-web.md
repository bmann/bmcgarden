---
layout: post
date: '2018-09-29T18:24:04.304Z'
title: 'MicroBlog, Jekyll, MicroPub and IndieWeb'
tags: indieweb micro.blog micropub jekyll
mf-mp-slug:
  - microblog-jekyll-micropub-indieweb
slug: micro-blog-jekyll-micro-pub-and-indie-web
---
As part of my dive back into open source, I took a look at my blog, social networks, and other tools I'm using.

Well, maybe that's not quite true. I've been tinkering with my blog for 16 years, I doubt I'll ever stop, regardless of how I'm spending my time!

## Twitter all the things

I've stopped using Facebook, Tumblr, Medium, and Instagram and doubled down on using Twitter for my "whole self". Which in my case means posting cooking storms, long threads on travel, as well as lots and lots of tech.

For this post I'm not going to get into why I'm off other platforms. With Twitter, I've always seen it as of the web, at the very least -- a link for every post. And, thanks to a long ago setup, I have an [automatically updated archive of all my tweets](http://tweets.bmannconsulting.com/).

Twitter once again made changes to their API for third-party apps. I've used Tweetbot for years with aggressive filtering to make using Twitter much much better. And Tweetbot still does that, but I'm worried for when that's no longer possible.

And then Twitter locked my account and wanted to send an SMS to my Canadian number while I was in the US.

And that was a good reminder that that I should work on being less dependent on Twitter[^twitter-failure] as well.

[^twitter-failure]: There's a whole other story about how Twitter's usernames are the de facto global namespace linking offline to online. I consider this a personal failure, as there was a window in time where these systems might have been at least federated rather than in one single commercial system, and I was working on bits and pieces of identity at the time.

## Using MicroBlog

I've had my eye on [MicroBlog](https://micro.blog/) for a long time. I reserved the handle [@boris](http://micro.blog/boris) there right at the beginning, but didn't do anything with it.

I have great admiration for [Pat Dryburgh](https://patdryburgh.com) and saw him working on a Jekyll theme and [using MicroBlog](https://micro.blog/pat) so all his content is on his own site.

MicroBlog is free to use. You sign up and then link in one or more feeds, either RSS/Atom or JSON, and it will publish these to your timeline, linking back to the original. It's centralized in its namespace, but aggregates content.

You can pay for a few different things. If you don't want to run your own blog, MicroBlog will run one for you. What I pay for is cross posting, which is only $2/month. This enables, on a per feed basis, linking in your Twitter, Medium, or LinkedIn accounts, and posting content to them. Facebook Pages are supported, but I haven't been able to get that working, and that isn't really what I want to spend time on.

## Jekyll and Git

Since I use [Jekyll](https://jekyllrb.com/) for my blog, all of the content is text/HTML/Markdown files. I store them in Git, and have used a variety of tools to generate and serve up the static HTML site.

Currently I have the blog source in a private repo on GitHub and use a free account on Netlify to build and serve it[^colophon].

[^colophon]:My [colophon](https://blog.bmannconsulting.com/colophon) has documented my blog travels over the years.

But, with a static site, I need to run a separate server if I wanted to accept short posts on mobile. Specifically, with MicroBlog's iOS client, it talks to either a Wordpress site or to anything that can accept Micropub[^micropub] posts.

[^micropub]: The [IndieWeb site talks Micropub](https://indieweb.org/Micropub), which is in fact a [W3C Recommendation](https://www.w3.org/TR/micropub/). It's been a while since I paid attention to this -- great to see the spec matured and formalized.

## Microglue

I talked to Pat, who was already doing interesting things with podcasts and Git to get things on MicroBlog, about what a little Microglue server would look like.

I'd want it to run on Heroku, talk to the GitHub API, understand Jekyll front matter and markdown, and speak Micropub.

I wrote this up as a [series of issues in a GitHub repo](https://github.com/bmann/microglue) with feedback from Pat, intending to place a couple of bounties. Time passed, I added a large BorisCoin[^boriscoin] bounty via [Gitcoin](http://gitcoin.co), and then had [ozkan leave me a note about an existing implementation](https://github.com/bmann/microglue/issues/1#issuecomment-425262713).

[^boriscoin]: My experimental Ethereum token.

## Rube Goldberg IndieWeb

And so I dove into Pelle's [webpage-micropub-to-github](https://github.com/voxpelli/webpage-micropub-to-github). He pretty much wrote it exactly how I had hoped to have such a thing built.

It's built in Node and has a _Deploy to Heroku_ button which can get you up and running in minutes.

Of course, minutes turned into _slightly_ longer as I worked on getting the entire IndieWeb toolchain configured and setup on my blog and various other places.

I documented the process in a [Github issue](https://github.com/bmann/microglue/issues/5#issuecomment-425662101) and will likely fork Pelle's code so I can experiment, bounty some issues, and generally make it work for me. And then contribute fixes upstream of course!

## Is it working?

Since I was using live accounts for all of this, various messages made it through to different systems.

This one [made it to twitter](https://twitter.com/bmann/status/1045576992270295040):

> I may quite possibly be posting this via [micropublish.net](https://micropublish.net), to my own micropub server on Heroku, which turns it into Jekyll compatible md file and posts it to Github, which sends it to Netlify, which creates a feed for MicroBlog.

Which got me a ["Saw what?" from @jimgroom](https://twitter.com/jimgroom/status/1045577439752196097).

But my favourite was the ["It's past midnight, is it working yet?"](https://blog.bmannconsulting.com/26600/) which made it all the way to [Medium](https://medium.com/@bmann/its-past-midnight-is-it-working-yet-430789104731) and [LinkedIn](https://www.linkedin.com/feed/update/urn:li:activity:6451342693070176256).

## Next Up

I'm now trying out a bunch of [MicroPub Clients](https://indieweb.org/Micropub/Clients), and also documenting that in [issues](https://github.com/bmann/microglue/issues?utf8=✓&q=is%3Aissue+label%3Amicropubclients+).

I'll turn a bunch of these things into issues and see how much farther I get.

I don't have the MicroBlog iOS client working yet, and neither is the [OwnYourGram](https://ownyourgram.com/) site (which is really great for walking you through every step of getting your IndieWeb / MicroPub setup). Both need some upgrades to the server to work with media handling.

I also need to share the micro and full JSON feed templates that I made for Jekyll to syndicate to Microblog with. Stay tuned, and perhaps I'll have time to actually organize a fun IndieWeb meetup in Vancouver soon.
