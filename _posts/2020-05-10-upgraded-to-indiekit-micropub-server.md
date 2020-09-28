---
title: 'Upgraded to IndieKit Micropub Server, Feed Tweaks'
date: 2020-05-10T15:43:01.897-07:00
category: "Blog"
tag:
- blogging
- IndieWeb
- IndieKit
- micropub
---
I should be all switched over to using [IndieKit](https://bmann-indiekit.herokuapp.com/), a micropub server that lets me use various IndieWeb technologies to easily publish to my blog.
<!-- more -->
One of the main features this gives me is media uploads. I can create a short note (aka Twitter posts) and attach one or more images, like this [mural and ebike rides post from yesterday](https://blog.bmannconsulting.com/zpmpn/).

For those following along via RSS -- sorry! [Ton noted that my feed was a bit messed up](https://www.zylstra.org/blog/2020/05/14095/), which was theoretically the last thing to fix.

You can see [Pat and I making faces in a previous test post](https://blog.bmannconsulting.com/testing-a-full-blog-post/) on Wednesday night. But as happens, there was much tweaking to be done.

With my custom post types where I glue in a gallery of images, everything wasn't really working right any more with the jekyll-feeds automatic feed creator.

I implemented an Atom feed manually, which theoretically requires a title for each post. Then, just now, I switched it to an RSS feed, and also found useful templates at [snaptortoise/jekyll-rss-feeds](https://github.com/snaptortoise/jekyll-rss-feeds) -- which also links to JSON feed templates at [snaptortoise/jekyll-json-feeds](https://github.com/snaptortoise/jekyll-json-feeds).

For those that want to dive even deeper into my setup, I tend to keep my [colophon](https://blog.bmannconsulting.com/colophon) up to date, and took the opportunity to put in an entry about the current state of things.

Please let me know if feeds or anything else seems broken or wrong!
