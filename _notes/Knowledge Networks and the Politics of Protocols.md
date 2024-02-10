---
link: https://blockscience.medium.com/knowledge-networks-and-the-politics-of-protocols-af81ad0fa2d4
tags:
  - article
  - opensource
via: https://social.coop/@christina/111908457043203535
published: 2024-02-08
author:
  - BlockScience
---
A lot of the things in here resonate with me, but I'm partially allergic to this kind of language. Here's the [discussion with Christina Bowen about it](https://social.coop/@christina/111908457043203535).

My blink reaction is "you're just describing open source software development" aka [[Commons Based Peer Production]].

Questions of protocol governance -- with the tensions between the protocol developer, the client application developer interacting with the protocol, and finally the end user of the client application -- are very real! 

A lot of the "who decides" / "how do we decide" questions of governance come from resources available. Ultimately, capital -- who can pay for development of features and implementation at various layers.

Some of the concepts that I am following that overlap with this include:

* [[Design for Deployment]]
* [[Bring Your Own Server]]

[[ActivityPub]] is a protocol going through this right now, especially with the [[Mastodon]] server and client interfaces having a major role. [[Threads.net]], Facebook's network that will be ActivityPub compatible, is looming and will have major impact.

My post on [[2022-01-15-networked-orgs-and-tooling|Networked Orgs and Tooling]] is related to this post as well. A set of networked orgs need to communicate, and so they need to choose platforms, protocols, and implementations.

> Building tools that allow users to provision, operate, maintain, and govern their own instances of an application is one of the most politically potent acts possible in open-source software development.

> Developers inevitably have to make subjective decisions that have downstream consequences, structuring and/or delimiting the action space available to users — hence cyborg anthropologist Amber Case’s claim that “design is governance.”[^1]

[^1]: [[Amber Case]] [How Design is Governance](https://uxdesign.cc/how-design-is-governance-7c8dd466d753)

> The goal of this initiative is to identify a “sweet spot” between designing for configurational freedom and designing for user-friendliness, so that the process of protocolization does not force users to choose between _software that is useful_ and _software that they can use_.

> _How can developers ensure that user-instanced open-source software is customizable enough to meet the needs and reflect the values of heterogeneous communities, but also sufficiently standardized to allow interoperability across instances — all while remaining easy to maintain?_

> The project at the center of our inquiry is perfectly suited to this purpose: BlockScience has developed an open-source knowledge management system (KMS) and knowledge organization infrastructure (KOI) for our own internal use[^3], employing an LLM as the interface to a database of our organizational knowledge, to anchor interactions within the scope of the content of the knowledge database and thus foster a genuine user interaction.

[^3]: [Constituting an AI: Accountability Lessons from an LLM Experiment](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4561433) - This paper explores an ethnographic study on an experiment conducted at an engineering services company called ‘BlockScience’. It focuses on the development and implications of 'constituting an AI' for accountability. The experiment integrated a pre-trained Large-Language Model (LLM) with an internal Knowledge Management System (KMS), making it accessible through a chat interface. By tracing the considerations of a group as they sought to design, deploy, and govern an AI, this research offers a foundational perspective to better understand accountability in human-AI interactions with organisational contexts. It also raises the need for further development of strategies to align AI technologies with human interests across various contexts.

This description most reminds me of a project that search company Algolia implemented -- using their own product -- inside their own organization [[How Algolia uses Electron to improve internal productivity]]. I see LLMs in part as "contextual search". Whether the Algolia project or what BlockScience is working on, I've very much wanted this both for myself as an individual (the bounds of info that I have access to) and for organizations that I'm a part of.

> We define self-infrastructuring[^6] as the ability of an organization to collectively design, own, govern, and maintain its own infrastructure. This concept underscores the significance of entities provisioning and operating their digital infrastructure, which is especially pivotal for entities whose ideals and objectives markedly diverge from those of external infrastructure providers. Due to the economics of scale, private digital infrastructure providers disproportionately serve majoritarian interests.

[^6]: [Web3 as ‘self-infrastructuring’: The challenge is how](https://journals.sagepub.com/doi/10.1177/20539517231159002), The term ‘Web3’ refers to the practices of participating in digital infrastructures through the ability to read, write and coordinate digital assets. Web3 is hailed as an alternative to the failings of big tech, offering a participatory mode of digital self-organizing and shared ownership of digital infrastructure through software-encoded governance rules and participatory practices. Yet, very few analytical frameworks have been presented in academic literature by which to approach Web3. This piece draws on the theoretical lens of infrastructure studies to offer an analytical framework to approach the emergent field of Web3 as an exploration in ‘how to infrastructure’ through prefigurative self-infrastructuring. Drawing on qualitative examples from digital ethnographic methods, I demonstrate how the origins of Web3 reveal the intentions of its creators as a political tool of prefiguration, yet its practices reveal the inherent tension of expressing these ideals in coherent technical and institutional infrastructure. Thus, I argue that one of the fundamental challenges Web3 is negotiating through technical and governance experiments is ‘how to self-infrastructure?’.

This overlaps with [[Self-hosting]], sort of.

> it unveils the inherent trade-offs between self-expression and operational ease, a dynamic that often propels entities to cede self-expression in favor of the convenience offered by Software as a Service (SaaS) tools.

> This exploration is poised to render self-managed infrastructural models viable for small research entities, thereby facilitating a more inclusive and diversified infrastructural landscape.

> the move to practice involves <mark>applying insights from the self-infrastructuring paradigm to the process of protocolizing open-source software</mark>, with the goal of enabling instances to interoperate while also adhering to (and representing) the divergent values and goals of different groups — and of different individuals within those groups.

I think what is meant by this highlighted part is that open source software most often is a single implementation with an API. Other instances of that software, running the same code, may interoperate. But without defining and separately maintaining a protocol specification, at best someone else writing another implementation (say, in a different programming language), must be "bug compatible" with the APIs of the original. And it makes the "original" software the locus of governance.

I'll put placeholder links here for my beliefs around [[Open Protocols are better than Open Source]] as well as [[S3 API as defacto protocol]].

> Our initiative will be successful if, at its conclusion, we have reached a richer understanding of the trade-offs between customizability and standardization in the specific context of knowledge commons and open-source AI-enhanced knowledge management software

> Ultimately, this work is about clarifying how open source digital infrastructure allows different organizations to organize themselves and their activities around non-identical worldviews, while retaining the ability to make common cause, or otherwise coordinate and collaborate in the world we all share.

> This research initiative is animated by a belief that open digital infrastructure should be treated as a public good, and our proposed work is meant to democratize access to digital resources and to catalyze innovation through collective societal engagement.