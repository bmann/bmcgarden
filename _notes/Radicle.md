---
link: https://radicle.xyz/
tags:
  - dweb
  - p2p
  - git
  - app
  - LoFi
  - DID
---
> Radicle is an open source, peer-to-peer code collaboration stack. It leverages Git’s architecture combined with cryptography and a gossip protocol to enable a fully sovereign developer stack.
## How it Works

The Radicle protocol leverages cryptographic identities for code and social artifacts, utilizes Git for efficient data transfer between peers, and employs a custom gossip protocol for exchanging repository metadata.

All social artifacts are stored in Git, and signed using public-key cryptography. Radicle verifies the authenticity and authorship of all data for you.

## Protocol Guide

More in the [Radicle Protocol Guide](https://radicle.xyz/guides/protocol), some quotes below:

> Radicle adopts a local-first, peer-to-peer (P2P) architecture, which draws inspiration from Secure Scuttlebutt (SSB) and Bitcoin’s [Lightning Network](https://en.wikipedia.org/wiki/Lightning_Network).

> Peer connections in Radicle are secured thanks to a [Noise protocol](http://www.noiseprotocol.org/noise.html) handshake. Radicle uses the [Noise XK](https://noiseexplorer.com/patterns/XK/) pattern specifically, just like the Lightning Network with the Node ID as the _static key_. This requires nodes to know the Node IDs of their peers before connecting to them, which takes place through the exchange of peer information over the gossip protocol.