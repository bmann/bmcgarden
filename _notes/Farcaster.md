---
tags:
  - protocol
  - web3
link: https://www.farcaster.xyz
---
> a protocol for building decentralized social apps

Farcaster IDs (FIDs) are stored on the Ethereum Optimism L2 blockchain, but everything else is offchain. 

From the [docs overview](https://docs.farcaster.xyz/learn/what-is-farcaster/overview):

> Farcaster is a [sufficiently decentralized](https://www.varunsrinivasan.com/2022/01/11/sufficient-decentralization-for-social-networks) social network built on Ethereum.
> 
> Users can create profiles, post short messages or "casts", follow others and organize into communities. It is a public social network similar in design to Twitter and Reddit.
> 
> Since Farcaster is public and decentralized, anyone can build an app to read and write data. Users own their accounts and relationships with other users and are free to move between different apps.

[[Warpcast]] is the original app built and run by the team that designed the Farcaster protocol. 
## Frames

Frames extend the [[OpenGraph]] standard and turn static embeds into interactive experiences. 

Example:

```html
<meta property="fc:frame" content="vNext" />
<meta property="fc:frame:image" content="http://...image-question.png" />
<meta property="fc:frame:button:1" content="Green" />
<meta property="fc:frame:button:2" content="Purple" />
<meta property="fc:frame:button:3" content="Red" />
<meta property="fc:frame:button:4" content="Blue" />
```

If you share the URL of a page in a cast that has these meta tags, it will show up as a frame. 

See [[Farcaster Frames]] and [[Open Frames]]