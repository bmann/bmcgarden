---
date: 2021-03-07T17:52:10.268-08:00
title: back-to-indiekit
draft: true
---
# Back to IndieKit

I’m back to using [[IndieKit]] with this site, a personal [[Micropub]] server that lets me publish to the Git repo where the source of this site lives. 

Micropub support means I can use any tool which supports this standard, of which recently there have been more and more. 

Previously there was the MetaWeblog API or AtomPub which lead to an explosion of blog clients. But it also meant passing username and passwords around. Micropub is based on OAuth, and authorizes with your site without sharing a password. 

In fact, [[IndieAuth]] means that my site is what I use for a login. 

But the thing I wanted to enable is posting on the go. While I have been spending a lot of time at my desktop, using my [[VSCode]] or [[Obsidian]] editor apps, I do a lot of reading on my phone. 

I wanted to quickly post a note, bookmark, or journal item directly to my [[SecondBrain]] site.

Running IndieKit as a Micropub server enables this. 

I used [[iA Writer]]’s iOS app to write this post. iA Writer has a [[Micropub]] publishing feature, so with [[IndieKit]] I can publish a note directly to the site.[^notevsarticles]

[^notevsarticles]: The IndieWeb “Articles” type is what I’m mapping to my local “Notes”. So iA posts Markdown articles which are then processed as new notes. Even more confusingly, I expect that I’ll actually sit down and use my desktop editor to turn this into a Blog post.

## Daily Journal Logs

But the main use for posting on the go is to power my [Daily Journal Logs](/journal/).

I’ve gotten used to having a daily work log that I write privately in [[Roam Research]]. Those are private internal notes, meeting notes, and personal TODOs[^personaltodo].

[^personaltodo]: Personal in the sense that they are TODOs that I need to track just for myself: my internal TODO system for work and life. As opposed to a shared TODO system like [[Trello]] or GitHub Issues that I am maintaining with other people.

And I have my [[Micro.blog]] powered personal blog, which I really enjoy. But, every post there gets cross posted to Twitter and Mastodon. 

In the reboot of this site I’ve always had Journals, but they were this weird mix of blog posts and notes.

So I made Journal Logs: smaller pieces of text that are more situated around capturing a thought, a web page, or something to flesh out as full notes and research later. 

I’ve been enjoying it. It’s like [[RSS Club]]: without broadcasting on social, people can [subscribe to these journal logs](/feed/journal.xml), but these posts are very much just little chunks of text out of my brain. I’m writing them **for me**. People are welcome to follow along, but they will likely lack context.

## Bookmarks

Since IndieKit supports many of the different [[Micropub]] post types, I ended up enabling Bookmarks too. 

They are styled a little differently and are a good way to capture links to tools or code. I don’t use Bookmarks for articles or other people’s blog posts — I’ll write a short journal log if I want to do that. 

This is probably the closest to overlapping with my existing Notes, where I do have optional `link` and/or `git` properties. The difference being, they just flow into the Daily Logs and aren’t captured as a first class note, on purpose. 

If I later do more with the Bookmarked item, it can become a full Note. 

## Other Post Types 

I looked at “Likes” as well but that got to be too many items to choose between: should this be a Like or a Bookmark?

Reply, RSVP, and [other Micropub post types](https://indieweb.org/Micropub#Examples_of_Creating_Objects) I’m not planning on using. 

In part because I have to build custom templates for them, and also because of inconsistent support in Micropub clients

## Micropub Clients

[[Indigenous]] for iOS is what I used to use but it is no longer maintained and doesn’t work any more. 

I use [[Gluon]] to post to [[Micro.blog]]... but it’s an Mb client, not a general purpose Micropub one. 

So I use @aaronpk’s web based [[Quill]]. Works great on my phone, works great on my desktop. 

In fact, I use Quill even on my desktop, when I’m a click away from my [[VSCode]] editor that usually has some page on this site open. 

Constrained interface, type a few things, and post. Don’t get distracted by immediately defining all the [[wikilinks]] you just added to the log item. 

I think I might like to build a simple web-based [[Micropub Client]]. I’d like to see more of them, to have people tinker with editing interfaces as much as they tinker with the content publishing & display systems of their blogs.

## On This Day

I might try and implement some sort of On This Day feature. This would be generated when I build the site, so it’s a display format for me: if I make at least one post on a day, my site would pull in any other posts made on that day. 

This one way to be reminded of content on the site, and further extend and refer to it. 

## Errata

I still need to troubleshoot uploading images. There have been a couple of times where I wanted to post a screenshot, which I think would be the main use case. 

I also haven’t figured out full templating. Bookmarks use a `bookmark-of` front matter property, and it would make templating simpler to just use the `link` property I use for notes. 

And feeds. All my feeds need some work I think. 

## Recommending IndieKit

This post is sort of a weird mix of workflow, notes to self, and pointers to the tools I used.

If you’re reading via RSS, you need to read the article on my site to follow the [[wikilinks]] (or hover over them to get a preview).

I configured IndieKit to power this strange journal log system, that works for me when things like Roam Research have them built in. I switched all my personal stuff to Micro.blog because I just wanted to post pictures of food or blog about music. But that just means that this site becomes the place where I experiment!

If you want to tinker with your digital garden or personal blog publishing, I can recommend [[IndieKit]]. It’s a single `index.js` file that runs great on the free Hobby tier of Heroku. My [source code is on GitHub](https://github.com/bmann/indiekit-bmcgarden).

Do you have a convoluted workflow or quirky IndieWeb integration into your site? Tell me about it!


