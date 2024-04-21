---
tags:
  - ATProtocol
  - premiumcontent
---
[[Bluesky]] already has built in support for [[Bluesky#Custom Feeds|custom feeds]]. Could this be used to create premium content feeds?

This could look like subscribers-only content, but available and readable directly within Bluesky or any [[ATProtocol]] that supports custom feeds.

This is most relevant for a kind of ATProtocol-based "subscribe to my blog or newsletter" integration -- [[Substack]] or [[Ghost]] being two common paid subscriber platforms.

I'll use Ghost as my example.

- The "My Cool Ghost Site" has both free and paid memberships; some content is available to all members -- sent via email, in RSS, and posted to the blog
- Paid members get access to premium content -- they get it sent via email and/or can login to the Ghost blog to read it
- assuming Ghost / a custom plugin has a feature to link your Ghost membership with your Bluesky login
- The plugin would also generate endpoints for a Bluesky compatible custom feed
- The algorithm is pretty simple here -- if the currently logged in user is a paid member, show them free and premium content; else, only show free content

Right now all content is public on Bluesky, so you could still fetch the content / navigate to it. In fact, can you generate posts in a custom feed??? Or does it first have to be posted to an account, so that it could be included?

Maybe something with blocks? Have a free Bluesky account,  `@my-cool-ghost-site.com`, and a premium one, `@members.my-cool-ghost-site.com`. When someone adds the custom feed, if they aren't a paid member, block them.

Blocking everyone on Bluesky (pre-emptively!) except for subscribers is not really a great method. This is probably another area where a Lexicon that supports premium content could be used.

And, this might just be way easier to implement by adding [[Open Frames for Bluesky]].