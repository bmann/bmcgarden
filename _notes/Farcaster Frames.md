---
link: https://docs.farcaster.xyz/reference/frames/spec
tags:
  - Farcaster
  - specification
  - frames
---
> Frames are a standard for creating interactive and authenticated experiences on Farcaster, embeddable in any Farcaster client.
> 
> A frame is a set of `<meta>` tags returned within the `<head>` of an HTML page. If a page contains all required frame properties, Farcaster apps will render the page as a frame. The frame `<meta>` tags extend the [[OpenGraph|OpenGraph protocol]].
> 
> Frames can be linked together to create dynamic applications embedded inside casts.

Inspired by [[David Furlough]]'s work on Mod, the Warpcast team created this Frames spec for the [[Farcaster]] protocol directly. David is working on [[Open Frames]] for use in Farcaster and beyond.

## Warpcast Testing Tools

* [Preview a frame](https://warpcast.com/~/developers/embeds) without having to cast
* [Frame validator](https://warpcast.com/~/developers/frames) to check that it's formatted correctly