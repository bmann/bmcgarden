---
title: Setting up a new blog and domain on Micro.blog
date: '2020-07-04T17:39:34-07:00'
tags:
  - blogging
---

I've decided to use [[Micro.blog]] directly for my short form, social posting. I'm happy with Micro.blog's approach to owning your content -- you can take an export of your Markdown content and images and run it in many static site generators. Having my own domain name means in the future I can redirect wherever I need.

I was already paying for simple cross posting, and I've realized that I am posting less in part because of my rather fragile setup.

So the plan is to do short form posts here, and keep long form content (other than posts like this one!) on `blog.bmannconsulting.com`. 

A few notes on setting up a new blog, and getting used to how things work here on Micro.blog (Mb). I'll update as I go, and put suggestions in **bold** for the Mb team:

---

Because of how cross-posting works, I'm going to set things up so I can choose which short form posts get sent to Twitter, LinkedIn, or other places. Each category has a separate feed, meaning you can use the feeds attached to a category to control that cross-posting.

Speaking of categories, I really like tags, where I can create them on the fly as I post. This may actually work with an external Micropub posting service, but in the Mb interface, you only get the categories you previously created.

Even if you're going to use a custom domain name, you need to initially pick a "short" name. I had forgotten that [other Boris](https://boris.micro.blog) is squatting on the `boris` microblog...although I do have the [@boris](https://micro.blog/boris) username. So, `bmann` it is.

I switched over DNS, creating a subdomain CNAME that points `microblog.bmannconsulting.com` to `bmann.micro.blog`. It seemed to be taking a while for Mb to pick up the custom domain. It's quite annoying that you can't save the page, and that the message is a drop down modal, until the DNS is working. I had a hunch, and turned off "Proxying" in Cloudflare, and then Mb saved the custom domain right away. **If your domain is on Cloudflare, turn off Proxying for your Mb CNAME**

I looked at my sample posts I had made. `bmann.micro.blog` was showing in a number of places, including the link to the test post image I made. I edited the post and linked to an off-site image post. This is great: while Mb includes image uploads to make it simple, it's also happy for you to just add links to images posted anywhere.

Basically, the take away here is, wait patiently until your custom domain is accepted, and until your https status is confirmed. Everything will work, and your custom domain is shown everywhere, without "leaking" any Mb-specific links, other than of course your Mb username (which you keep and can use even if you no longer host here).

