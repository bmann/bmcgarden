---
---

link:: https://matrix.org/blog/2022/12/25/the-matrix-holiday-update-2022
tags:: #article, #Matrix
published:: [[Dec 25th, 2022]]

- 44M to 80M Matrix IDs in the main global network
- id:: 63af8f03-71a9-4ae0-96d0-20f8af929184
  > We’ve seen an amazing number of major new players entering the Matrix ecosystem: [Reddit appears to be building out new Chat](https://macaw.social/@wongmjane/109529583352532543) functionality using Matrix; [TeamSpeak announced](https://twitter.com/teamspeak/status/1589621116032585728) Matrix-based chat in TS5; [Discourse](https://meta.discourse.org/t/matrix-protocol-for-chat/210780) is working on adding Matrix support; [Thunderbird](https://www.theregister.com/2022/06/30/thunderbird_102) launched Matrix support;
- Lots of government usage and adoption
- > On the other hand, only a handful of these initiatives have resulted in funding reaching the core Matrix team. **This is directly putting core Matrix development at risk.** We are witnessing a classic tragedy of the commons. We’ve released all the foundational code of Matrix as permissively-licensed open source and got it to the point that anyone can successfully run it at scale themselves. The network is expanding exponentially. ==But in return, it transpires that the vast majority of these commercial deployments fail to contribute financially to the Matrix Foundation - whether by donating directly or supporting indirectly by working with [Element](https://element.io/), who fund the vast majority of core Matrix development today.==
- > The only viable solution to this is for organisations building on Matrix to contribute to sharing the costs of maintaining Matrix’s core projects. We made [a proposal](https://matrix.org/blog/2022/12/01/funding-matrix-via-the-matrix-org-foundation) to address this a few weeks ago, which we’ll iterate on further in the new year to find an approach which both empowers the community and encourages organisations to participate.
- [Funding Matrix via the Matrix.org Foundation](https://matrix.org/blog/2022/12/01/funding-matrix-via-the-matrix-org-foundation) [[Matrix/Foundation]] #[[commons funding]]
  id:: 63af8fdc-e22d-489d-8aea-4274afa29bde
	- id:: 63af9052-c017-4b56-8e28-72d1d16f7720
	  > To put it in perspective, even though there are over 5000 contributors to [github.com/matrix-org](https://github.com/matrix-org) - over 90% of the actual committed lines of code come from Element employees. Similarly, while we are *enormously* thankful for the past and existing generous donations from the wider Matrix community, today they only come to $6,000 a month, relative to the $400,000 a month that Element has been funding.
- Long list of work the Matrix Foundation does, including 240 repos in the GitHub org
- > Another big project in 2022 has been to create a general purpose Rich Text Editor to provide WYSIWYG (What You See Is What You Get) message composition for Matrix clients. This has ended up being a very ambitious project to define all the core editing semantics in a shared rust library, with platform-specific bindings to link it into the editing UI available on Web, iOS & Android. The end result lives at [https://github.com/matrix-org/matrix-rich-text-editor](https://github.com/matrix-org/matrix-rich-text-editor)
- Tried this on mobile and it seems pretty terrible, but I’m excited by the concept of a #Rust -based rich text editor with #Wasm
- [[OpenID Connect]] as default login method — and tracking progress https://areweoidcyet.com
- > The team also went on a very exciting detour to figure out how to perform login-and-E2EE-setup in a single operation by scanning a QR code ([MSC3906](https://github.com/matrix-org/matrix-spec-proposals/pull/3906)), and how it might integrate into OIDC in future.
- > Another massive new initiative this year has been the process of proposing Matrix to the IETF as a candidate for use in interoperable instant messaging standardisation. The [MIMI (More Instant Messaging Interoperability) working group](https://datatracker.ietf.org/group/mimi/about/) emerged earlier in the year within IETF as an initiative to define how MLS could be used to interoperate between different instant messaging silos
-