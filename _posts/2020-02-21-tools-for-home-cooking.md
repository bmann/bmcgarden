---
layout: post
date: '2020-02-21T10:53:12.210Z'
title: Tools for home cooking
tags: programming heroku ton-zijlstra roland-tanglao hypercard
mf-mp-slug:
  - tools-for-home-cooking-sloan
slug: tools-for-home-cooking
categories:
  - Blog
---
I do write about cooking here, but this is a long post comparing programming to cooking. If you haven't read it already, go read [Robin Sloan's "An app can be a home cooked meal"](https://www.robinsloan.com/notes/home-cooked-app/). Sloan wrote an iOS app for himself, his sister, and their parents, and considers himself a "home cook" equivalent programmer.

Ton and Roland beat me to a write up with their thoughts on the post. I knew as soon as I read the article that they'd both have thoughts on it.

[Roland](http://rolandtanglao.com/2020/02/16/p1-robin-sloan-an-app-home-cooked-meal/) picked out all of the juicy quotes. I'll plus one the first two:   


> In a better world, I would have built this in a day using some kind of modern, flexible HyperCard for iOS, exporting a sturdy, standalone app that did exactly what I wanted and nothing else. — Robin Sloan

Search for a [recent tweet of mine about HyperCard](https://twitter.com/search?q=from%3Abmann%20hypercard&src=typed_query), I found another thread from 2018 that [points at HyperCard plus IPFS plus blockchain](https://twitter.com/bmann/status/1046448784731832320) that is roughly where I'm pointed at these days. Including mobile devices as a creation and deployment platform for apps. And upthread has a quote from @patrickc:

> End user computing is becoming less a bicycle and more a monorail for the mind. — Patrick Collison

This is a call back to [Steve Jobs' computer as bicycle for the mind](https://talk.fission.codes/t/bicycle-for-the-mind-steve-jobs/490).

> In our actual world, I built it in about a week, and roughly half of that time was spent wrestling with different kinds of code-signing and identity provisioning and I don’t even know what. I waved some incense and threw some stones and the gods of Xcode allowed me to pass — Robin Sloan

The developer experience of building software locally, on your desktop or laptop, is very good in 2020. Live reloading, a mobile emulator, debugging tools, your code editor checking things as you type. But as soon as you get to deployment — to launching this thing into the world without turning your screen to show someone else — is an incredibly difficult learning curve, immediately.

Roland's [part 2 commentary](http://rolandtanglao.com/2020/02/20/p1-programming-feels-like-home-comfy-chesterfield/) finds [Eugene Wallingford's Programming feels like home](http://www.cs.uni.edu/~wallingf/blog/archives/monthly/2020-02.html#e2020-02-18T16_00_24.htm):

> Sloan reminds us that programming can be – is – more than a line on a resume. It is something that everyone can do, and want to do, for a lot of different reasons. It would be great if programming “were marbled deeply into domesticity and comfort, nerdiness and curiosity, health and love” in the way that cooking is. That is what makes Computing for All **really** worth doing. — Eugene Wallingford

---

Ton writes [I am the programming equivalent of a home cook](https://www.zylstra.org/blog/2020/02/i-am-the-programming-equivalent-of-a-home-cook/).

> I would never call myself a ‘real’ programmer, or a programmer at all really. Yet, I’ve been programming stuff since I was 12. — Ton Zijlstra

I have a degree in Computer Science, earned in an era where Java and then a few academic programming languages were taught. I graduated with classmates who couldn't really program at all. And so I have the same feeling: Am I actually a 'programmer'?

Talking to [Brooke](https://twitter.com/expede) at our team retreat last week, she learned 22 programming languages in a handful of months.   


As I thought about programming languages, I wasn't really sure which languages I could say I "know", or can actually write new code in from scratch. This will turn into a separate blog post with a little trip down memory lane. Brooke has assured me that if I actually coded full time, I'd be a solid intermediate developer — although mainly because of my systems experience in servers and DNS and general abilities in tracing down error messages with web searches.

Ton included a [lovely picture of he and I home cooking side by side in my old Vancouver apartment](https://www.flickr.com/photos/tonz/2675261471/), way back in 2008.

---

Let's loop back to Sloan's article:

> …my app doesn’t need a login system. It doesn’t need an interface to create and manage contacts. It already knows exactly who’s using it.

He then goes on to reference [Clay Shirky's Situated Software from 2004](https://web.archive.org/web/20040411202042/http://www.shirky.com/writings/situated_software.html) — "Situated software, by contrast, doesn’t need to be personalized—it is personal from its inception".

Sloan (Ton quoted this too):

> And, when you free programming from the requirement to be general and professional and scalable, it becomes a different activity altogether, just as cooking at home is really nothing like cooking in a commercial kitchen.   


If we expect home cooking to happen, we must build tools designed for home cooking. Home cooking from inception.

That gas-powered apartment stove that Ton and I cooked at, it was "designed" for landlords to supply the narrowest, cheapest stove possible to buy.

At the same time, I distinctly remember [The Black Hoof in Toronto](http://theblackhoof.com/) having two electric coil "apartment" stoves as their main cooking implements.

Masterpieces can be made with home tools, but an industrial oven cannot be moved into an apartment. And that's how software is designed and deployed today.   


---

I am supremely annoyed that Drupal or WordPress can't easily be self-hosted by average users: the amount of experience and maintenance required to keep an entire LAMP stack running — and more importantly, secure! — means that you have to pay someone else to host it for you. I consider this to be a failure on my part: I poured a lot of energy into the Drupal code and community so that people could self-host, and self-publish, and blogging and groups and communities arose out of this. And now we're back to needing to pay someone, probably at least $10-$20 per month, just to keep the lights on.

We've been writing LAMP stack applications for 30 years or so. Linux (operating system), Apache (web server), MySQL (database), and PHP/Python/Perl (application code). Some of the initials have changed (NodeJS, Ruby on Rails), but the pattern remains the same: care and feeding from operating system to web server.

I wrote an article called [The New Hack Stack](https://blog.bmannconsulting.com/new-hack-stack/) in 2012. In it, I advocated for Platforms-as-a-Service (PaaS). The provider takes care of maintaining the operating system and the web server, provides plugins for many different add-ons including databases, and then you're left only needing to maintain or update application code.

My particular favourite in this category is Heroku. In my general quest to not have to maintain operating systems or web servers, I've spent a lot of time hacking on open source applications so they can be one-click deployed to Heroku.

I have to give up on some of them: these applications are not _designed_ in such a way that it is easy to deploy them to Heroku. They are designed such that step one is "login to your Linux server, mess around with the operating system, and configure your web server". Perhaps OK for another developer, but _why_ are they designing them this way, to not make it easy for "users" to deploy?!?

I didn't know it at the time, but the design pattern of the [12 Factor App](https://12factor.net/) had just been authored in 2011, by the Heroku founders.   


Not so coincidentally, many of the members of the original Heroku team are doing very interesting things at industrial research lab @inkandswitch, including writing last year about [Local first software](https://www.inkandswitch.com/local-first.html) that goes all the way to insisting that software should work for users locally, under their control.

I can see these new shifts beginning to happen. We **can** build tools for home cooking. But we have to design them that way from the beginning.
