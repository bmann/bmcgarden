---
title: Digital Garden Transclusion
date: 2024-03-17, 13:33:01 -07:00
tags:
  - BMC
  - digitalgarden
categories:
  - Digital Garden
  - BMC
---
Reading a [post by Rui on his Tao of Mac](https://taoofmac.com/space/blog/2024/03/17/1900) led me down a number of rabbit holes: Cool review of a mini Linux gaming PC! Bazzite gaming Linux distro! [[Universal Blue]] format for desktop distros! All things I read and wanted to both share with others and leave notes for myself.

I use journals to bookmark / share / give an update[^silentblog]. When I use just a regular link rather than making a note, I'm both sharing that link but also leaving it for future me. I might come back later and make a full notes page. For readers of my social cross-posts, they get to go visit the link directly, rather than clicking on the link to me site, and then needing to go off to read the thing they were interested in.

[^silentblog]: funny, I'm now using blog posts as stuff that is a little less public than my journal, because my journal blasts everything to all of my socials. Affordances matter! 

[[Tao of Mac]] is setup as a wiki / digital garden[^readingtao]. I wanted to bookmark [[Bazzite]] for myself locally and reference Rui’s note page but not copy it. [[Transclusion]] would be ideal, but I'm not up for doing an iframe or something quite yet.

I did make a new `transclusion` property in the front matter and stuck the link to Rui's note in there. It's a list, so if [[Bill Seitz]]'s digital garden has a note page for it, or anyone else, I could link to it as well.

Have I looked at this before? Of course I have! [June 2004](https://2023.bmannconsulting.com/archive/2004/06/07/purple-everywhere/)  reblogging [Tim Bray's post on Purple Pilcrows](http://www.tbray.org/ongoing/When/200x/2004/05/31/PurpleAgain) and then [July 2007](https://2023.bmannconsulting.com/archive/2007/07/03/testing-purple/) prompted by a [Les Orchard](https://lmorchard.com) post[^oldbloggers].

Let's quote 20 years ago me on transclusion:

> From Facebook apps to photos stored on Flickr, we want to have all our "stuff" just magically collected together wherever we happen to be, whatever network we happen to be interacting with. Aggregation, sucking this content in, pushing it over there -- all just temporary ways of flowing content around. One that arguably duplicates content and spews extraneous permalinks around. I just want my pictures right here, or I just want to link deep into someone else's posting and pull in a piece of text. And I want the "other end" to know about that inclusion, a gentle ping, yeah, kind of a trackback. That's the Semantic Web to me: where every plain old HTML file is dynamic and intelligent and knows about the links and people that are incoming and outgoing.

I'm not really looking to reach for semantic web tooling today, because the question I'm asking is, what's emerging as the way to indicate that these pages in a digital garden are "equivalent" or "describe the same thing"?

And: how do we easily display such things in a way that communicates this affordance? Where easily means "on a statically hosted website, perhaps enriched by some JavaScript".

This is the part where I should go do a little research of any current stuff on transclusion. But, really, I'm just waiting for [[Noosphere]], and I'll adopt where things end up there.

[[Quotebacks]] are interesting but are focused on quoting, not transcluding. Related, but not quite the same! And, in some ways, quite _atomic_: a chunk of text, rather than a whole page/url.

For now, I'll file this under blog tinkering, and add it to my [[BMC]] TODO list. Stay tuned for another 20 years of linking, transcluding, and generally being in conversation with other people and their writing! 

[^readingtao]: The Tao of Mac blog, written by Rui Carmo, is one of the blogs that have been around for 20+ years that I've been reading and linking to forever.

[^oldbloggers]: Tim and Les are two other 20+ year blog reads.