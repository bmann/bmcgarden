---
---

git:: https://codeberg.org/silverpill/mitra
tags:: #ActivityPub, #Rust, #opensource

- From the README:
	- Federated micro-blogging platform and content subscription service.
	- Subscriptions provide a way to receive monthly payments from subscribers and to publish private content made exclusively for them.
	- Supported payment methods:
		- [Monero](https://www.getmonero.org/get-started/what-is-monero/)
		- [ERC-20](https://ethereum.org/en/developers/docs/standards/tokens/erc-20/) tokens (on Ethereum and other EVM-compatible blockchains)
	- Other features:
		- [Sign-in with a wallet](https://eips.ethereum.org/EIPS/eip-4361) #eip4361
		- Account migrations (from one server to another).
		- Donation buttons.
		- Token-gated registration (can be used to verify membership in some group or to stop bots).
		- Converting posts into NFTs.
		- Saving posts to IPFS.
	- Demo instance: [https://public.mitra.social/](https://public.mitra.social/) ([invite-only](https://public.mitra.social/about))
	- Network stats: [https://the-federation.info/mitra](https://the-federation.info/mitra)
	- Matrix chat: [#mitra:halogen.city](https://matrix.to/#/%23mitra:halogen.city)
	- ## [](https://codeberg.org/silverpill/mitra#code) Code
		- Server: [https://codeberg.org/silverpill/mitra](https://codeberg.org/silverpill/mitra)(this repo)
		- Web client: [https://codeberg.org/silverpill/mitra-web](https://codeberg.org/silverpill/mitra-web)
		- Ethereum contracts: [https://codeberg.org/silverpill/mitra-contracts](https://codeberg.org/silverpill/mitra-contracts)
	- ## [](https://codeberg.org/silverpill/mitra#requirements) Requirements
		- Rust 1.56+ (when building from source)
		- PostgreSQL 12+
		- IPFS node (optional, see [guide](https://codeberg.org/silverpill/mitra/src/branch/main/docs/ipfs.md))
		- Ethereum node (optional)
		- Monero node and Monero wallet (optional)