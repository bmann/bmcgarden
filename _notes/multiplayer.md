---
---

- The reference comes from gaming, where multi player technology was/is hard and different than #[[single player]] experiences
  title:: multiplayer
- Has come to mean
- [[Dec 4th, 2022]] [[Mark Upton]] kicked this off in a #[[Tools for Thought Rocks]] [thread on Mastodon](https://toolsforthought.rocks/@mark/109458959685234385):
  id:: 63b705ac-2245-46c8-a50f-6e70920e38e5
	- Question for the [#ToolsForThought](https://toolsforthought.rocks/tags/ToolsForThought) community:
	  
	  What is the origin/history/evolution of the term "multiplayer" in relation to TFT?
	  
	  ...and has it stabilised around a consistent/shared meaning?
- My [answer](https://toolsforthought.rocks/@boris/109459449891400199):
	- 1) multiplayer notes == multiple people editing multiple documents over time (eg Notion, many hosted wikis, some sort of git process)
	  
	  2) collaborative editing == real time editing of one document by multiple people
	  
	  I think (1) is rare because the space is so fixated on Markdown and files on disk.
- [[Gordon Brander]]'s first post on the [[Subconscious]] Substack included it
	- ((63b708b2-da9e-4394-b134-339f40fd0b43))
- Me [on Mastodon](https://toolsforthought.rocks/@boris/109525981803037278):
	- So putting collaborative real time aside, multiplayer asynch needs:
	- a common user account layer
		- a sync protocol
		- some way of displaying changes / versions / edits / annotations by others, ideally labeled in such a way that you can tell who did them
		- permissions
		- notifications
	- I n a centralized server architecture this is easy — everyone has user accounts and all data is in the database and the app takes care of everything. aka “most SaaS apps today”