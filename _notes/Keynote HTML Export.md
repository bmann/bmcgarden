---
tags:
  - Apple
  - Keynote
---
I recently used the Apple Keynote HTML export and it works pretty great! I haven't found a lot of information about this that isn't stale, so capturing a few notes.

See [[Open Source Beyond Licensing - The Evolution Ahead]] for an embedded iframe version, and here is the [direct link to the html export](/assets/2024/06/26/open-source-beyond-licensing/).

The export is about 20MB, and is an `index.html` file and an assets folder, which has a folder for each slide. If you poke around, you can see that there's a PDF for each slide as well as some JSON, a thumbnail, and a few other things.

Here's a link to the [assets folder uploaded to IPFS](https://ipfs.runfission.com/ipfs/bafybeibikizcshxug634ssg4aobxrhcwkbyll2mlj6vt3fc4nhhatotr4u/) so you can have a look.

Keynote has had this feature for a long time, and apparently people complain about the quality or semantics about the HTML. I'm just delighted it "just works".

## Resources

[Keynote Extractor](https://keynote-extractor.com/) extracts really clean HTML, including slide notes. It exports straight images doesn't really do transitions or interactive presentations.