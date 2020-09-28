---
layout: post
title: "The Flickr Question"
description: "Is paying for Flickr still worth it? What self-hosting options are available for photos?"
categories:
- Analysis
tags:
- Flickr
- self hosting
- photos
modified: '2018-08-19T19:50:34-07:00'
---

It's that time of year again, when I face the same question: my Flickr Pro subscription has expired, and I need to pay so that all my photos are accessible online. But maybe I should self host? Is paying for a [Flickr](http://flickr.com) Pro subscription still worth it?
<!--more-->
Don't get me wrong - I think the "Flickr deal" is still fantastic: about $2 per month for unlimited storage of all my photos. From a pure storage perspective, even Amazon S3 would cost me more than that.

Flickr was one of my first loves when it came to online community. When I could finally give the company money, it felt that much better: I was supporting something great by paying for it.

On top of just photo storage, I get a great API, thumbnail generation, maps, tagging, and so on and so on.

Community? Not so much, anymore, although perhaps that's also a function of me taking less photos and more iPhone snaps. I do miss the great community that built up there, but I'm used to the ebb and flow of taste and online fashion. Heck, I'm even [posting to G+ these days](https://plus.google.com/115428955497675100505/posts)!

What options do I have outside of Flickr?

## OpenPhoto

[OpenPhoto](http://openphoto.me) looks promising – and in fact, they [overheard a discussion on Twitter between myself and Darren Barefoot](http://bitly.com/XOsX3M)[^twitterconvo].

OpenPhoto is both a desire by people to self host (own their data), to use their own domains (own their permalinks), and in general not to be beholden to advertising or commercial entities.

But it has a couple of issues. The first is the permalink issue (here's [OpenPhoto's blog post on the subject](http://blog.theopenphotoproject.org/post/10537443380/namespacing-the-web-for-your-photos)). All of that is great - I would much rather have my images available at photos.bmann.ca/photo/1234 than on Flickr or Facebook.

But what a LOT of people love Flickr for, is using it as the place where they upload source images, and then they embed the Flickr thumbnails in their blog. And that's where the OpenPhoto "bug" with their permalinks story is: the thumbnails they generate (and it looks like they only generate one size right now?) are hosted on a separate server with an address that is not your own.

My test site is at [boris.openphoto.me](http://boris.openphoto.me). The original image embedded below is [here](http://boris.openphoto.me/p/1), but the [thumbnail is on the awesomeness subdomain](https://awesomeness.openphoto.me/custom/201211/hidef_bacon-12a74d_870x550.jpg).

<img src="https://awesomeness.openphoto.me/custom/201211/hidef_bacon-12a74d_870x550.jpg" height="275px" width="435px" />

Of course, OpenPhoto is committed to open-ness and hosting your own data, so I assume they'll fix this at some point. This [GitHub issue thread on writing metadata (favorites, comments, etc.) directly into the photo file itself](https://github.com/photo/frontend/issues/680) is a great example of some forward thinking around this.

## Self Hosting
The other issue I have with OpenPhoto is their approach to even writing the software. Or rather, their assumptions.

It used to be that self hosting meant running a Linux box / LAMP stack off behind your own cable or DSL connection. Perhaps a cheap managed server or (more common these days) a VPS of some kind.

But I don't think that's the path forward. The expertise needed to manage the entire stack of an operating system, a web server, a database server, AND the programming language you've chosen is too much complexity.

As I wrote in [The New Hack Stack](https://blog.bmannconsulting.com/new-hack-stack), I see the way forward being <acronym title="Platform-as-a-Service">PaaS</acronym>: choose a programming language, choose a PaaS. The database should be fully managed as well.

In short: I don't want to take a step backward and have to run a full server stack just to have to run OpenPhoto. I'd love to see an alternate approach from the team where a git clone, some basic config file editing, followed by a push to Heroku / Staccato / PaaS of your choice (which probably means ditching PHP - I had to get a language dig in here somewhere!).

Heck, maybe a central photo management app that keeps your account, settings, lets you uploads centrally, but publishes the photos / thumbnails / etc. to relatively flat files on your own storage space on S3, Dropbox, etc. is an interesting way to make this even easier.

## What's the answer to the question?
For now, I'll keep paying for Flickr Pro.

1. It's cheaper than any other storage option
2. No one else has solved the permalink issue
3. I want great user-supported web services to exist

I am not worried about my photos or the portability of the data there: Flickr was one of the very first of the new breed of websites to have a really great API, and there are tons of end user friendly export systems.

I _am_ worried that Flickr will continue to slide along with the rest of Yahoo, but with Marissa Mayer at the helm, all sorts of changes are coming, that on balance look to be good.

I'll keep experimenting with OpenPhoto and other solutions. I really like having my main site on Amazon S3 and this blog on Heroku, and paying for the storage on my own.

You can find me and my photos on [Flickr as boris](http://flickr.com/boris), and on [Instagram as bmann](http://instagram.com/bmann).[^notonflickrorig]

[^twitterconvo]: Originally embedded via Storify, and the content did exist in their ```noscript``` tag in the source for this blog post, but is more easily read on the [Exquisite Tweets website](http://www.exquisitetweets.com/tweets?eids=ud7thVAIXA.uegUTg9g4a.ueg2hHTuj7.uehfZXkoxw.uehAw7FaqP.uehOMmPftC.uehZcNHy6S.ueiGOFa2a4.uej7OtV8vc.uekRK6ympo.uemGfUCsQU.uemNXDwuTk.uesE2wXgEm.ueuO4bp8ge.ue4WIcvKvJ.ue434rRjMW.ugRtyAD9PM.ugRQh6Gvqm.ugTmerFE7M.ugU5wYL4Wi.ug0tL8N3AW), which is what that previous bitly link linked to in any case. That was probably more than you needed to know.

[^notonflickrorig]: And of course, while those links still work, I don't actually put new content on those services anymore.

