---
title: Wiki
---

_Various thoughts on wiki software_

## WikiJS

Used to run this site -- see [[WikiJS]].

## Outline
* https://www.getoutline.com/
* https://github.com/outline/outline
* https://twitter.com/outlinewiki

[Licensed as Business Source License](https://github.com/outline/outline/blob/master/LICENSE) -- which I had not heard of. Documenting under [[Licensing]]

My fork: https://github.com/bmann/outline, setup to easily deploy to Heroku (not updated to recent head, yet). The `app.json` did get merged, so you should use the main version.

The other issue I had, with having multiple Google accounts logging in to one team, [got solved with a small edit by someone else](https://github.com/outline/outline/issues/862#issuecomment-501333940).

# Resources

> I’d like to have a wiki that is private except for a group of (50-100) people I whitelist. Preferably free, or worst case, fixed fee that doesn’t scale with users.
>
> Howwww do I do this!? New pricing for GitHub and Notion don’t help here, unless I’m missing something.
> -- [Lee Edwards (@terronk), May 19th, 2020](https://twitter.com/terronk/status/1262883499708575744)

My response:

> I'm just in the midst of setting up @requarks for personal use. It syncs to a git repo, runs on Heroku for about $16/month ($7 paid dyno & $9 paid postgres DB)
>
>Even GitHub Free now appears to allow unlimited collaborators on a private repo.

---

## Wikis that use source-control for their backing store, Paul Hammant, Sept 2017

https://paulhammant.com/2017/09/23/wikis-that-use-source-control-for-their-backing-store/

Quoted from the article:

---

Maintained wiki implementations
- Gollum - Git backing store, Docker ready, maintained but has not had a lot of commits recently
- SahrisWiki - Mercurial backing store, Docker ready, maintained but has not had a lot of commits recently
- Zim Wiki - Bazaar, Git, Mercurial, or Fossil backing stores - personal desktop (fat client) rather than group web-app. v cool.
- Fossil’s Wiki - Fossil is a VCS itelf and has a built-in wiki.
- Realms - Git backing store. Python2. Actively maintained.
- DokuWiki - Git backing store. PHP. Actively maintained.
- Jingo - Git backing store. PHP. Actively maintained.

---

Has this to say about WikiJS:

> Can be linked to a Git repo and do round trip, but the database is the main DB, with sync to/from Git being done at intervals via single committer ID. That said, it is “Docker ready” using NodeJS and is actively maintained.

Which is not quite true. The DB is essentially a cache. The single committer is true.

My notes:

- [[Gollum]] -- not really setup for differential access without runing a whole SSO server
- [[Realms]] -- domain is dead, last code update 2018
- [[DokuWiki]] -- git backed plugin is 5 years last update https://github.com/woolfg/dokuwiki-plugin-gitbacked, still might be worth trying
- [[Jingo]] -- https://github.com/claudioc/jingo -- worth checking, although very basic auth