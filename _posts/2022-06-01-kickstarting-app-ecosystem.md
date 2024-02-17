---
title: Kickstarting an app ecosystem
tags:
  - app
  - enduserprogramming
  - toolsforthought
date: 2022-06-01T21:20:00
categories:
  - Commons
---
I’ve been thinking about kickstarting a couple of different app ecosystems.

I’m going to be a bit vague here, but imagine a tablet like dedicated device. I wrote a post about [using the reMarkable](https://bmannconsulting.com/blog/2021/02/14/remarkable-tablet-first-usage/) — so maybe consider something like that. But more open and a desire to build a software ecosystem around it. If you’re intrigued, ping me and I can tell you more[^preorder].

[^preorder]: Yes I pre-ordered the founder’s edition. 

At the same time, for my own use and generally thinking what I want to see in the world, I’m a fan of end user programming.

Or at least, no code like customization. That could range from Zapier automating getting data from one system into another, or building custom forms, data, and views with Airtable. 

The web technology stack is the one with the lowest bar to entry for custom apps. And even there you immediately need logins and storage to make an app that users can come back to and have some preferences and content tailored for them. 

When thinking about new systems — new interfaces, new devices — how do you get developers to commit?

Actually, even better, how do you get developers — or end users — to _start_?

One way is customization directly. Think MySpace[^myspace]: give people tools to directly customize their environment. 

[^myspace]: Ok, this is an extremely old reference, and one that I personally didn’t experience. The story is that people learned HTML in order to customize their MySpace page.

But is that even the right metaphor? With smartphones, users customize some icons and widgets and background screens. Very much within proscribed parameters. 

To be clear: I think in popular culture, the concept of an “app” is an excellent base layer object. Web apps, mobile apps, I have an idea for an app, what app do you use for that? — and so on, this is very mass market concept at this point. 

So: you should support apps, and developers. User accounts choose which apps to use to customize their usage of the device. Maybe you support some sort of git-repo aka “link” based sideloading, because the lift of going “full App Store” is a lot. Maybe you want to have some app manifest files with required info to get basic info from the developer and for the user. Use a git repo of your own for people to PR in links to their plugins and widgets, and use that as a source for your “App Store” to start. 

What if we think in more basic primitives? What do I want from a reading / processing / note taking device? 

Notes. Links. Images. People. Environment-wide entities.

Pretty quickly you maybe end up taking on the whole complexity of the mess we’re in. At the same time, there’s a lot of stuff and standards out there.

Do I want to sync my contacts to such a thing, so it needs to support CardDAV? Not really, although as we know, every piece of software eventually gains the ability to send email[^pos].

[^pos]: I was thinking about this today when I entered my email address into a point-of-sale machine that sent my a receipt by email. 

But email is maybe an “API that isn’t an API” to consider. Can my device system account be issued multiple inboxes? So I could configure and route all sorts of info — from notes to self to read letter to images — into the system.[^imap]

[^imap]: Or go full IMAP (or [[DeltaChat]]!) and use email as a sync mechanism!

RSS might be another primitive that works as an inbox like thing. 

And since connective tissue tools like Zapier have both email and RSS outputs, creative users can pipe a lot of stuff.  

Bonus: build your own first class Zapier integration that exposes your system primitives as much as possible.

And of course, you need outgoing tools in the same way. Sync is a super power. Export is considered harmful. 

Right. Display layers and canvas and widgets. Being able to target a widget type as a Zapier endpoint for max flexibility. 

The reMarkable has notebooks and pages as its core data metaphors and visual / display metaphors. It has list view or grid view. No dashboards. No clock widget. No histogram of pages created by day / week / year. 

Making some core widget types like lists, galleries, show first N words and then a more link, etc. 

At which point developer-designer-tinkerers[^sitebuilder] can make custom widget display types before they have to make an entire app. 

[^sitebuilder]: there are people in certain code ecosystems — eg the Drupal or TiddlyWiki site builder archetype — who become expert at plugin/widget configuration all with the tools of the system, with perhaps some light CSS and/or JS skills to do customization. But you need the right level of remixable primitives. 

There’s a whole other riff here about building plugins and widgets into OTHER systems. eG build a widget for WeChat-like super App ecosystems, so content from your ecosystem can easily be manipulated inside the super app, and easy content flows in the other direction. 

And I think I’ll end my somewhat context-free stream of consciousness here. Stay tuned!

## Update Feb 2024

I originally [posted this to my Micro.blog June 1st, 2022](https://blog.bmannconsulting.com/2022/06/02/kickstarting-an-app.html).

The device I pre-ordered hasn’t shipped yet. [Tom Critchlow reviewed the reMarkable and made a few suggestions](https://tomcritchlow.com/2024/02/09/remarkable-notes/)