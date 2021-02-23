---
title: Jam
git: https://gitlab.com/jam-systems/jam
link: https://jam.systems
date: 2021-02-14
tags:
    - "drop in audio"
---

"Jam is an audio space for chatting, brainstorming, debating, jamming, micro-conferences and more."

Open source under the [[AGPL License]], mostly written in [[JavaScript]].

From the README:

> Jam is an Open Source alternative to Clubhouse, Twitter Spaces and similar audio spaces.
> With Jam you can create Jams which are audio rooms that can be used for panel discussions, jam sessions, free flowing conversations, debates, theatre plays, musicals and more. The only limit is your imagination.

It uses [[Docker]] and is made up of a [[React]] front end, [mafintosh/signalhub](https://github.com/mafintosh/signalhub) for managing [[WebRTC]] connections, and a [[NodeJS]] server `pantry` "lightweight server for handling authentication and coordination of Jam"