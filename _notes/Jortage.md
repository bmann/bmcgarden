---
link: https://jortage.com
tags:
  - Fediverse
  - storage
  - Mastodon
  - S3
---
The Jortage Storage Pool is an S3-compatible frontend to Backblaze + Fastly that performs file-level deduplication, designed for fediverse instances.

> Jortage is a communal project providing object storage and hosting. Our model is to pool together hosting expenses of our members to allow pay-what-you-can usage and to reduce everyone's costs overall.

Supported by [[Fastly]]’s Fast Forward program. 

> When media is uploaded to Jortage, it is received by our "ingest server", running the open-source [Jortage Storage Pool Manager](https://github.com/jortage/poolmgr), or poolmgr for short. Poolmgr hashes media being uploaded to it on-the-fly with SHA-512, while simultaneously streaming it to a temporary file. Once the entire file has been uploaded, poolmgr checks if this SHA-512 hash has been uploaded before. If so, the data is discarded. If not, it is uploaded to our backing store (Backblaze, currently). In both cases, the hash is then associated with the requested path in the database in the "name map".