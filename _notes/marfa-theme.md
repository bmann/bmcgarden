---
title: Marfa Theme
git: https://github.com/bmann/theme-marfa
date: 2020-12-06
modified: 2021-01-10
---

I'm using the Marfa theme from [[Micro.blog]] for my site [blog.bmannconsulting.com](https://blog.bmannconsulting.com). My fork is public here: https://github.com/bmann/theme-marfa

## To Do

Home page has avatar and "follow on Mb" links. Change to ???

No pagination on Photos page. Remove and replace with a new / different photos layout.

Error on bio page (linked to avatar). Need to include new partial.

Custom 404 page, need to add `not_found.html`

## [[WIP]]

Copied [yearly grouping](https://github.com/jnjosh/internet-weblog/blob/master/layouts/partials/yearly_grouping.html) across from `internet-weblog` theme into the marfa theme. Live example on the authors blog: <https://jnjosh.com/posts/>. Copied `list.archivehtml.html` and `list.photoshtml.html` across from the `theme-blank` default Mb theme. Figuring out how these all fit together, how do I get Hugo to locally create this archive page? Just make an `/archive` folder?

## Done

Added tags to the `#post-meta` section at the bottom of `single.html`. Messed around with CSS styling to make button-style tag links with an arrow in front.

Post pages have avatar and microblog at the bottom. Removed this section entirely.

The "Call to Action" (CTA) on single posts in the upper right hand corner points to Mb -- point it at bmannconsulting for now.

Footer link to Mb, point it at bmannconsulting for now.

Moved custom footer partial inside the **actual** footer, rather than just blank text at the end of the page.

Looking at [internet-weblog theme](https://github.com/jnjosh/internet-weblog) for ideas, adding categories to posts.
