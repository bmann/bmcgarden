---
---

alias:: Locutus
tags:: #[[key-value database]], #Wasm

- Old Freenet is being renamed to Freenet Classic
- New Freenet will be Locutus
- From the [GitHub README](https://github.com/freenet/locutus):
	- Locutus is a decentralized key-value database. It uses the same [small world](https://freenetproject.org/assets/papers/lic.pdf) routing algorithm as the original Freenet design, but each key is a cryptographic contract implemented in [Web Assembly](https://webassembly.org/), and the value associated with each contract is called its *state*. The role of the cryptographic contract is to specify what state is allowed for this contract, and how the state is modified.
	  id:: 63e6665e-4a45-4ea5-a476-687e227caf78
	- A very simple contract might require that the state is a list of messages, each signed with a specific cryptographic keypair. The state can be updated to add new messages if appropriately signed. Something like this could serve as the basis for a blog or Twitter feed.
	- Locutus is implemented in Rust and will be available across all major operating systems, desktop and mobile.
	  id:: 315633de-a53c-444f-bec5-f964d8030e9c