---
tags:
  - WIP
---
_Startup and small business operations and efficiency_

_Note: this page is undergoing major renovations. Skip to the bottom for other resources tagged with startup_

**"Startup"** is this weird phrase that means lots of different things. For me, one of the things that it means is really internalizing a couple of different concepts.

One is the [[Lean Startup]], which has lots of baggage associated with it today, but at its core there is the **Build - Measure - Learn** loop.

You start with a hypothesis (another key concept), like "adding an ecommerce channel will lead to more sales", and then you build the minimal version of that that you can, measure the results, and learn from that.

Did you make a Return on Investment (ROI) of your time / money / interest? Does it look promising, but you need to build a more complete store or have a person dedicated to running it? Did you learn that you don't enjoy the process of figuring out an ecommerce app and online marketing, but want to have someone else do it as part of your business?

I also associate efficiency with my version of startup. This efficiency can come from:
* "operationalizing" or "productizing" parts of your business so that you understand what runs your business, what the steps are, and how you might apply the next two concepts
* using digital workflows and automation
* outsourcing parts of your business / workflows so people can focus on what they like to do, are good at, or simply make more money by working on their core

# Types of Startups

## Venture Startup
A venture startup is a business that can grow (or "scale") to a very large revenue over time. The classic number is, can your business get to $100M in annual revenue in 5 years?

[[Venture Sized Business]]

The other line you'll hear a lot at the beginning of a venture startup is "do things that don't scale".

You don't know what the most valuable parts of the business will be, so you are optimizing for learning and insights from your customers rather than efficiency.

## Digital Small Business

TODO

## Deep Tech

TODO
## Moonshot

TODO

Also [[Vancouver Moonshots]]

# Capital Investment

* Angel vs VC
* Crowdfunding
* IndieVC-style investment
* Revenue Financing
* Future of Venture

# Getting Started

All businesses, companies, and ideas get started somewhere, and over time have various setup and improvement needs.

I say over time as well, because changes in the business -- either a growth in the size of the business, adding more people, or trying out new ideas -- will need new things to get started.

These are a set of recommendations of tools, generally aimed at the "just getting started".

* [[Canadian Incorporation as a non-resident]]

## Web Presence

TODO: write up "spend $0 or $5K on a website"

* [[Namecheap]]
* [[GSuite]]
* [[Fastmail]]
* [[Squarespace]]
* [[Webflow]]
* [[Ghost]]

## Company Information

TODO: Using Discourse Forum & Discord Chat for Company and Community

* [[Discourse]]

## Company Formation

TODO: write down a couple of different options, esp. venture startup vs. small business

* [[Ownr]]
* [[Stripe Atlas]]
* [[Clerky]]
* [[Startup Lawyers]]
* [[Small Business Lawyers]]
* [[Reverse Vesting]]

## Banking, Finance, and Accounting

* [[Xero]]
* [[Wave Payroll]]
* SMB / consulting finance vs. Startup finance
* [[Budget Scenario Template]]
* User Model / Business Model Worksheet template
* Sprout Accounting

### International Payments and Transfers

[TransferWise](https://transferwise.com/invite/u/borism73) will give you the best foreign exchange rates and also will give you USD, GBP, EUR bank accounts (amongst others) that you can accept money into from others.
## Metrics

* [[Posthog]]
* [[Metabase]]
* [[Plausible Analytics]]
# Resources

Other notes tagged with startup:

<ul>
{% for post in site.notes %}
{% if post.tags contains "startup" %}
{% unless post.tags contains "organization" %}
<li><a href="{{ post.url }}" class="internal-link">{{ post.title }}</a></li>
{% endunless %}
{% endif %}
{% endfor %}
</ul>