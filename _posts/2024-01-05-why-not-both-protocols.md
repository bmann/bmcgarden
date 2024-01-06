---
title: "Why not both: an ActivityPub Server on an AT Protocol PDS"
date: 2024-01-05, 21:21:56 -08:00
aliases: 
categories:
- Protocols 
tags:
  - ActivityPub
  - ATProtocol
  - standards
---
I missed Berjon’s [ActivityPub Over ATProto](https://berjon.com/ap-at/) when it was published back in November 2023. 

It’s a design provocation of using the two protocols together:

> With relatively little work, we could run ActivityPub atop an AT Protocol PDS.

The little sub heading says “¿Por qué no los dos?”, which of course translates to:

![Why don’t we have both meme little girl](/assets/memes/why_not_both.jpeg)

Well played [[Robin Berjon]]. Let’s make sure to capture the meme origin here in my notes [[Why not both]].

The meat of the article is that both protocols are great in their own way. 

> Both the Activity* standards and ATProto break this siloing in different ways. ==Activity* are built around URLs and can sort of "socialise" more or less anything on the Web, which is great,== but they don't touch the underlying substrate. The expectation tends to be that either you run your own server (which isn't for everyone) or you have to join a federated server, which tends to put you at the mercy of an admin (and, as some people are unfortunately finding out, not all admins are great). ==ATProto, on its side, provides a good initial foundation for an extensible PDS designed around [user agency](https://berjon.com/user-agency/) and [credible exit](https://subconscious.substack.com/p/credible-exit).== This means that your online presence can be custodially hosted (so you need not worry about running a server) but if you don't like your host, you can be guaranteed to be able to take your content elsewhere (verifiably) and nothing will change, you won't even need to update your handle or set up redirection.

(highlights my own)

[[PDS]] stands for Personal Data Server. As an ATProtocol user, I either run my own PDS, or delegate authority to a service to run it on my behalf. But it’s me that’s in control, not an admin. 

So yeah, ~~running my own~~ having control over my own data server that can also talk ActivityPub sounds pretty great. 

There’s a discussion thread about Berjon’s post at the [ActivityPub SocialHub Forum](https://socialhub.activitypub.rocks/t/robin-berjon-running-activitypub-over-atproto/3707/3) and a [mini thread](https://hachyderm.io/@hrefna/111580064413015748) by [@hrefna@hachyderm.io](https://hachyderm.io/@hrefna) who has been digging into AP nuances as well and is a great follow if you’re interested in protocols.

I’ve got concerns about governance for both protocols. Another great Berjon post [[Internet Transition]]

ActivityPub is a finalized spec and is stewarded by the W3C which at its core has large players. Folding in community group commentary is hard. But it’s work that has to be done, and Facebook Meta’s Threads going for interop here is important for everyone, never mind Medium, Wordpress.com, Flipboard, Mozilla, and others. 

I’m more of a fan of the pre-standards body open protocol work that Bluesky is doing with ATProtocol. Here it’s the opposite problem: Bluesky is the only “large” player — who isn’t very large, is very busy running one platform while they also evolve the protocol. The DID:PLC that allows for delegation of accounts needs to evolve into a consortium model. 

My belief is that both protocols offer a path forward for composable, user centric data. Social and messaging and media and moderation are part of virtually all multi-user apps. Building on top of vocabularies and lexicons, re-using a person’s data and social connections, and being able to interop is where the next generation of applications are heading.

I’m the 22nd user on BlueSky. But I also helped found an ActivityPub-centric Canadian co-op, [[CoSocial]].

Why not both?