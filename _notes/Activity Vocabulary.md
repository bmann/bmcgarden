---
link: https://www.w3.org/TR/activitystreams-vocabulary/
published: 2017-05-17
tags:
  - W3C
  - specification
---
## Object Types

The [Object]([[Activity Vocabulary/Object]]) Types include:
- [[Activity Vocabulary/Article]]
- [Audio](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-audio)
- [Document](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-document)
- [Event](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-event)
- [Image](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-image)
- [[Activity Vocabulary/Note]]
- [Page](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-page)
- [Place](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-place)
- [Profile](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-profile)
- [Relationship](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-relationship)
- [Tombstone](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-tombstone)
- [Video](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-video)

## Object

Describes an object of any kind. The Object type serves as the base type for most of the other kinds of objects defined in the Activity Vocabulary. [¶](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-object)

### Properties
[attachment](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-attachment) | [attributedTo](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-attributedto) | [audience](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-audience) | [content](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-content) | [context](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-context) | [name](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-name) |[endTime](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-endtime) | [generator](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-generator) | [icon](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-icon) | [image](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-image) | [inReplyTo](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-inreplyto) | [location](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-location) | [preview](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-preview) |[published](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-published) | [replies](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-replies) | [startTime](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-starttime) | [summary](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-summary) | [tag](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-tag) | [updated](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-updated) | [url](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-url) | [to](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-to) | [bto](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-bto)| [cc](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-cc) | [bcc](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-bcc) | [mediaType](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-mediatype) | [duration](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-duration)

## Article

Represents any kind of multi-paragraph written work. [¶](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-article)

Inherits all the properties from Object
## Note

Represents a short written work typically less than a single paragraph in length. [¶](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-note)

This is the main type used by [[microblogging]] apps like [[Mastodon]]