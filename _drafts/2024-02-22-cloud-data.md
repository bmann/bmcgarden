---
tags:
  - personaldatastores
title: Cloud data
date: 2024-02-22T15:17:00
categories:
  - Own Your Own Data
---
[[Rosano]] has an [encryption rant](https://utopia.rosano.ca/encryption-rant/) about attempting to back up data from a number of secure chat apps, and how it's all basically impossible for people without strong technical skills:

> …there's no feigning moral superiority in using 'alternative tech' until it includes a real foundation to stand on for people without this domain expertise. Fleeting personal data is like alternative tech's equivalent of platform enshitification and doesn't fill me with confidence to trust these systems or recommend my non-tech friends to do so.

And what he actually wants more generally:

> I hope to see more apps with comprehensive export or supporting personal data stores.

I agree with his message that perhaps one could design tech for export/backup, much like I've been talking about [[Design for Deployment]].

The [[Personal Data Store]] is the generic term for what Rosano and I have been wanting for a long time: a user owned file system, where different apps get given permission to read and write into. That's the actual design I'd love to get to.

If this sounds confusing to you, you'll recognize it from how mobile apps work today. A new app will ask permission to access your Photos or Contacts, or some other standardized form of data. Rather than keeping a separate copy of data in some other backend server somewhere, the app is given permission to share.

If you uninstall the app, you still have your Photos and Contacts, and can hand permission to any other app.

And of course on a Professional Desktop Operating System[^death]

[^death]: See [[death of the professional desktop operating system]]

It's clear that to Rosano, his chat history is very important.