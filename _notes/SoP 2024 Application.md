---
link: https://forum.summerofprotocols.com/t/pig-community-search-engines-event-chat-artifacts-as-research-building-block/879
tags:
  - sop24
---
I applied to the Summer of Protocols 2024 program with this RFC plus a private personal submission that [[walkah]] and I sent in. It was not accepted. I now call this [[Community Search Engines]].
# Community Search Engines: Event & Chat Artifacts as Research Building Block

## Team member names
* [Boris Mann](https://bmann.ca)
* [James Walker](https://walkah.net/)

The protocol of in-person conferences, symposium proceeedings, and other classic gatherings are at best stuck in a published PDF or slide deck world. If you're lucky, event websites have permalinks that remain year over year, and maybe a youtube playlist or two.

And, we have yet to develop a protocol that better supports digital communities, hybrid events, unconferences, and other emerging forms.

We propose a Community Search Engine Protocol for events & digital communities.

### Short summary of your improvement idea

Events, Cozy Web digital groups, and other gatherings are all flow, no stock. Every group should have access to easy tools to gather community context.

Part community search engine with high relevance resources from people you have trust with, part serendipitious discovery from webring surfing.

In the age of AI, leaning into a trusted community context can further help to elevate signal from noise.

### What is the existing target protocol you are hoping to improve or enhance?

Today's events, from meetups to traditional full conferences, at best use a static snapshot of an event websitem, slides, and speaker bios. If the event has enough funding ($1000s of dollars), there are high quality video recordings, and maybe some attempt is made at transcripts.

For [Open Space Technology](https://en.wikipedia.org/wiki/Open_space_technology) / unconference techniques, images of sticky notes and personal write ups, and perhaps professional facilitation summaries or live graphic facilitation could be part of the artifacts.

### What is the core idea or insight about potential improvement you want to pursue?

Digital gardens with valuable backlinks are stuck in single-player mode or commercial platforms. Chat communities, especially those on commercial platforms, are constantly losing context, or their entire archives. An easy toolkit for communities to gather context, resources, and new insights that can grow over time. Community Search in a box.

### What is your discovery methodology for investigating the current state of the target protocol?

We've run events and communities of this form for years. We will look to find other pains and problems by interviewing other community leaders and recruiting early testers.

### In what form will you prototype your improvement idea?

We will produce a toolchain of code and configuration as well as test installs of a community search engine.

Some of the building blocks we will look to use as starting points:

* [Lieu](https://github.com/cblgh/lieu) an existing open source community search engine
* The [Noosphere](https://subconscious.network/) tool-for-thought protocol
* Social feeds of community participants from Bluesky, ActivityPub, and Farcaster as a source of new resources
* RSS feeds that are aggregated and synced p2p as local resources for each person using IPFS -- both as distributed archive and way to include ongoing content over time

### How will you field-test your improvement idea?

**Causal Islands Toronto 2023:** [Causal Islands](https://causalislands.com) as a traditional centrally organized multi-day conference. The current archive, including high quality. It has spawned a Discord and Podcast and desire for more "Causal Islands" style events, including one "community edition" in LA. Participants have said they'd like to see more of these events, as well as better find a home for computational research / future of computing topics embodied by the original conference. 

Can we turn a conference into a community, and facilitate a template for future events?

We will start by using the 2023 event outputs, including inviting attendees of that event to add their personal resources, in creating a community search engine.

**The Discord formerly known as Fission:** Fission the company is shutting down, but the community Discord continues. Chat is notoriously bad at capturing long term context, and Discord as a commercial platform is not a good long term home.

We will explore extracting links and people into a community search engine.

This approach should be expandable to other Discord-based communities.

---

This approach may also be interesting for the SoP community itself.

We will look to recruit other communities to try out the process, including beta testing if technical people can effectively configure and deploy the tooling on their own, as well as differing approaches to activating the communities themselves.

### Who will be able to judge the quality of your output? Ideally name a few suitable judges.

* Gordon Brander
* Ronen Tamari

All of these might also be collaborators. Ideally communities and people who try and install / deploy this will be those who can help judge if it's helpful

### How will you publish and evangelize your improvement idea?

We will publish a repo containing the community search engine, configuration, and deployment guidelines to get up and running.

We will create an onboarding and community activation checklist to help communities be successful. 

We will find seed communities to deploy into, and host introductions and kick off events both virtually and in person.

### What is the success vision for your idea?

Communities of interest that form around events, digital places like chat groups, and other gatherings have an easy way to deploy a community search engine that provides both archival as well as ongoing high context trusted resources over time.