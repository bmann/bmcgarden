---
title: Github Actions for Jekyll
---
TLDR; you can use Github Actions to build and publish your Jekyll site for free, which lets you do things like use arbitrary Jekyll plugins, as well as custom publishing end points like Fission.

I used the [nicely commented limjh16/jekyll-action-ts](https://github.com/limjh16/jekyll-action-ts/blob/master/.github/workflows/workflow.yml) to power the [[Github Actions]] to build this [[Jekyll]] site.

I didn't do anything special to make it work. Here's the code [bmann/bmcgarden](https://github.com/bmann/bmcgarden/blob/master/.github/workflows/jekyll-build.yml), with [[Fission Publish]] added at the end.

You have a certain amount of minutes included with your [[Github]] account. Looking at the [timing for my workflows](https://github.com/bmann/bmcgarden/actions), they are about 4 - 6 minutes to build and publish the site. I pay for a personal Github Pro account ($4/month), but because this site is not a private repo, I guess I can use as many minutes as I want? I'm not seeing any indication that I am using up minutes.

For private repos, the [billings page](https://github.com/settings/billing) says that 3000 minutes per month are included. That would be 3000 minutes / 6 minutes per build = 500 builds, So, I could publish up to 500 builds / 30 days per month = 16 builds per day.

My site takes quite a long time to build because the [[Simply Jekyll]] theme which powers [[backlinks]] and various other features is all implemented at the theme layer. And, Jekyll is slow for large sites like mine.