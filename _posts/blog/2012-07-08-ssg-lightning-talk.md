---
layout: post
title: "Static Site Generators Lightning Talk at HTML5 Vancouver Meetup"
description: "Intro to static site generators"
categories:
- Event
tags:
- static site generator
- presentation
- HTML5 Vancouver
comments: false
---
I gave a quick 10 minute lightning talk at the [HTML5 Vancouver Meetup group](http://www.meetup.com/Vancouver-HTML5/events/67866502/) about static site generators (SSGs).

I ended up putting the presentation together using [Hekyll](http://brianmcmurray.com/blog/2012/02/07/hekyll-for-awesome-easy-presentations/), which is, itself, an SSG for making presentations using [impress.js](http://bartaz.github.com/impress.js). impress.js is an HTML5-based clone of Prezi, the panning / zooming presentation app; I just opted for simple presentation mode.

Check out the [SSG Lightning Talk](http://projects.bmannconsulting.com/ssg-lightning-talk) or view it in the iframe below (use arrow keys to advance).
<!--more-->
<iframe src="https://projects.bmannconsulting.com/ssg-lightning-talk/preso.html"
  width="800" height="600"
></iframe>

This presentation needs work (never mind the fact that using my new machine to do a presentation caused a bit of a fumble). I spent a lot of time futzing with the tech, which should've gone into tuning the content. I'm finding a bit of a problem determining the right level to cover with SSGs. There are a lot of moving pieces around generators, layouts, and hosting, plus trying to explore the "why" of SSGs and what kind of solutions they apply to.

Hekyll was an interesting experiment. I like that I can keep my presentations on GitHub directly. Theming needs work - or my design + CSS skills need work, depending on how you think about it :)

I also ended up demo'ing [Prose.io](http://prose.io) (read [Development Seed's intro blog post](http://developmentseed.org/blog/2012/june/25/prose-a-content-editor-for-github/)), which is a web-based content editor for GitHub. So, if you're creating / hosting content using GitHub's native pages functionality (which uses the Jekyll static site generator), it means you can edit your content online in a friendly, Markdown-aware environment in your browser.