---
tags:
  - crossposting
  - platform
  - organization
  - saas
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

Currently, here’s how this works:
* Reads the `<title>` as the content of the post
* Maximum content is 257 characters across all networks 
* Scans the `<description>` field and attaches the first `<img>` that is present
* Adds a link back to the post at the end

One thing to note is that if you have feeds without titles — which is how my journal [[feeds]] work — then the posts will only have a link and no content.  

I’ve put in a support request and am having a discussion with the team and it sounds like they are open to two new features:
* support for optionally reading the description field for content 
* Variable truncation per network — eg 500 for Mastodon, 300 for Bluesky, 3000 for LinkedIn, etc; or, optionally, threading long posts automatically (I would love auto-threading)

Thanks for looking at this Fedica team!
