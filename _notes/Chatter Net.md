---
---

tags:: #protocol, #DID, #ActivityStreams

- From README of the client repo https://github.com/chatternet/chatternet-client-http
- Chatter Net is a modern decentralized semantic web built atop [[self-sovereign identity]].
- For more, you can have a look at the sibling [server project](https://github.com/chatternet/chatternet-server-http), and a prototype work-in-progress [social application]([[Conversely]]) used to dog food the development process.
- ## Project Objectives
	- Chatter Net is a platform which is:
	- **Open**: anyone can participate in, extend, and innovate on the platform.
	- **Decentralized**: there is no central point of failure. Network consensus determines what content arrives to a user.
	- **Self-moderating**: a user has enough control over what they receive to reject spam content.
	- Chatter Net aims to solve the problem of central ownership of user identity. There are currently few organizations which control the vast majority of the identities of online users. When the objectives of these organizations and those of the users become misaligned, this can cause major problems for the users.
	- After investing 100s or 1000s of hours into building a network and content on a platform, a user might be banned from the platform with no appeal process, a user's content might be subject to summarily deleted or otherwise made inaccessible with no explanation, a user might be asked to pay fees to continue accessing the content and network they built themselves, etc.
	- The proposed solution is simple: allow a user to prove their identity to other users without relying on a 3rd party; and allow users verify the origin of some content without relying on a 3rd party.
- Data Model
	- [[ActivityStreams]] is semantic, self-describing JSON data format. It can be used to describe arbitrary data as well as interactions between actors and the data.
- Identity
	- The [DID Key](https://github.com/digitalbazaar/did-method-key/) standard uses public-private key pair cryptography to prove identity. An account is created locally by a user, and the private key created by that user allows them to prove their identity. [Verifiable Credential Proofs](https://w3c.github.io/vc-data-integrity/) allow the users to verify the authenticity of messages.
	  id:: 63e09982-0080-45ea-8c84-9c6b28ca3156
- Networking
	- Chatter Net does not rely on a specific network stack or protocol. It is instead specified by its *data model*. It would be possible (though prohibitively slow) to operate a Chatter Net network using carrier pigeons.
	- This library includes client functionality to communicate with a network of [HTTP servers](https://github.com/chatternet/chatternet-server-http/). Other network implementations could be added in the future.