---
tags:
  - protoapps
---
I’m adopting the term “Protocol Apps” from David Phelps’ [[Proto-App Thesis]].

In short, the thesis says that large, mass market apps that rely on network effects are saturated and it is extremely difficult to break in. The existing large apps are all built on centralized, proprietary platforms.

With Protocol Apps, building on a protocol takes advantage of both network effects (many apps share a pooled set of users and content) and interop (the protocol is the API, allowing for interop, multiple clients, and no risk of centralized platform turning off an API).

## Open Social Protocol Winners

The three [[Open Social Protocols]] that I think are going to be the winners are:

* [[ActivityPub]]
* [[ATProtocol]]
* [[Farcaster]]

## D.R.E.A.M.

Distribution Rules Everything Around Me

As an app developer, getting distribution — getting your app in front of potential users — is the number one challenge. 

Closed social platforms like Twitter or Instagram charge you for APIs and restrict what you can do. Their algorithms are opaque and in many cases you’ll need to pay for ads to promote your app to get installs.

App stores are the same: a proprietary algorithm for search ranking, or pay to be promoted. 

Direct “social” word of mouth is one of the few avenues left for independent promotion and discovery. 

The more your app is multiplayer and has public content, the more building a Protocol App makes sense. 

Either you’re building a proprietary platform that you hope will draw users from elsewhere, or you pick one of the three open social protocols as a core building block for your app. 

## Architecture 

If you’re building an app that is meant to be used by many users at scale, you’re immediately needing to design your app to solve problems that the open social protocols already have answers for. 

For example, how do you make it possible to have users own their data?

For ActivityPub, this would be the ability to run your own server, and built in tools to move between servers. 

With ATProtocol, the [[PDS|Personal Data Server (PDS)]] is part of the architecture. You can run a default PDS for users but they can bring their own by self hosting or delegating to some other PDS provider. 

And Farcaster’s Hubs can be run by anyone, or outsourced to specialized hub hosts like Neymar or Piñata. 

All three have different scaling trade offs. And ActivityPub, being the oldest, also has a number of different implementations in different programming languages. 

There are many more features and social patterns built into these protocols - likes, moderation, data structures, search, indexing etc etc

As a developer, you can lean into these features rather than figuring them out from scratch. 

## Multiple Protocols

Should your app integrate with more than one of these open social protocols?

For simpler integrations where you are running your own classic, centralized architecture, yes: you can build integrations into multiple of these. This is the world we are in today, with “share” buttons or basic automated posting across multiple networks.

But, I’m saying that for certain classes of apps, you may want to fully base your app on one of these three protocols.

Much like picking an app building framework like Django or Rails.

