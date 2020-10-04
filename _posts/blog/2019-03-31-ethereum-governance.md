---
layout: post
title: "Ethereum Governance"
excerpt: "An explanation of different layers of Ethereum Governance: open source collaboration, protocol standards governance, Core Dev coordination, nodes running client software, plus extended reading and links."
modified: '2019-04-01T10:48:34-07:00'
categories:
- Commons
tags:
- "open source"
- governance
- Ethereum
- blockchain
- EthMagicians
comments: true
---
This is my attempt to write up an overview of the different layers of governance that applies to Ethereum. The core concepts and further discussion are also [posted to the Ethereum Magicians forum](https://ethereum-magicians.org/t/definitions-of-governance-layers/3054).

You can [read about my journey into the Ethereum Community](#boriseth) at the end of the article if you would like some context. I'm relatively new, but have a long experience with open source collaboration, including having helped form the Drupal Association that helps support the Drupal CMS.

Ethereum is a number of different things:

1. There is the [Ethereum Foundation](https://ethereum.foundation/)[^efdated], aka Stiftung Ethereum, which is a Swiss foundation that was formed to help run the crowdsale and initially boot up the network. It holds the trademark for Ethereum. It manages a number of pieces of community infrastructure and employs / contracts several teams working on major software for Ethereum, from [testing frameworks](https://github.com/ethereum/testing) to the [Geth client](https://github.com/ethereum/go-ethereum). Currently it employs or invests in researchers and teams doing the primary cryptographic / blockchain research for future innovations, now mainly focused on ETH2[^efresearch]. It also runs the "official" developer conference ("DevCon") that happens annually. The Ethereum Foundation does _not_ control the technical direction of the network.
1. Ethereum is a set of protocols, from the [Ethereum Virtual Machine (EVM)](https://en.ethereum.wiki/evm) that underlies the smart contract system and many core features, to the [devp2p](https://github.com/ethereum/devp2p) peer communications protocol, to the [JSON-RPC middleware](https://github.com/spadebuilders/ethereum-json-rpc-spec) for getting data in and out of nodes.
1. Ethereum is a main-net global public blockchain, operated by 1000s of nodes worldwide, transactions processed & secured in exchange for a block reward by miners calculating a proof-of-work algorithm with hash power. It has the ETH ticker symbol for its core cryptocurrency which is used to pay for gas charges on smart contracts and transactions, and as value within the network. The network can be reached with chain id 1 and network id 1[^chainid].
1. Ethereum is a community, which wants to keep building on the Ethereum protocols, distributed applications on top, and related decentralized web protocols. It congregates mainly on main-net, but over time increasingly also builds side-chains, layer 2 protocols, and more.

Now that we've got some foundational information in place, let's look at the layers of governance. These are listed roughly in order, although higher layers do loop back to lower level layers.

[^efresearch]: Thanks to [Tim Beiko for suggesting I add research as an EF activity](https://ethereum-magicians.org/t/definitions-of-governance-layers/3054/3). Clearly spelling out what the community thinks the EF does / is responsible would be a very valuable discussion to have, but is not the core thrust of this post.

[^efdated]: The material on the [Ethereum Foundation site](https://ethereum.foundation/) is out of date, but I link to it as the primary reference that refers only to the foundation. The ethereum.org is considered more of a community resource, although sadly at time of writing it, too, is several years out of date.

[^chainid]: Visit [chainid.network](https://chainid.network) for more information on all the chains that run Ethereum protocols and their corresponding chain- and network-ids. I help maintain this site.

## Open Source Collaboration

Open source is in reality a shorthand phrase that means a couple of things: a license, a way of working, and an ideology, as covered by me in [Blockchain & Open Source Definitions](/blockchain-open-source-definitions/). My follow up on [Commons Based Peer Production](/commons-based-peer-production/) uses the long form of how to describe the way that open source licensed code is managed: maintainers, issues, pull requests, forks (the good kind and the bad kind), and a global community of users and contributors.

The Ethereum wiki has a [list of the ETH1 clients](https://en.ethereum.wiki/eth1/clients)[^ethwiki] -- as you can see, the majority today are managed by the Ethereum Foundation, although in practice the individual teams and contributors run the projects on their own, relatively independently, although many of them are paid by the EF as employees or contractors. The Parity Ethereum client (owned by Parity Technologies) and the new PegaSys Pantheon client (owned by ConsenSys) are the two notable exceptions. These other two clients are also considered "major" clients, as they are actively maintained and are used to run nodes that connect to the main-net. The Nimbus client by Status is on its way as well, so we can see that diversity of ownership is increasing. The [early list of ETH2 Beacon Chain implementations](https://en.ethereum.wiki/eth2/clients) highlights this as well.

All of the Ethereum clients are managed as open source projects, with varying amounts of organic contributor contributions. When we say "managed as open source", this means that issues representing bugs or feature requests can be filed by anyone, anyone can submit code fixes or new features using pull requests, and a group of maintainers manage these processes. Maintainers are those that have write access to the code repository and/or can help with management of the issue queue. Maintainers may be paid by a single organization, or unpaid volunteers.

The software license does matter, and much of the Ethereum stack today is strong copy-left. This limits the interest and/or ability of many corporate organizations to participate directly. On the other hand, if the main copyright holder of the software sells licenses to corporations, this may provide a stream of funding. This is something the entire open source software ecosystem is currently wrestling with[^kemitchell].

My recommendation in this area is to move to Apache2, as it is broadly permissive in a way that is compatible with corporations, and includes patent protections.

In many ways, those of us in open source for a long time have "won" -- Microsoft bought Github and aims to be the most open company in the world -- but at the same time, many of the core norms of open source are no longer being taught, even to developers. I think we can do more here, and would love to work on onboarding more new developers to become valuable developers to the core Ethereum stack, as well as the emerging ETH2 stack to build our next generation of experts.

In summary, if you are a business person or other non-technical role, having an understanding of the norms and processes around open source software development is critical. Open source software powers not only virtually all blockchain technology, but the vast majority of the software that runs the world at this point.

[^ethwiki]: I help maintain that particular page, but the whole thing is editable by anyone, and the [code](https://github.com/ethresearch/en-ethereum-wiki) is managed by [Virgil Griffith @virgilgr](https://twitter.com/virgilgr), who works for the EthResearch arm of the Ethereum Foundation.

[^kemitchell]: If you really want to go down this rabbit hole, [read expert software licensing lawyer Kyle Mitchell](https://writing.kemitchell.com), who himself has proposed a number of new licenses.

## Protocol Standards Governance

The Ethereum Improvement Proposal (EIP) process is what is used to propose and agree on standards. Broadly speaking, protocol standards governance. These standards apply at both the Ethereum software level (clients implementing interoperable software) and also at the network layer. When I say network layer -- that means the Ethereum network -- but also other Ethereum networks. Other networks may follow Ethereum main-nets inclusion and adoption of EIPs directly (most do, today), or also extend the process with their own improvement process.

For now, lets consider the EIP process as targeted at making standards that are primarily designed for the Ethereum main-net. Whether or not they are developer and deployed to the main-net is another matter.

You can browse all published EIPs on the [EIPs website eips.ethereum.org](https://eips.ethereum.org)[^eipswebsite]. The process for submitting EIPs and the stages they go through for Core EIPs (those that would change consensus on the network, and need to be agreed upon to be deployed) and all other types is documented in [EIP-1](https://eips.ethereum.org/EIPS/eip-1).

There are also application-layer standards in the EIPs repo, known as Ethereum Request for Comments (ERCs). These ERCs may be split out into a separate repo and process (something that I am in favour of).

Very roughly, the process of creating and submitting an EIP is open to everyone and relatively simple, although it does require some knowledge of GitHub. No coding is required. One uses the template, creates a text document formatted with Markdown, and submits a pull request on GitHub to suggest it as a Draft. If the EIP is formatted correctly, it is merged into the repo, which generates a web page for that EIP, and further discussion can continue. Some EIP editor discretion is available, but so far there hasn't been much in the way of "spam" -- plainly ridiculous EIPs. Getting the formatting right and learning GitHub have been a high enough barrier.

A lot of that is very process focused. An important thing to understand is that this process and some of the technical processes around it are informed by the Internet Engineering Task Force, or [IETF](#ietf) (that link leads to more reading and links that I've included below). Building one -- or several! -- global networks is a similar task, so it is likely that similar techniques are part of best practices for moving protocol standards around blockchain networks forward.

I think the EIPs process works quite well, and is only improving. More education, especially for technically proficient developers who can add value to the network, would still be better.

[^eipswebsite]: The EIPs website is generated from the [GitHub repo ethereum/EIPs](https://github.com/ethereum/EIPS) and hosted on GitHub Pages, which is powered by the [Jekyll](https://jekyllrb.org) static site generator.

---

[Andrew @cyber_hokie](https://twitter.com/cyber_hokie) has been participating as long as I started dropping in to [Gitter ethereum/governance](https://gitter.im/ethereum/governance): right before the EthMagicians Council of Berlin in June 2018, when some pre-emptive blog posts went up about fund recovery.

He's been very active again recently, and wrote up a really great tweetstorm that is an excellent overview of how the EIPs process isn't itself overall network governance, but rather part of the standards process.

I'm going to include his tweetstorm here directly:

<div id="tttt_1112305608047427584" data-option="1"><strong><a href="https://threadreaderapp.com/thread/1112305608047427584.html">Thread by @cyber_hokie: "1/ Ok I think I sort of get it now. Thanks @nicksdjohnson for bearing with me. A longish thread. […]" #eipsarentgovernance #eipsaretechnicalstandards #META</a></strong></div><script async src="https://threadreaderapp.com/embed/1112305608047427584.js" charset="utf-8"></script>


---

The EIPs process is for standardization -- for making sure that software is developed that is interoperable and can be implemented by multiple groups. With Ethereum having a number of different clients, this is crucial. In fact, it's more crucial than the license of the software. If there is a good standard, then anyone can implement it and know they are interoperable.

There is a movement that is just beginning to have dedicated maintainers and repositories for different parts of the Ethereum stack -- the EVM, devp2p, the JSON-RPC interface, and so on. This means that even more collaborators can work together, even beyond the boundaries of Ethereum main-net, to improve and be interoperable.

## Core Devs Coordination

Andrew's thread covers the AllCoreDev calls, as a place where coordination happens among the developers of major client implementations. These happen every two weeks, facilitated by Hudson Jamieson, who works for the Ethereum Foundation full time.

The same core agenda is made in a Github repo, [ethereum/PM](https://github.com/ethereum/pm), as an issue. Anyone can make a comment in the issue suggesting that they have time to speak and bring up an issue or share something with the group.

On the day of the calls, the link to join the call directly is posted in the [AllCoreDevs Gitter](https://gitter.im/ethereum/AllCoreDevs), and the whole call is also livestreamed and recorded.

As a whole, this process is meant to be technically focused. The concern of the Core Devs are the technical correctness of a particular EIP, as well as on a broader scale certain "health of the network" features. Of course, every technical decision can have non-technical implications, and this fuzzy line is where problems have started.

Core Devs have indicated that they don't want to make decisions that are non-technical. The people involved are mainly highly technical, interested in the challenges around global blockchain network development. They aren't facilitation experts or community engagement experts. Even as open source maintainers, we haven't seen the client code be very active.

Having spoken with individual client teams, the feedback is that code implementation really doesn't take a lot of time: forward progress is being limited by non-technical decisions making and roadmap arguments _today_.

What process is used for Core Devs to make decisions? Well, it's kind of a "live" version of the EIP process, except with the nuance of a live discussion every two weeks. What I mean by this is that IETF-style, rough consensus and running code, is what constitutes agreement. Recent discussions indicate that adding a bit more formality -- calling for consensus and recording discussions -- may be needed to remove uncertainty.

Useful to understand the EIP and Core Dev flows is [Dan Finlay's process flow diagram](https://ethereum-magicians.org/t/strange-loop-an-ethereum-governance-framework-proposal/268). I've included it directly here:

![](/images/2019-03-31/danfinlay_governance_flow.png)

## Network Governance

I'm going to use the term "network governance" to indicate governance that applies to the entire main-net Ethereum network. This is espressly bigger than "just technical".

From all of the previous methods -- open Source collaboration to protocol standards to Core Dev coordination -- these are all quite technical processes. There is a limit to how much you can contribute without writing lines of code, or pooling funds and hiring developers.

What is the responsibility of the Ethereum network to stakeholder engagement? If "we" want broader stakeholder participation, how do we accomplish that?

A note on "we": I'll define this as the broad set of people that define themselves as part of the Ethereum ecosystem, and care about its functioning and further evolution. **ALL** of the methods of interaction are currently on a step-up-and-get-it-done, volunteer basis (as is natural for open source communities). As far as I know, Hudson Jamieson is the only full time paid person in the entire ecosystem dedicated to community. And even there, the majority of his time is spent around Core Devs Coordination.

A lot of the recent friction has been about understanding where network governance sits in the process, how it gets implemented, and who gets to participate / how voices get heard.

One point of view is that "stakeholders should self organize". I believe in this, but I also believe that we can welcome people to use some existing infrastructure and channels.

The smallest unit of decision making we have at this point are Core EIPs: EIPs that affect the core functioning of the network, that major clients must implement if it is to be deployed, and must be proposed to be included in a hardfork in order to be active on the network. This seems like the best place to gather sentiment around. The [Tennagraph tennagraph.com](https://tennagraph.com) app is the first place where broader feedback can be gathered on a per-EIP basis. It, too, is open source software that got a little grant to get started, but welcomes help and participation. Check out the [issue queue on Github](https://github.com/TennaGraph/TennaGraph/issues) -- even going through and leaving a comment on items that are important to you (or hearting them!) helps the contributors prioritize and learn from users.

I don't think placing network governance "before" protocol standards or Core Devs makes sense. It's much more of a simultaneous process. We as a technical community can do better at indicating what upcoming Core EIPs are, so a wider group of stakeholders can inform themselves. The Ethereum Magicians forum now as a [Core EIPs category](https://ethereum-magicians.org/c/eips/core-eips). I still have some work to do to upgrade the EIPs website so it can have a feed of just Core EIPs.

From what I can see, right now network governance mainly occurs by sowing doubt in the minds of Core Devs. Since Core Devs care about the health of the network -- including not wanting to necessarily have a contentious hard fork -- they can then speak up and break consensus. However, this mainly just means that EIPs are not implemented: saying "yes" is a lot harder.

I think the discussions around broader stakeholder interactions around network governance are just beginning. For now, the other processes will move along, and unless stakeholders raise their voices on a per EIP basis, that process will continue. I am happy to assist in network governance efforts by educating, assisting with events, and translating from technical to non-technical, but this is not an area I am interested in leading efforts on directly. (just to make my own stance clear!)

## Nodes Running Client Software

Ultimately, the core of decentralized blockchain networks today is that anyone can run a node, and anyone can choose which version of open source client software to run. This includes forking the client codebase to make your own, or running an old version or patched version that differs from "the majority".

From there, hashpower of miners and node operators may determine what the consensus chain is, which may cause a split into more than one "viable" chain.

## Ethereum Roadmap

The other issue beyond individual EIPs is the roadmap for Ethereum. This was first brought up at the EthMagicians Council of Berlin, and increasingly there have been events, calls, and discussions where long term roadmap discussions are held.

No one is "in charge" of the Ethereum roadmap, as it is composed of all of the previous items once again.

But, it is important to highlight what has become known as ETH1x and ETH2.

The next version of the Etherem network, ETH2 for short, is meant to be fully built on proof-of-stake rather than miner hashpower operating on a proof-of-work algorithm. It also features sharding, with multiple shards that make up the entire network, leading to much greater scalability of the network as a whole. This is still primarily driven by researchers, funded primarily by the Ethereum Foundation. There are initial implementors that are working on Phase 0, the Beacon Chain, with Phases 1 and 2 still to come. There is no EIP process, mainly implementors and researchers coordinating on the specification.

Initially, the narrative was that ETH2 and proof-of-stake were right around the corner. Now, I don't think it's controversial for me to say that it is likely 3 years away from a full production roll out, as there are still multiple unknowns and open research questions in Phases 1 & 2.

In the meantime, attention kind of fell away from the current chain. But it's the only chain we've got, and it _is_ the network until there is another one to migrate to or integrate with. Hence, a movement beginning in Prague around DevCon in November 2018, and now momentum of its own, to improve and evolve the ETH1x chain. I am a proponent of making these improvements now -- and learning how to make them -- in order to take those learnings and apply them to future chains as well.

One of the upcoming meta-discussions is whether many small hardforks should be planned, or fewer larger ones. Right now, consensus seems to be leaning towards more frequent, smaller hardforks.

For more info, see the Ethereum wiki [Roadmap page](https://en.ethereum.wiki/roadmap) and the upcoming [Istanbul October 2019 hardfork](https://en.ethereum.wiki/roadmap/istanbul).

## How to get Involved

If you've read all this, you might want to get involved in the Ethereum community!

I spend the vast majority of my time in the [EthMagicians Discourse Forum](https://ethereum-magicians.org), which has the benefit of long form writing and threaded discussion. It has also become a hub for discussion around EIPs -- moving out of GitHub Issues which are less accessible, and don't support threaded discussion.

I also organize community calls, events, and work on standards, including improving the EIPs repo and making connections to wider users of the Ethereum protocol stack, such as the Enterprise Ethereum Alliance or the [RUN EVM](https://runevm.com) event I'm organizing in Berlin.

Even as a person with a non-technical background, learning Github is a useful super power. Issues and project tools are pretty much like a shared to do / project management system that anyone comfortable with web apps can learn. I am trying to collaborate with more people on using the [EthMagicians Issue Queue](https://github.com/ethereum-magicians/scrolls/issues) to make calls for volunteers and to get work done.

Bottom line: lots of ways to move beyond Twitter or other social media short posts to longer discussion, collaboration, and -- most importantly! -- filing issues, asking for accountability, and getting stuff done!

---

## Boris in the Ethereum Community
<a name="boriseth"/>

[Bob Summerwill](https://twitter.com/bobsummerwill) sat me down and explained the Ethereum world computer to me when he was working for the Ethereum Foundation in early 2016. I got intrigued, bought some ETH on Coinbase (because I needed it for launching contracts via Mist) and started tinkering a bit. In 2017 I founded a company and worked on a variety of things, including a security token issuance platform.

I dove into the deep end of the core Ethereum community starting May 2018. I had been talking to [Richard Burton](https://twitter.com/ricburton) from Balance and others about getting together discussion around wallets and wallet standards, that I was calling [WalletConf](https://twitter.com/WalletConf).

Conveniently, I bumped into the Kyokan and Thunder Token folks who were thinking the same thing, and so I got to attend and then [help document the proceedings](https://ethereum-magicians.org/t/thoughts-and-findings-from-the-web3-uxunconf/311).

That documentation on EthMagicians meant that I "met" a bunch of other people that were interested in the same thing. Having met a number of people in person at the WalletConf event in Toronto meant that I already had some "social proof" that carried over to my online interactions. I had previously attempted to enter the [Ethereum Reddit community /r/ethereum](https://reddit.com/r/ethereum), but had been unable to get comments or posts approved and couldn't figure out how Reddit karma worked, so I ignored it. I'm also from a pre-Reddit age, so I never really spend much time on that system.

I then went on to help organize the EthMagicians Council of Berlin and generally used it as a way to meet and learn more about the community. I was in transition from my previous company and spending the summer in Berlin, so I had free time to commit to this. And, my background in open source projects and organizing unconferences meant that I had some familiarity with the subject matter.

In Q4 of last year, I [cofounded a company dedicated to working on open source, SPADE](/hello-spade/). The open source standards and products we work on we call [FISSION](https://fission.codes). We were lucky enough to get an open source grant as part of the [ConsenSys Tachyon accelerator](https://fission.codes/post/consensys-tachyon), which has given my cofounder Brooke & I some funding to work on open source and community. We make money through software R&D consulting and some [hosted services we're planning to launch](https://www.producthunt.com/upcoming/fission-tools/). We continue to apply for grants, as this allows us to work on open source projects that are valuable to the community, rather than client consulting.

---

## Further Reading

Vlad Zamfir's [Blockchain Governance 101](https://blog.goodaudience.com/blockchain-governance-101-eea5201d7992) and then the follow up where he [admits to his own intentions](https://medium.com/@Vlad_Zamfir/my-intentions-for-blockchain-governance-801d19d378e5) are good reading for thinking about the landscape of possible blockchain governance directions.

I read it and recognized that Ethereum is headed for "dev capture", and that I could work to help prevent that.

### IETF
<a name="ietf"/>

If you don't know much about the Internet Engineering Task Force (IETF), finding out how it governs and manages the development of core Internet standards is useful reading. The [About page](https://www.ietf.org/about/) is a good starting point. From there, [Getting Started in the IETF](https://www.ietf.org/about/participate/get-started/), where I'll quote the opening paragraph:

> The IETF's mission is "to make the Internet work better," but it is the Internet _Engineering_ Task Force, so this means: make the Internet work better from an engineering point of view. **We try to avoid policy and business questions, as much as possible.** Most participants in the IETF are engineers with knowledge of networking protocols and software. Many of them know a lot about networking hardware too.

Emphasis mine, and now some of the background of the EIP process -- and the Core Dev Calls -- should be clearer.

A motto of the IETF is "rough consensus and running code". There is an RFC published in 2014 called [On Consensus and Humming in the IETF](https://tools.ietf.org/html/rfc7282) that expands on this.

### NANOG

[NANOG](https://www.nanog.org/) stands for "North American Network Operators Group". It has been around almost as long as the IETF has. From the about page:

>The North American Network Operators Group (NANOG), is the professional association for Internet engineering, architecture and operations. Our core focus is on continuous improvement of the data transmission technologies, practices, and facilities that make the Internet function.
>
>NANOG is a membership organization organized as an 501(c)3 non-profit.
>
>Our members are typically drawn from the core engineering and product staffs of the major North American carriers, content providers, hosting and cloud companies, multi-tenant data centers, and interconnection service providers. NANOG is governed by the NANOG Board of Directors, elected by the membership, every two years.

This might be equivalent to people who run node clients, in an understanding of how such groups might organize as a stakeholder group.
