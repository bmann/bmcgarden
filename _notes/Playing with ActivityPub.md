---
---

link:: https://macwright.com/2022/12/09/activitypub.html

- published:: [[Dec 9th, 2022]]
- author:: [[Tom Macwright]]
- tags:: #ActivityPub, #Netlify
- Looked at [[Darius Kazemi]]’s #NodeJS AP implementation as a reference
- > So, the whole time I was doing this I was looking at [express-activitypub](https://github.com/dariusk/express-activitypub), one of Darius’s projects. It’s great - simple, but it works. Most of my work here was making it even simpler - removing some of the configurability and hardcoding things like accounts - and porting code that was dependent on Node.js to code that could run in Netlify’s edge functions, which are a whitelabeled layer on top of [Deno](https://deno.land/) and thus use standard web APIs instead.
-