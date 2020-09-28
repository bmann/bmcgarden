---
title: wget
---

## Download an entire website with wget

Source: [Linux Journal](https://www.linuxjournal.com/content/downloading-entire-web-site-wget)

```
wget \
     --recursive \
     --no-clobber \
     --page-requisites \
     --html-extension \
     --convert-links \
     --restrict-file-names=windows \
     --domains example1.com example2.com \
     --no-parent \
         example1.com
```

You may also want to add `--limit-rate=10k` (or some similarly slow speed) so that you don't trigger the site blocking you.

Checking this into a git repo and putting it on [GitHub Pages](https://pages.github.com/) is a good way of archiving sites.