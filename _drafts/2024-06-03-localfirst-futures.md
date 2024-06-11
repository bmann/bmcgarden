---
title: Local first software futures
date: 2024-06-03, 07:19:17 -07:00
categories:
  - Blog
tags:
  - localfirst
---
What are some of the ways that Local-first software will evolve?

I had a chat with [Philipp](https://bsky.app/profile/matheus23.com) where he wondered whether a publisher role makes sense for local-first:

> One monetization model for local first apps is actually similar to games: pay once up front, pay another time for the "second release" etc. Thus perhaps Publishers make sense in that system, too.

For starters, I think that local-first is an architectural pattern, and a business model is separate from an architectural pattern. This is the same as talking about software licensing: open source isn't a business model.

I've used the word "app" very intentionally for a long time, because I believe that it's the most well understood term by the mass market. And because of that, this might point towards the concept of an "app store". The role of an app store includes distribution and discovery.

Philipp:

> With games, there's still both Publishers and distribution separate. Publishers help cover up front cost, taking on risk & help with marketing. And distribution (app stores) are already commoditized. It's hard to go against the app or play store. Web distribution is also commoditized

Publishers are less common in (non gaming) apps because it takes less people, less time to build. Effectively, publishers are an investment layer. Why do we think software needs specialized investment?

The SaaS subscription model means one can grow recurring revenue over time. With games, all of the effort is up front, and then only unit sales. There are of course season passes, DLCs, in-game currency, cosmetics, and a host of other gaming specific revenue sources.

While there are various places to get bundles of SaaS software[^setapp], it's relatively rare. App makers go direct to their audience and sell subscriptions as part of their app on the web, or use app stores[^appstores].

[^setapp]: [Setapp](https://setapp.com/) being one example, which is a single monthly subscription for a number of different MacOS & iOS apps.

[^appstores]: Apple app store (both iOS and Mac), Google Play, Microsoft Windows store. I found this [Reddit thread with some comments on the Windows store](https://www.reddit.com/r/dotnet/comments/16tn768/is_windows_app_store_still_profitable_for_an_app/) -- doesn't really seem like much of a channel.

## Local First App Stores

What do app stores have in common? Why are the used? Focusing on Apple and Google Play, those are tied to operating systems. Apple in particular strongly bundles identity, storage, and synch, which app developers can integrate with.

For local first software, every app needs auth, storage, and synch between devices. Right now, we don't have strong leaders in those categories, whether those are commercial services for developers or end users, nor protocols that interoperate.

My mental model of local first software is that it's _not_ just an architectural pattern, but that it contributes to user owned data, and to "automatic" interop. That is, as a user, I can see all my local first files together, and can easily use the same account for many apps.

How is this different than installing desktop apps, where your file system is the interop layer? And your user account is (sort of) tied to your operating system or just not that important.

If local first _doesn't_ end up leading to interop and standards adoption…is it any different than choosing a Rails or Django framework for building? Those two frameworks lead to classic hosted client/server apps, where the developer holds all of the data, and there isn't any interop without actively building and maintaining APIs across all apps.

## Multi Device and Multi User

I think one of the ways that the world has changed significantly when it comes to software, "the cloud", and SaaS is that we have some base expectations:
* apps and app data can be accessed across multiple devices. At the very least, one person's computer and smartphone.
* apps can be shared between multiple people, again with all the same data reflected everywhere

Local-first has some interesting opportunities here. A new feature is that apps can work offline, without an Internet connection constantly connected to a server. 
