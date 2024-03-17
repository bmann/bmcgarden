---
link: https://webrecorder.net
tags:
  - app
  - protocol
  - backup
  - IPFS
---
## About

> the goal of Webrecorder has been to build quality open source tools enable 'web archiving for all' to allow anyone with a browser to create their own web archives, and to accurately replay them at a later time.
> [About](https://webrecorder.net/about)

### Quality Open Source Web Archiving Tools

### Making web archiving more accessible via decentralized technologies

> Rather than supporting a single centralized silo, a key goal remains to support web archives in a variety of environment and storage scenarios. From users' personal laptops, to google drive, to IPFS, Webrecorder tools will be designed to support creating and accessing web archives wherever they may be found.

[ReplayWeb.page](https///replayweb.page) as one example
> Serverless replay of web archives directly in the browser
* GitHub [webrecorder/replayweb.page](https://github.com/webrecorder/replayweb.page)
### Intersection of web archiving and software emulation

## Protocols

### WACZ

> WACZ stands for _W_eb _A_rchive _C_ollection _Z_ipped, and is a new file format designed to make creating and hosting web archives quicker and easier.

[specs](https://github.com/webrecorder/specs)

### IPFS Custom File Chunking for WARC and WACZ

> This specification presents a specialized content-aware chunking strategy for adding composite web archive files (WARC and WACZ) to IPFS that maximizes content-based deduplication and is optimized for range-based access while producing a standard IPFS (UnixFS) file object.

[spec](https://github.com/webrecorder/specs/blob/main/wacz-ipfs/latest/index.md) for [[IPFS]] integration.

Talked to Ilya about using [[WNFS]] rather than UnixFS since it is more of a file system (including versions), and could support private files through encryption.
