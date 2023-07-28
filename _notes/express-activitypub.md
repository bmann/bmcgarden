---
---

author:: [[Darius Kazemi]]
tags:: #opensource, #ActivityPub, #NodeJS
github:: https://github.com/dariusk/express-activitypub

- A very simple reference implementation of an [[ActivityPub/Server]] using Express.js that supports:
	- creation of new Actors via API
	- discovery of our Actors via webfinger (so you can find these accounts from other instances)
	- notifying followers of new posts (so new posts show up in their timeline)
- *This is meant as a reference implementation!* This code implements a very small subset of ActivityPub and is supposed to help you get your bearings when it comes to making your own barebones ActivityPub support in your own projects. (Of course you can still fork this and start building on it as well, but it's not exactly hardened production code.)
-