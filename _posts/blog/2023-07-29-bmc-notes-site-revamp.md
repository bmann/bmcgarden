---
date: 2023-07-29T22:12:10.268-08:00
title: Notes & Homepage Revamp
categories:
    - BMC
tags:
    - blogging
    - LogSeq
    - Digital Garden
---

This is very much a blogging about blogging (and Digital Garden) post. I've written many words in many places since the <a href="{% link _posts/blog/2021-03-14-moa-party.md %}" class="internal-link">last post</a>. Many of those words have been into LogSeq, which I flipped the switch on at the beginning of this year to run this whole site, including my (lapsed) tech [blog]({{ '/blog/' | relative_link }}), and long term [archive]({{ '/archive/' | relative_link }}).

I wanted to have one grand intertwingled set of both Digital Garden style Note and Journal pages, as well as all of my archive of posts.

But LogSeq is not well suited to blog-style articles. And, the way that it publishes, <a href="https://notes.bmannconsulting.com/#/page/Jan%207th%2C%202023" class="noteslink" target="_notes">it packs everything into a single index.html file</a>, which for my 20 year archive of blog posts was gigantic. It got up to 40MB![^40MB] So someone visiting the site would have to download 40MB ... and only then be able to start interacting with the site.

So, I've spent some vacation time this past week[^foodwiki] moving things around. LogSeq had 2000+ archive posts trimmed out of it, and now lives at the [notes.bmannconsulting.com](https://notes.bmannconsulting.com) subdomain. That means that it's a bit smaller, but the `index.html` is still 9MB, and will only grow as a I add more pages. But it works for me, on both desktop and on my phone, using git to sync. 

I'm calling this site my Homepage. Which is what it is![^neocities] It's the boring domain I picked a long time ago, and this root domain and other subdomains hanging off it is where all my stuff should be.

* bmannconsulting.com: This site, my default domain that represents me and "my stuff". A homepage. With a blog. And an archive.
* [blog.bmannconsulting.com](https://blog.bmannconsulting.com): more personal posts, often around food and local stuff, runs on Micro.blog which powers cross-posting.[^crosspost]
* [notes.bmannconsulting.com](https://notes.bmannconsulting.com): LogSeq powered, default home page is the Daily Journals

And "other stuff", that I can easily keep at subdomains, and maybe do more with in the future:

* [twitter.bmannconsulting.com](https://twitter.bmannconsulting.com): my Twitter archive, powered by [Tweetback](https://www.zachleat.com/web/tweetback/)[^twitterarchive]
* [2022.bmannconsulting.com](https://2022.bmannconsulting.com): a snapshot of late 2022 version of the website, Simply Jekyll edition[^colophon]

I'm not convinced I'm going to get back on the regular blog posting schedule. I've fallen off the wagon of RSS _reading_, myself, in part because I'm bouncing around multiple decentralized social networks[^decentsocial], and in part as I said at the beginning -- I'm writing a lot of words in a lot of places already.

I may end up doing a weekly round up of the Daily Journal pages from my Notes site. That's usually where I clip links and articles and such. And there's a [feeds]({{ '/feeds/' | relative_link }}) page here again, so my site should be subscribable.

[^40MB]: The linked note has a screenshot that shows it at 18MB. You can go [look at the gh-pages branch](https://github.com/bmann/bmcnotes/blob/gh-pages/index.html) to see how big the current version is.

[^foodwiki]: The FoodWiki has views & food from around Nanaimo, starting on [July 22nd](https://foodwiki.bmann.ca/July%252022nd%252C%25202023.html). See what I mean? I'm writing a lot of words!

[^neocities]: Notwithstanding the [bmann.ca](https://bmann.ca) one page kind of link tree thing I put together on Neocities.

[^crosspost]: Anything I post to Micro.blog ends up on Mastodon, Bluesky, Nostr, Tumblr, and even LinkedIn.

[^twitterarchive]: I ran a [Twitter to Github Pages script for many years](https://hawksey.info/blog/2016/08/keeping-your-twitter-archive-fresh-and-freely-hosted-on-github-pages/) that is still up at <https://tweets.bmannconsulting.com>. You can see when the Twitter API finally died in June. Tweetback has the potential to interconnect

[^colophon]: There's always a [Colophon]({{ '/notes/colophon/' | relative_links }})

[^decentsocial]: Or [DecentSocial](https://notes.bmannconsulting.com/#/page/decentsocial) as the shorthand goes
