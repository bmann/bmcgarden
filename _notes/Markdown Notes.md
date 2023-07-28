---
title: Markdown Notes
---

Markdown Notes is one of the [[Foam]] [recommended extensions](https://foambubble.github.io/foam/recommended-extensions) for [[VSCode]].

For reference, my settings. These are kept in `.vscode/settings.json`.

```
  "vscodeMarkdownNotes.newNoteDirectory": "_notes",
  "vscodeMarkdownNotes.newNoteTemplate": "---\ntitle: ${noteName}\n---\n"
```

Which results in front matter being created that looks like:

```
---
title: Full Note Name
---
```