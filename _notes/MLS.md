---
title: Messaging Layer Security
aliases:
  - Messaging Layer Security
link: https://messaginglayersecurity.rocks
tags:
  - standards
  - e2ee
  - IETF
---
Messaging Layer Security (MLS) is an [IETF working group](https://datatracker.ietf.org/wg/mls/about/) building a modern, efficient, secure group messaging protocol.

From the FAQ: _Should I use this right now?_

> Yes! The protocol has been approved by the IESG and has been published as RFC9420. There are several [implementations](https://github.com/mlswg/mls-implementations), of which some are open source.

[List of existing MLS implementations](https://github.com/mlswg/mls-implementations/blob/main/implementation_list.md)

## Open Questions

Is MLS compatible with decentralized architectures?[^natanael]
* [federation spec](https://datatracker.ietf.org/doc/html/draft-ietf-mls-federation-00)
* [[p2panda]] is local first and p2p, and implements MLS - see [about page](https://p2panda.org/about/)
* [[Matrix]] has notes on [Decentralized MLS](https://gitlab.matrix.org/matrix-org/mls-ts/-/blob/decentralised2/decentralised.org)

[^natanael]: Thanks [Natanael](https://bsky.app/profile/natanael.bsky.social) for chasing down a bunch of these links

Does MLS hide metadata? That is, can we tell who is talking to each other?
* 