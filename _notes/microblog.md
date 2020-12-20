---
title: Micro.blog
link: https://micro.blog
tags:
    - blogging
    - saas
    - IndieWeb
    - Micropub
---

A hosted microblogging service that uses [[Hugo]] static site generator underneath. Supports [[IndieWeb]], [[Micropub]], [[ActivityPub]] and more independent and open web protocols.

Founded by [[Manton Reece]].

[[Recommended]] for people who want to run a blog on their own domain, while still being able to cross post to Twitter, LinkedIn, Medium, Tumblr, and Mastodon. Also supports podcasts and videos at premium accounts.

---

I pay for an account to [run my microblog at blog.bmannconsulting.com](https://blog.bmannconsulting.com). My username and feed are at [micro.blog/boris](https://micro.blog/boris)[[I sometimes forget that 'other' Boris Jabes has the <em>boris</em> microblog link at <a href='https://boris.micro.blog'>boris.micro.blog</a>.::lsn]].

I'm using a custom version of the [[Marfa Theme]].

## Micro.blog Sidebar

The help article explains that you can [embed your microblog feed into other sites using sidebar.js](https://help.micro.blog/2016/sidebar-js/).

The nice thing about this is that your feed automatically includes the posts you make to your blog, but you can also add third party feeds. This means Micro.blog can be your own aggregator, rather than having to merge feeds somewhere else.

Unfortunately, there is no permalink included for these posts, so they are much less useful. This is generated as HTML -- which is great, because it can just be output. But, without linking back to the original, I'm not sure that it makes a lot of sense? It would mean that Mb needs to know / store the permalink or source of each feed item. I _think_ [[JSON Feed]] that you include would have this?

### Feature Request: include permalinks in sidebar.js

For each feed item in sidebar.js, wrap the date or a separate small `#` (or the title for posts with titles?) in a permalink that points to the source item.

Optionally, consider linking to the micro.blog post itself OR the source item, as an option.

This means that when your micro blog feed is embedded, people can actually follow the link to see where it came from. As it is, it's just a chunk of HTML, and there is no way for the user to easily get the permalinks.

I'm embedding my own [boris feed](https://micro.blog/boris) below so I can point to it as an example:

---

<script type="text/javascript" src="https://micro.blog/sidebar.js?username=boris&count=5"></script>

<hr style="margin-bottom: 50px;">