---
tags:
  - management
  - networkedorgs
title: Networked Orgs and Tooling
date: 2022-01-15T20:51:39
categories:
  - NetworkedOrgs
---
Originally written by me in the Fission [Discourse forum](https://talk.fission.codes/t/networked-orgs-and-tooling/2402), posted January 2022. My focus on tooling is in part because the affordances of tools is what influences the day-to-day praxis of organizations.

[[NetworkedOrgs]] is my local notes page that connects more related articles and resources.

---

At the PLN talk on hiring / recruiting in Web3, we ended up discussing afterwards about the nuances of different chat systems, and also identity, and chat vs long form, and thoughts on how and what tools to use and promote in a web3 way, while also needing to bridge company, compliance, community, and other needs.

I haven’t written about it publicly to date, but I have been enthusiastically sharing that I am hugely inspired by Protocol Labs and their “versioning” approach to company and organizational evolution. This current version sees the birth of the Protocol Labs Network, or PLN, to which Fission is lucky enough to have been invited to become a member of.

Fission is a remote first organization that spans 4 time zones, plus another two time zones that we collaborate with external partner orgs. Our software, apps, protocols, and dev tools are published under a variety of open licenses, and the team has a history of participation in open source. <mark>The company uses the same tools for internal collaboration as it does for community collaboration</mark>, which makes for a very fluid boundary between external and internal.

The three core collaboration tools we use are Discord chat, the [Discourse forum we call “Talk”](https://talk.fission.codes), and Github. 

## Chat

Chat is a huge part of day to day life, both socially as the primary native mobile interface, and in business with the rise of Slack beginning ~2013.

This is “flow”[^flow] and it is great for even large groups of people to jam together. We’ve been using it to great effect since the beginnings of open source and IRC.

[^flow]: See [[Stock and Flow]]

Having an open chat community where people can drop in and get questions answered, often quickly, and by anyone that happens to be there and awake. And, this is “working in public” — anyone can “watch” a text interchange and learn from it and see the context.

The downside is that it is synchronous, which doesn’t work great for differing time zones. And it isn’t very discoverable or browseable. Most chats aren’t indexed by search engines. Search of chat history goes from atrocious to mediocre.

This story of Stripe deleting chats to encourage people to treat them as ephemeral is amazing:

> An engineer at Stripe told me about their careful balance of email, forums, and Slack. They recognize that Slack is not suitable for meaningful conversations, so they automatically delete chat messages older than a few weeks to discourage relying on it for long-term archival. In retrospectives, team members often reflect on whether they chose the right medium (email, chat, or forum) for various conversations.
> -- [Derrick Reimer](https://www.derrickreimer.com/walking-away)

TODO: talk about Fission’s monologue channels

TODO: talk about email, and how Fission sends zero internal email
### Slack

Slack is built for enterprise, and has lots of compliance and retention rules that can be set up per workspace. The workspace is owned by a company, and it is assumed (aside from Slack Connect channels into other workspaces) that IT admins and other company staff have access to every single piece of information, including “private” direct messages.

Permissions are such that it is assumed that everyone “inside” the Slack has the same base level of trust. Having an “open” slack is hard in a number of ways, including extremely limited moderation tools.

From an account perspective, you’ve probably got dozens of separate Slack accounts, which may or many not be tied to a variety of different email addresses.

It is tuned for the needs of business and gets more enterprise focused every day. Developer communities in particular have been moving to Discord as their primary backbone, rather than Slack, over the last 2-3 years.

From an API perspective, the intended user is the organization, not the individual.

Free Slack instances have a message history limit, and a bunch of other restrictions. The jump from free to paid can be incredibly large. E.g. a community with 100 members might go up to $500 / month from free!
### Discord

Discord is one big platform where you have a single account as a user, and can participate in direct messages, or in servers. It can be used as a DM platform, including DM groups like Signal, WhatsApp, or Telegram, but its main interface object is the Discord Server: you are a member of one or more Servers, and have various Roles and thus Permissions on those Servers.

It started in gaming, and so very quickly had to gain robust community moderation tools. The roles and permissions available really do let you do a lot.

From an API perspective, you have an account that can access everything anywhere that you have access to on the Discord platform. If you are a server owner, that means some elevated access, but it also means that as a user, you can supply credentials and in fact suck out / mirror / export every piece of content that you have access to, anywhere on the Discord platform.

Every user is on an even playing field with respect to the platform. Yes, there are server owners, but they too are “just” another Discord user account. This is in contrast to the corporate owned model of Slack.

Discord has a novel business model. Individuals buy boosts, and then they can give boosts to servers, and the servers get more features. Technically this is a form of freemium.

Server owners can also buy and pay for boosts directly.

If you squint, this is the users of a platform (at the server level) paying for the stuff they value. **Is Discord the largest example of co-op payment at scale????**

There’s more to say here about Discord audio and video features, their new events stuff too.

Oh right. Discord “announcements”. It’s a pub sub mechanism that most reminds me of RSS in a strange way. Announcements can be subscribed to, by other servers, and you can choose which channels those announcements go into. An interesting way to keep tabs on other servers and the info that they deem high value enough to announce / publish.

There’s a whole **other** thing to write about server-centric sticker / emoji slots. Both user centric (you can use emoji from any server you are a member of) and also server centric (get more boosts, get more custom emoji slots).

While Discord has rich APIs, the whole stack is centralized and proprietary. What’s my justification for recommending it? Chat is ephemeral, therefore low risk (and/or you should also mirror “important” stuff elsewhere). Full APIs, so export and other tools **can** be written.

### Element / Matrix

The [[Matrix]] protocol is great! End to end encryption, you can self host as well as federated, it’s open source.

I’m personally super bullish on it as a building block. The [Beacon](https://walletbeacon.io) system for app <> wallet communications on Tezos uses Matrix in browser, and it’s a pretty great experience that I hope to implement as part of [FIL Accounts](https://talk.fission.codes/t/fil-accounts-pl-unconference/2254).

The Element clients and the actual experience and feature set of using Matrix is … OK. A couple of years back, I would rate it as barely usable.

High ideological and technical alignment, could use UX polish and/or alternate front ends.

There are even Matrix powered comments!

It’s also working on fundamental research into important areas of the dweb, like [distributed reputation](https://talk.fission.codes/t/combating-abuse-in-matrix-without-backdoors/1127).

I think Matrix should be prioritized to be used as a transport layer and in other chat-like situations. It works in native applications and it works in browser.

I’d love to see more front end innovation and integration. Are there technical limits to making something more Discord-like? (There are people that hate Discord UX, so mostly I’m thinking about the community moderation and usage here).

### Other Chat Systems and Protocols

There are other open source chat systems / protocols.

#### Signal

If we could connect to the Signal network and/or interop with its protocol — that would be amazing! A high polish system that goes all the way to mass market end users.

Might be good to explore this, and at the same time it is focused on group chat, and not really a larger server / company setting.
#### Gitter

It is transitioning to use Matrix, and is highly focused on developer chat. Very interesting!

## Long Form Community Writing

Github Wikis are trapped on Github namespace and don’t really have permissions. Confluence is part of the greater Atlassian sphere and couldn’t be farther away from open source and community work.

HackMD is OK, you’ll need the enterprise version to really use it. HedgeDoc and various other open source versions that forked off of HackMD are pretty janky.

Every company has handfuls of GDocs in various states of “where the heck is that file” that is basically invisible to search.

I loved Quip, but then the Salesforce acquisition. I loved Dropbox Paper, but…so many Dropbox thoughts.

What does long form community even mean? Well, it’s the stock to chat’s flow[^stock]. Write down the notes, evolve a wiki page, share a link rather than re-answering the same question all the time, and make notes / information browseable and discoverable for all those that should be able to find it.

[^stock]: Really, go read [[Stock and Flow]]. It's not super deep, but you can start sorting things into one bucket or the other.

I’ll leave project management and spreadsheets for another rant.

### Discourse

I personally have setup and admin 5 Discourse communities. The makers of Discourse have a strong open source ethos. They run a commercial hosting service, but there are a number of third party commercial hosting options, **and** the core team maintains and updates Discourse and plugins in such a way that it is very easy to keep updated and maintained. And easy to install! A $10/monthly VPS will let you comfortably run a Discourse forum.

Most peoples’ experience with Discourse is as a public forum. But it has extensive groups and permissions, and some really interesting email integration features that lets it do all sorts of other things.

Yes, you can mirror an IMAP inbox into a group, for running things like support ticketing or any other shared inbox use cases (e.g. the kind of thing you might use anything from ZenDesk to Front App for, or god help you the nightmare that is Google Groups).

It can be your wiki, your discussion forum, your meeting notes, your company vacation calendar, your public events calendar, your project management tool, and even power the comments on one or more blogs. The team at Discourse has integrated Github in such a way that they do code reviews in Discourse that round trips to Github.

It’s got great APIs and Webhooks, and a very good auth / SSO system.

There is a new [Discourse Teams offering](https://teams.discourse.com/)  — which is configured as private / internal, tuned out of the box to be used as internal company collaboration. Fission has configured some of its internal usage in a similar way. 

It works well on mobile. It’s editing experience is such that you can close your desktop and pick back up editing a draft on mobile or vice versa, and it will pretty much auto save in the background.

The bookmarking system is super interesting. It’s bookmarks crossed with reminders — so you can use it as a simple TODO or reminder system, to come back and answer someone or do something.

Discourse has great tools and automations — and really, is set up out of the box — to do really good community moderation, at scale, out of the box. 

In decentralized communities, Discourse has been adopted for governance of protocols, pointing to a whole other wave of growth.

Are there any issues with Discourse? Well, it’s a very unique system that takes a lot to customize and extend. The core team has strong opinions, which means your usage has to somewhat align with those opinions.

Anyone with an admin account has full access to everything. There is good audit trails built in, but you can’t keep stuff in private from the admin user. The work around to this is to use a shared, privileged set of admin accounts, and day to day everyone uses lower permissioned accounts that are fully bound by the privacy settings on groups and categories. 

I think Discourse is peak long form community, built in a classic Web2 Rails with a database style. I’d say it doesn’t scale down well to smaller groups (albeit Fission has been using it since we were 5 people). The “activation energy” of setting up an entire Discourse is hard, but a single Discourse can itself easily host groups and categories very simply.

## Better Futures for Networked Knowledge Sharing

I have long been inspired by [this story from 2016 of how Algolia used their own product to create universal search for all of their company knowledge](https://stories.algolia.com/how-algolia-uses-electron-to-improve-internal-productivity-8e89efe60b59).

The [Orbit Model](https://talk.fission.codes/t/orbit-model-of-developer-engagement/635) — and [Orbit the SaaS tool for community analytics](https://orbit.love) — acknowledges that communities can’t be modeled as sales funnels, and so developed a model and “orbits” of engagement:

We also had [founder of Orbit Patrick Woods come and present](https://talk.fission.codes/t/the-orbit-model-with-patrick-woods/1031).

There is a lot of [[Tools for Thought]] folks that hang out with Fission who are all interested in IPFS with content addresses uniquely identifying versioned documents and other assets. And, thoughts of interop, linking between people’s digital notes.

Led by Roam Research (not open source), there has been a wave of TFTs, and in fact certain base concepts like [[wikilinks]] that generate backlinks have become another textual interface that I think is getting up to the common interface patterns like @-mentions and `#tags`.

Discourse itself supports backlinks (and @ and #) but without the wikilink square brackets — if you link to some other article, that article will show a “backlink” to the things that link to it. This could be improved by better theming to highlight those backlinks in a better way, and probably lots of other interesting relevance graph stuff, too.

We haven’t seen “backlinks at scale” in an open way, quite yet. What if across PLN, meeting notes or project proposals or events or many other kinds of common written material included [[backlinks]]? If you can browse all the things pointing to `fvm` or `FIL Accounts` or `OpenLunar` you start getting really interesting signal. Frequency, relevance graphs, clusters, and so on.

What does it mean to build a search engine that indexes the websites and blogs of all the people, companies, and projects in the PLN? What if you instrumented all their social media (opt in!) to also grab all the favourited tweets?

What if we ran a PLN Mastodon instance? Maybe [add an IPFS file store to it](https://github.com/fission-codes/bounties/issues/4) while we’re at it.

My thinking about organizational and community conversations and evolutions is much influenced by [[Simon Wardley]]. He has correctly predicted (actually, mapped, using [[Wardley Maps]]) the growth of the cloud industry since 2007.

Another important Wardley concept are people / organization group archetypes: [[Pioneers, Settlers, and Town Planners]]. Pioneer types don’t tend to write things down / do much documentation. You need at the very least “pioneers with settler tendencies” to help bridge and grow this.

Wardley has refreshed his look at traditional vs next gen organizations in [[How Organizations Are Changing]] in 2021.

I think you’ll see a lot of PLN in there, and broadly speaking networked organizations. He has other writing on organizational capabilities and different stages of organizational maturity, but I’ll leave it there for now.

I’ve suggested that I’d like PLN to learn [[Wardley Mapping]] together. I’m actively looking to join a peer group who goes through some paid training on Wardley Mapping, and then helps critique each other’s mapping strategies for the areas their organization is targeting

## Update February 2024
This post ends a little abruptly! There are some further good links and discussion in the original [forum post](https://talk.fission.codes/t/networked-orgs-and-tooling/2402).

I'm retroactively publishing this as a blog post, with many of the links re-pointed to local note posts that I've imported.

This very much fits into my [[pooling capital and collaboration]] theme.

[[co-op]] structures aren't naturally networked orgs, but one of the principles is to work with and support other co-operatives, so co-ops could benefit from thinking of themselves more as part of a network.

On tools, there's probably something to say about [[Open Collective]]. Self-hosted git forges are emerging. "Sharing" engineering resources -- both from a cost/funding perspective and a coordination perspective is very hard, and [[Open Source Licensing]] needs an evolution.

Stay tuned!