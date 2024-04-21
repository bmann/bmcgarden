---
tags:
  - membership
  - newsletter
  - opensource
  - blogging
  - CloudronApp
  - app
link: https://ghost.org
github: https://github.com/TryGhost/Ghost
frame:
  image: /assets/2024/ghost_logo_black.jpg
  image-aspect-ratio: "1:1"
  button2:
    label: "Github"
    action: "link"
    target: https://github.com/TryGhost/Ghost
  button1:
    label: "Home"
    action: "link"
    target: "https://ghost.org"
  
---
A blogging and membership based newsletter app. [[MIT]] licensed open source. 

Maintained by the [non-profit Ghost Foundation](https://ghost.org/about/), who also run a paid managed hosting service at <http://ghost.org>.

## Moving Paid Subscribers from Substack

I’ve been recommending Ghost instead of [[Substack]] for a long time. [Molly White wrote up her whole migration](https://citationneeded.news/substack-to-self-hosted-ghost/), I’ve quoted a few sections below.

On paid subscribers:

> The good news is that you can migrate your Substack subscribers (paid and free) from Substack to another service. Substack uses Stripe for payment processing, and so as long as you continue to use Stripe (used by Ghost, Buttondown, beehiiv, etc.) you can swap out the newsletter platform without any interruption to them. This is huge — as someone who migrated from Patreon way back when and had to ask everyone in my (much smaller) subscriber base to manually re-subscribe, that's a nightmare.

There’s a second step where you also need to ask Substack to remove themselves from your Stripe:

> I needed to ask Substack to disconnect themselves from my Stripe account. **This is critical**: if you don't do this, subscriptions created through Substack will _continue_ to send a 10% cut to Substack, even after you've left the platform!

## Pricing

For self hosted Ghost, [[Mailgun]] is going to be your biggest expense. It’s also the only thing that Ghost supports for sending email. 

Molly also include a bit on pricing:

> After all of this, I have found myself with a roughly $103/mo setup: $28/mo for the VPS, $75/mo (plus overage tbd) for Mailgun. This is considerably cheaper than staying on Substack, and also slightly cheaper than both hosted Ghost and Buttondown.

She wrote a lot of custom code and migration scripts as well as dealing with a lot of DNS and email settings. For most people, hosted Ghost would be an option. 

The other way to make this cheaper would be to work together with a number of people. 

eg [[Cloudron]] supports Ghost and you could share a server with a number of people. And also share a Mailgun account, which also gets cheaper in bulk. And some of those people could become experts in email and DNS. 
## Headless CMS

You can use Ghost as a headless CMS, which is what [[Fission]] does for <https://fission.codes>. Everything is authored in Ghost, and then a GitHub Action pulls all the content from the Ghost API  and builds a static site with [[Eleventy]].

This is getting less feasible over time and has a number of work arounds required especially for membership support. I’d pick a [[Headless CMS]] instead. 

## Ghost Annoyances 

The Ghost Foundation has made it harder and harder to self host Ghost over time. 

I used to maintain a Heroku buildpack, we made an [[IPFS]] plugin at [[Fission]], one used to be able to choose Postgres now only MySQL is supported. 

And of course, fair enough. The Ghost Foundation is doing the work of maintenance and they’re optimizing it for their needs, which is a managed hosting platform. 

But it doesn’t feel as much like a community platform any more. 

I still recommend it if what you need matches what Ghost offers out of the box: both blogging and newsletter sending, and/or paid membership management.

But, because of the way it’s managed as a project, it’s going to be hard to build on top of for anything other than basic plugins or API integrations. 

## Other Notes

I wrote some comparison pages and have a whole set of inter-linked notes about Ghost over at [my old LogSeq site](https://notes.bmannconsulting.com/#/page/ghost).