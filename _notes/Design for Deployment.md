---
---

Designing software while very much thinking about how it will be deployed and operated.

Design is trade-offs, so one one end one has software optimized for smaller, individual users, vs cloud operators and devops.

Designing for deployment by operators will look at things like automation and provisioning and testing in cloud environments.

Designing for less technical end users who want to run the software day-to-day either personally or for small groups should look more like one-click deploys and auto-updates, and might even be designed to fit within the resource limits of freemium PaaS services.

A great example is [[Discourse]]. The team runs a paid hosting service, but it also has a really great dockerized install and update system. There are complexities, but a somewhat technical user can follow instructions and setup and install the system, and most importantly, has an automatic update system built in.

[[Cloudron]] is another great example. Any of the apps they package, are automatically updated over time. Some of them have [[OIDC]] single sign on built in, which enables deeper integration into Cloudron and more simplicity in user management. I don't see a lot of apps specifically targeting Cloudron today -- that is, they aren't designing for this type of deployment -- but a lot of open source software probably should.