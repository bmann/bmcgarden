---
---

github:: https://github.com/piku/piku
author:: [[Rui Carmo]] 
tags:: #opensource, #PaaS, #Python
link:: https://piku.github.io

- The tiniest Heroku/CloudFoundry-like PaaS you've ever seen. **Seldom updated because it is *stable*** and used in production daily by several people.
- `piku`, inspired by [dokku](https://github.com/dokku/dokku), allows you do `git push` deployments to your own servers.
- Core Values
	- Runs on low end devices.
	- Accessible to hobbyists and K-12 schools.
	- ~1000 lines readable code.
	- Functional code style.
	- Few (single?) dependencies
	- [[12 Factor App]]
	- Simplify user experience.
	- Cover 80% of common use cases.
	- Sensible defaults.
	- Leverage distro packages in Raspbian/Debian/Ubuntu (Alpine and RHEL support is WIP)
	- Leverage standard tooling (`git`, `ssh`, `uwsgi`, `nginx`).
	- Preserve backwards compatibility where possible