---
tags:
  - crossposting
  - platform
  - organization
  - saas
  - Canada
  - Toronto
link: https://fedica.com
---
Website: <https://fedica.com>

Used to be Tweepsmap for mapping of Twitter. Now full social media analytics, with scheduling and crossposting across 8 networks. 
## Pricing

The free plan allows for basic cross posting across 8 networks, 1 account max per network. 

Additional accounts are $10/month. So 2 accounts per network (16 accounts total), is $20/month for the Publish account.

* Publish: $10/month 
* Grow: $24/month
* Research: $79/month
## RSS Publishing 

Importing via RSS is a feature of paid plans. 

After my feedback to the Fedica support team, they've updated how this works and [documented it here](https://fedica.com/social-media/how-to-setup-rss-feeds).

* Reads the `<title>` as the content of the post, OR `<description>` if no title field
* Posts are auto split into threads for those networks that support threads
* Scans the `<description>` field and attaches the first `<img>` that is present, or up to 4 images in the `<enclosure>` field
* Adds a link back to the post at the end / last post in the thread
* Hashtags are defined per pipeline, and are also added at the end / last post in the thread
* Pipelines can be configured to exclude certain words, and title, description, category, and content fields are all checked for this; this means you could make a "nocrosspost" category for instance

[This page describes how to set up pipelines](https://fedica.com/social-media/how-to-setup-rss-feeds), but the bulk of the info is in this video:

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/HfrPWP_bBw8?si=7EjdiJWj9Kmv_oxj" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

A few other notes from my messages with the support team, and as I configure things.
### Repeat

> Repeat will publish your content again if your pipeline runs out of new content, but fresh content will always take priority over repeated content. You can set for how long you want to repeat the content. Tweets are usually reposted as retweets when repeated​.



