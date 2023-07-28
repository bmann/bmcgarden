---
---

tags:: #LogSeq, #[[Github/Pages]], #[[Github/Actions]], #howto

- Check your #LogSeq folder into a Git repo
- Use the [[logseq-publish]] action by Pengx17 in a GitHub Action
	- Example in the #BMC/Garden repo that publishes this site https://github.com/bmann/bmcgarden/blob/logseqconversion/.github/workflows/logseq.yml
- Turn on GH Pages publishing for the repo
- Flip the “all pages public when publishing” in Settings > Editor OR set `public:: true` on individual pages
	- You can set public to false to selectively have private pages
- Whenever you git commit, the action will trigger and build and publish your site to GH Pages
- You can also [[Publish LogSeq from Mobile]]
	- Technically this is also being synced via iCloud and accessible on your desktop for you to view and edit using the LogSeq app there