How images are handled ends up not being perfect for me. This [bike photo](https://microblog.bmannconsulting.com/uploads/2020/a28194eb67.jpg) got resized by Mb to an ~883KB JPEG. The original from my phone is ~5.1MB. I now have to think about making sure that that original is somewhere else. Also: no other sizes are created, other than for the Timeline, where Mb seems to run a resizing proxy. [Example of same biking photo](https://micro.blog/photos/1000x/https://microblog.bmannconsulting.com/uploads/2020/a28194eb67.jpg). **Feature request: Ideal for me would be a "keep original photo size" option (likely with a $ increase, same as for podcasts and videos), as well as having some other standard sizes generated to be used in templates.**

I selected `@boris@microblog.bmannconsulting.com` as my Mastodon username. This means that if you're on Mastodon, you can "follow" that account and you'll get all my posts. [@manton](https://micro.blog/manton) [wrote about Micro.blog + Mastodon](https://manton.org/2018/11/07/microblog-mastodon.html) back in November 2018.

As far as I can tell, from the Design page you can't easily get to full size previews of the themes. I found them on [Mb's GitHub organization](https://github.com/microdotblog) which was easier to browse the full size screenshots. **Suggestion: make thumbnails of designs clickable to full site previews**

There's still no "export" page anywhere in [Help](https://help.micro.blog/).  Here's what you can get when you search:

<img src="{% link assets/microblog/ae1324bcbf.png %}" width="568" height="495" alt="" />

Github is the closest, which is currently not an active feature, but it does tell you that you can go to _Posts_ and click on the _Export_ link at the top of the page, which is where you'll get links for export formats of WordPress and Blog Archive:

<img src="{% link assets/microblog/ba76d7ee41.png %}" width="287" height="154" alt="" />

**Suggestion: Make an export page in Help, and include this screenshot and describe WordPress and bar**. Maybe link to [Manton's blog post about Blog archive format](https://www.manton.org/2017/11/24/blog-archive-format.html).

Having tried a test export of `.bar` (rename it to `.zip` and you can open it and browse), this isn't very useful to me. I'd prefer individual Markdown files. I understand there are lots of different kinds and getting them to work with a particular static site generator is going to take _some_ work, but they also feel a lot more standard than `.bar`. I'll have to think about whether this is a dealbreaker for me. It's close to one, since WordPress is then the only other system that people could relatively seamlessly switch to. **Feature request: include a Markdown export format**

Looks like [per category archive links are broken on the Lanyon them](https://microblog.bmannconsulting.com/categories/biking/). I'll be experimenting with different themes and customizing them, so that link may show something different. Here's a screenshot:

<img src="{% link assets/microblog/999d04337d.png %}" width="277" height="194" alt="" />

---

## Update 1

I'm writing these notes up for me, and ideally in a way that it's helpful for others. I'm trying to be clear about feedback to Mb.

Suggestions are maybe design or documentation.

Feature requests are asking for new things and why they would be valuable to me. Balancing the feature requests of many users is very hard, so please consider these just out loud notes. And -- I'm happy to help with testing!

---

I thought about bringing together a few bits and pieces of stranded content. I was pleasantly surprised at all the import options!

I imported both Medium and a long ago WordPress account `boris.wordpress.com`. Wow, both worked great -- including bringing in Medium drafts that I had long forgotten about.

With so many posts, I ended up buying a license to [MarsEdit](https://www.red-sweater.com/marsedit/), a desktop blog editor. Works great!

One issue with the import is that in the web editor, Categories become unusable. Here's a screenshot from my phone:

<img src="{% link assets/microblog/eee291fd35.png %}" width="250" height="444" alt="" />

I'd like to see tags be supported, where you type and add a comma to create tags as you go. Categories are useful too, but also need to scale. **Feature Request: add Tags and/or let people use Categories with a tagging interface that scales to large numbers.**

I'm struggling a bit to figure out how to do selective cross posting. I thought I could use Twitter and LinkedIn category feeds and only enable cross posting of those categories, but its not currently working as expected. I'll experiment more and write this up.

I do a lot of creation on my phone. In the past, I had a full Micropub workflow using lots of different clients.

I setup [Quill](https://quill.p3k.io/), a web based Micropub client that works great on mobile.

Mb supports Micropub, advertising support for the following types:

* Post (note)
* Article (article)
* Photo (photo)
* Reply (reply)
* Favorite (bookmark)

The Mb label comes first, followed by the Micropub type in brackets.

Photos are Posts with images attached, and Articles are long form with titles.

I had used Bookmarks to create a mini directory of websites I want to share and organize by category.

On Mb, it turns out these really are Favorites. I thought I had found a bug, but posting a "Bookmark" adds a website entry and shows up in your account's Favorites (same as you favoriting another user's post). See screenshot:

<img src="{% link assets/microblog/cffa790d90.png %}" width="250" height="444" alt="" />

---

## Update 2 - July 6th

I turned on Replies showing up on the microblog. They [appear on a separate Replies page](/replies).

They don't appear to be able to be downloaded via MarsEdit MetaWeblogAPI, and they don't appear in the Posts web interface. Which means that Replies can't be edited. Don't know if they show up in an export, will have to test that.

I did a [reply](https://microblog.bmannconsulting.com/replies/2020/07/06/9893803.html) directly via the Mb feed to [Ton's post](https://www.zylstra.org/blog/2020/07/the-network-effect-by-martha-wells/). Remotely, the Webmention points to `micro.blog/boris`, which I consider to be a bug when I have a custom domain set (but I did initiate it from within the Mb timeline, so...).

Used Quill to make a Micropub reply to [Ton's other post](https://www.zylstra.org/blog/2020/07/quotebacks-block-quotes/). As of this writing, wasn't displaying yet -- the previous one showed up right away, but might be spam control on Ton's side. It initially redirected me to a [reply on the micro.blog timeline](https://micro.blog/boris/9893953) -- including some markdown that didn't get translated.

But I do get a [permalink on my custom domain](https://microblog.bmannconsulting.com/replies/2020/07/06/9893953.html), with the markdown now properly transformed.

**Feature requests: make replies available via MetaWeblogAPI and in exports. Should probably be available in Posts as well.**

**Bug: can't edit Replies.** If we consider it an advanced feature, maybe it's OK to only be editable via MetaWebAPI. This would be another dealbreaker for me: I need to be able to edit all the content I post to my site. I could work around it by only posting _Posts_ and not using Replies (which I'm already going to do for Favorites / Bookmarks, which is fine).

---

<a name="crosspost"></a>I thought I had Twitter cross posting working, but it seems inconsistent. What I did was turn off cross-posting for the main feed -- and also didn't "attach" any of those accounts for cross-posting. Screenshot shows "enable crossposting" because it is turned off :)

<img src="{% link assets/microblog/5e6fe2c90b.png %}" width="516" height="134" alt="" />

Then I added two other feeds for a Twitter category `https://microblog.bmannconsulting.com/categories/twitter/feed.xml` and a LinkedIn category`https://microblog.bmannconsulting.com/categories/linkedin/feed.xml`. On each feed, only the respective social account is linked / enabled.

So my thinking is, whenever I add either of those categories to a post, they will show up in those feeds, and then cross-post. Anything else will show up in my "main" Mb feed / blog feed but not cross post.

Twitter cross-posting [worked](https://twitter.com/bmann/status/1279868513402982400) for [this biking photo post](https://microblog.bmannconsulting.com/2020/07/05/a-test-ride.html). But then didn't work for [this second post](https://microblog.bmannconsulting.com/2020/07/05/digital-spaces-generally.html). I forget if I used the web interface or Gluon to post both / either of these, which may have something to do with it.

This [music post I just made today](https://microblog.bmannconsulting.com/2020/07/06/what-year-is.html), using the Posts web interface here, and tagged it with music and Twitter, and didn't cross-post to Twitter.

I haven't tried LinkedIn yet.

I guess this is sort of a **bug report**, I'm not sure if looping back category feeds into Mb is an expected use case. Since I can't control cross-posting behaviour through Micropub (and not through the Posts web interface here), it's my solution that if it works reliably would be really great and be very flexible.

---

Turns out there is a [@help thread](https://micro.blog/help/9896693) that covers this. I went ahead and removed the "main" feed, so it looks I should be able to add a LinkedIn tag _or_ Twitter tag and things will work how I want, but that adding _both_ won't work? I'll try them individually for now and see how it goes :)

I tried a LinkedIn-tagged post, authored it through Quill (in part, because the Mb Post editor was giving wildly inaccurate character counts?). [Worked!](https://www.linkedin.com/feed/update/urn:li:activity:6686317602719055873/) Looks like links / HTML gets stripped, and you get a link back to [your post here on Mb](https://microblog.bmannconsulting.com/2020/07/07/via-davidcrow-the.html). The theme I have doesn't have social metatags, so I'll add that to my TODO.

---

Posted [a from scratch post](https://microblog.bmannconsulting.com/2020/07/07/its-ottawaera-boris.html) via MarsEdit (only made edits before). Post didn't make it to the Mb feed. Is this because I deleted the "main" feed? Not a big deal really, I'm either cross posting or posting for feed subscribers mostly.

Also, this post itself doesn't seem to show up in MarsEdit at all?

---

To be continued...

