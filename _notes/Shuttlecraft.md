---
---

link:: https://shuttlecraft.net
github:: https://github.com/benbrown/shuttlecraft
tags:: #opensource, #ActivityPub, #microblog, #NodeJS
author:: [[Ben Brown]]

- A single user [[ActivityPub/Server]]
- Intro video https://www.loom.com/share/a6441bcebdc64f54b5010c95eae1e180
- Currently, this means:
	- a stand-alone NodeJS web application
	- with no external service dependencies
	- that is hostable on Glitch or commodity virtualhost
- Including features:
	- Follow people (on Mastodon, other instances)
	- Compose posts and deliver on the web, and also via ActivityPub, RSS
	- Fave, boost and reply to posts
	- View notifications
	- Send and receive DMs
	- Block people or instances
- Not yet supported:
	- Incoming updates and deletes
	- Media uploads
- Built on [[Darius Kazemi]]’s [[express-activitypub]] project
-