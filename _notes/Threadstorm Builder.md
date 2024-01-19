I wrote up the design for this many years ago now, when I called it a [Tweetstorm Builder and Blog](https://talk.fission.codes/t/tweetstorm-builder-and-blog/433). I'm copying that write up here.

In our post Twitter era, both [[ActivityPub]] and [[ATProtocol]] would be good choices. [[Micropub]] really isn't widely used and I think tying it more social platforms makes more sense.

[[Noosphere]] could be a fit as well, but also isn't currently social, and I also think they would do well to e.g. post to [[ATProtocol]]. The Noosphere mobile client app, [[Subconscious]], could evolve to be a threadstorm builder.[^threadstorm]

[^threadstorm]: OK OK, this is a terrible phrase, but in my defense, I came up with in 2 seconds when I realized I didn't want to call it a "Tweetstorm" any longer, I will absolutely not say "Tootstorm", and "Skeetstorm" is also incredibly bad. Threads is the more generic cross platform way of what to call these things. Except, for, you know [[Threads.net]] is a thing.

There are a whole bunch of people who have adopted Twitter as their Digital Garden. So as well as being a builder, it should make it easy to transclude (quote post) and generally maintain and weave long running threads over time (mentioned below as a feature).

I say here Twitter in particular (and continue that the below because that’s when it was originally written). How we can we think about this as cross platform, and supporting crossposting?

A variety of platforms ([[Farcaster]]’s Warpcast client is one) support rich embedding of Tweets when a Twitter link is included. What does cross platform quote posts look like?

One of the things we looked at with [[Moa Party]] was translating @-mentions across platforms. This might be a feature for [[Fedica]] to think about supporting: opt-in linking / verification of your accounts across platforms.

Below is the cut and paste of the original.
## Description

People write tweetstorms because they’re “easier” than whatever their blog setup is. And the constraints of 280 characters at a time makes for both careful sentence construction and flow.

But - then you’ve got this lovely writing that is trapped on Twitter. At best, you come back and copy / paste the tweets back into a blog post.

The idea is a blog + tweetstorm builder. You log into it with your Twitter account, compose Tweets, and post to Twitter as a tweetstorm. But, you also get a “blog post” that is generated for you.

## Concept Overview

People still don’t seem to be able to get over the hump of blogging. Twitter helps frame bite sized ideas and gets spread and quoting and interaction.

You might get followers, but you don’t have an easy way to keep or highlight that tweetstorm of yours.

Twitter web client now has tools for making multi-tweet threads. Your one option is to fire them all at once, and you are one browser refresh from losing everything you’ve written. Also: no draft tweetstorms.

The tweetstorm client helps you draft and publish tweetstorms.

Once you publish, it also creates a markdown and/or HTML formatted version of your tweetstorm — aka a blog post. Initially, title and optional header description.

This is a bit like Storify, which used to support arbitrary chunks of text between tweets.

## Features

A Fission app, enabled with login and file storage

Twitter Auth: Auth with Twitter and keep credentials local per session. Have to figure out webnative<->OAuth connection here.

Cut and Paste: cut and paste the markdown or HTML and publish it on your own blog. (use case for atJSON native storage here?)

Choose timing of tweets: all at once or pace them out by X minutes

Personal Microblog: if we’re already generating the HTML for a blog post — just be a blog! For Fission, select a public folder to post to / edit from. Need to set up a separate “blog app” for display if we want a custom domain.

Full Micropub client: why just multiple posts? Make it a full Micropub client, so you can draft/write tweet length posts and post to anything that supports Micropub.

Long running threads: the other emergent behaviour is long running tweet threads. Search tools within Twitter are pretty hard to do, so this is actually difficult to manage. If you keep threads around and searchable / browseable, make it simple to attach / post a new tweet to the end of a thread.

Also: look up Twitter “collections”? Tweetbot has the option to “create a topic”, but also “make it a collection”. Can collections include tweets from multiple users? Make it easier to do this.

Mastodon support: Initially point people at [Moa Party](https://moa.party/), but first-class Mastodon support may be of interest to some. Means OAuth into your home server, which is pretty much just like Twitter. But, longer posts and other Mastodon specific features.

Medium, LinkedIn, Tumblr, WordPress, Drupal etc posting: various things have APIs. WP and Drupal can both accept Micropub with the right plugin. Also, [Micro.blog](https://micro.blog/) can accept Micropub posts, and handle cross posting.

## User Impact

_Who would want to use this and why?_

Anyone that wants to compose tweetstorms in a richer environment while also having it post to their own site.

Blogging, but easier. Twitter promotion, without having to be “on” Twitter.