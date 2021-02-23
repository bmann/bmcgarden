---
date: 2021-02-20T22:28:45.084-08:00
tags:
    - IndieKit
    - iA Writer
    - Quill
modified: 2021-02-22
---
Well, everything is working, but need to figure a few things out. I used [[iA Writer]] to post to the site and it works! I've made Article post types into what I call Notes here, the main post type.

Posting from [[Quill]] as an Article isn't going to work[^article], since it turns everything into HTML and escapes the square brackets in [[wikilinks]].

[^article]: That is, the Micropub Article type, which is meant to be long form and HTML.

For the (Micropub) Notes post type, I've created a new kind called [[Logs]]. They use the current date stamp as their filename, ~~and I made a temporary logs page to display them~~.

So, I can post arbitarily long Notes posts with Markdown formatting and wikilinks. This could replace my manual Journal entries. Instead, I would auto-generate journal pages per day (not sure if this is possible), or maybe just show the last N days of logs on a main journal page.[^logstojournal]

[^logstojournal]: As of 2021-02-22, I'm calling this log type a journal, and in fact merging the journal posts I made before into the logs category.