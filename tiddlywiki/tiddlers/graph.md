---
title: Graph
---

The default [[Digital Garden Jekyll Template]] has a "notes graph" embedded on every page.

Since I'm doing things a little differently, and also including my [[Archive]], I had to modify the [[Backlinks]] plugin `bidirectional_links_generator.rb` to include posts as well.

It throws an error on generation now:

```
warning: regular expression has redundant nested repeat operator '*'
```

And while Jekyll is in watch mode, it keeps editing the `notes_graph.json` file continuously.