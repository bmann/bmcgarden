---
---

alias:: LogSeq Conversion

- The conversion of [[BMC/Garden]] to #LogSeq
- DONE Figure out how to include the ~~blog and~~ [[BMC/Archive]] for searching and linking
  collapsed:: true
	- Technically included in the graph now
	- Trying out `archive:: true` and changing `created` from a Unix time stamp to a LogSeq compatible and human readable `Jun 1st, 2003`
	- I might use the #published property instead of created since that’s what I already use for external articles
	- Maybe I’ll just slowly convert? I think so!
	- Pages remain in the same folder, but with a filename the same as the page name
	- #completed [[Dec 27th, 2022]]
- DONE Move posts out of _posts structure
  collapsed:: true
	- Keep an archive folder and a blog folder
	- #completed [[Dec 30th, 2022]]
		- Made the move on desktop
- Convert more recent blog posts
	- Needs a plan for footnotes, currently uses [[Littlefoot]] which I quite like
	- LogSeq supports Markdown footnotes already, so let’s just make a backlog item
	- It is easiest to do quickly directly in [[Working Copy]] — keeping them as non outliner Markdown is fine
	- CANCELLED Support [[Littlefoot]] for footnotes in published LogSeq [[BMC/Backlog]]
	  id:: 63af89eb-3371-42cb-a4d9-677b0293913e
		- [[Dec 30th, 2022]]
			- Tried to do some installs but it doesn’t look like it’s going to work
- DONE Flow for new blog posts
	- Use #published to give them a date
	- ~~Tag them with #blog~~
	- Use property [[BMC/Blog]]
	- Turn off outline bullets / special styling?
- DONE What goes on the home page, how to theme a custom home page for LogSeq
- DONE Troubleshoot Fission publishing
	- #completed [[Dec 31st, 2022]] Works fine with the `fission.yaml`
- DONE Switch back to main bmannconsulting domain / main branch of repo
	- #completed [[Dec 31st, 2022]] Set the `logseqconversion` branch as default