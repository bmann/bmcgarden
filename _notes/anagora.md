---
title: Anagora
link: https://anagora.org/
date: 2020-11-24
modified: 2021-01-24
---

An [[Agora]] implementation by @Flancian.

The concept is to have nodes / notes where people maintain their own digital notes garden like I do here, but then pull them in and link them through their public git repos. Aka a "distributed knowledge graph".

The [Agora Plan](https://anagora.org/node/agora-plan) page has more details, including a link to the [[Agora Server::https://github.com/flancian/agora-server]]. It is written in [[Python]] / Flask and is open source under the [[Apache2 License]].

---

This site is [[Connecting to the Agora]] as of January 24th, 2021

---

## Features and Documentation

<https://anagora.org/@bmann> is my profile page. If you start browsing there, all the links default to my notes only.

<https://anagora.org/node/agora-actions> lists the actions you can use.

<https:/anagora.org/node/agora-search> describes how to use the agora as a search engine.

## Conventions

Notes on suggested conventions
### Accepting the Contract

Link to the contract with a date indicating you accepted it.

## Feature Requests

Ideas about the agora social system as a whole, but for now mostly technical features of the Anagora server software.

### Include / Ignore Content

Can I indicate that some portion of the git repo should be included or ignored?

I would like to ignore my archive and journal posts, or at least only selectively include them. 

Suggestion: include a file, `.agora` or `.agora-config` or similar that is YAML or similar.

```yaml
exclude:
    - _posts/journal/*
    - _posts/archive/*
include:
    - _posts/journal/2021-01-24-journal.md
```