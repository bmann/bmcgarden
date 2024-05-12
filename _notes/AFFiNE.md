---
link: https://affine.pro
tags:
  - opensource
  - app
  - localfirst
github: https://github.com/toeverything/AFFiNE
---
AFFiNE is a workspace with fully merged docs, whiteboards and databases. Built local first with cloud sync using CRDT for multi-device and multi-user. 

Open source and self host-able - Postgres and Redis in Docker. 

Described as a Notion or Miro replacement. 
## Licensing

Similar to Cal.com, MIT-licensed with a backend portion [AFFiNE Enterprise Edition License](https://github.com/toeverything/AFFiNE/blob/canary/packages/backend/server/LICENSE) that will restrict / charge for organization and team features. 
## Other Open Source

The Affine team have extracted several frameworks out of their core application stack. 
### Blocksuite

[BlockSuite](https://blocksuite.io/) is a toolkit for building editors and collaborative applications.

Based on [[Web Components]] (which is notable because Affine is built in React).

[toeverything/BlockSuite](https://github.com/toeverything/blocksuite)

### OctoBase

[OctoBase](https://octobase.dev/) an offline-available, scalable, self-contained collaborative database implemented based on CRDTs. It is the core to resolve conflicts between the duplication of data and manage the databases so that real-time collaboration and local-first storage is possible. It supports local storage and serve-side storage.

A light-weight, scalable, data engine written in Rust.

Additionally, OctoBase can function as a standalone server database, or it can be integrated directly into your application as an embedded database while remaining fully functional.

AGPL licensed 

[toeverything/OctoBase](https://github.com/toeverything/octobase)

## Self Hosting

The [Affine Self Host docs](https://docs.affine.pro/docs/self-host-affine) talks about steps to take to run Docker / Docker Compose.

### Portainer Setup

I have a demo running on my test install of [[Portainer]].

I used the [compose file on Github](https://github.com/toeverything/AFFiNE/blob/canary/.github/deployment/self-host/compose.yaml) and added `version: '0.1'` to the top and pasted that into Portainer's "stacks" interface.

I used the interface to add env variables for admin email and password.

Once the stack was deployed, I went to `$MYIP:3010` and created a new cloud workspace.

It is currently very unclear what the costs will be for self-hosted. There is a [Github issue with many items marked offtopic](https://github.com/toeverything/AFFiNE/issues/6156) -- which also includes details on what to edit in the database to remove restrictions. Github Discussions has a couple of topics on self hosting -- [5975](https://github.com/toeverything/AFFiNE/discussions/5975), [6299](https://github.com/toeverything/AFFiNE/discussions/6299).

[[Outline]] has a no-charge community edition with limited features, as does [[Cal.com]].