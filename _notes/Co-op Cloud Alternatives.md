---
---

[[Co-op Cloud]] has done a great job of listing out their opinions of the pros / cons of other server / app management software. 

Copy / pasted from their [FAQ](https://docs.coopcloud.tech/intro/faq/) so I can easily reference.
## [[Cloudron]]

### Pros

- 👍 Decent web interface for app, domain & user management.
- 👍 Large library of apps.
- 👍 Built-in SSO using LDAP, which is compatible with more apps and often has a better user interface than OAuth.
- 👍 Apps are actively maintained by the Cloudron team.
### Cons

- 👎 Moving away from open source. The core is now proprietary software.
- 👎 Libre tier has a single app limit.
- 👎 Based on Docker images, not stacks, so multi-process apps (e.g. parsoid visual editor for Mediawiki) are a non-starter.
- 👎 Difficult to extend apps.
- 👎 Only supported on Ubuntu LTS.
- 👎 Upstream libre software communities aren't involved in packaging.
- 👎 Limited to vertical scaling.
- 👎 Tension between needs of hosting provider and non-technical user.
- 👎 LDAP introduces security problems - one vulnerable app can expose a user's password for all apps.
- 👎 Bit of a black box

_**@boris commentary:** do I wish that Cloudron were fully open source? Yes. But I also like that the team has a sustainable business where they keep all of these apps packaged and updated over time! They mention the SSO model here as LDAP, but in fact it's OIDC now._

## [[Yunohost]]

### Pros

- 👍 Lovely web interface for app, domain & user management.
- 👍 Bigger library of apps.
- 👍 Awesome backup / deploy / restore continuous integration testing.
- 👍 Supports hosting apps in subdirectories as well as subdomains.
- 👍 Doesn't require a public-facing IP.
- 👍 Supports system-wide mutualisation of resources for apps (e.g. sharing databases by default)
### Cons

- 👎 Upstream libre software communities aren't involved in packaging.
- 👎 Uninstalling apps leaves growing cruft.
- 👎 Limited to vertical scaling.
- 👎 Not intended for use by hosting providers.

_**@boris commentary:** I took a look at Yunohost and found it scary from a security perspective. Packaging is a pile of bash scripts. More apps but they're mostly undermaintained_
##  [[Caprover]]

### Pros

- 👍 Bigger library of apps.
- 👍 Easy set-up using a DigitalOcean one-click app.
- 👍 Works without a domain name or a public IP, in non-HTTPS mode (good for homeservers).
- 👍 Deploy any app with a `docker-compose.yml` file as a "One Click App" via the web interface.
- 👍 Multi-node (multi-server) set-up works by default.
### Cons

- 👎 Single-file app definition format, difficult to tweak using entrypoint scripts.
- 👎 Nginx instead of Traefik for load-balancing.
- 👎 Command-line client requires NodeJS / `npm`.
- 👎 [Requires 512MB RAM for a single app](https://github.com/caprover/caprover/issues/28).
- 👎 [Backup/restore is "experimental"](https://caprover.com/docs/backup-and-restore.html), and doesn't currently help with backing up Docker volumes.
- 👎 Exposes its bespoke management interface to the internet via HTTPS by default.
## [[Ansible]]

### Pros

- 👍 Includes server creation and bootstrapping.
### Cons

- 👎 Upstream libre software communities aren't publishing Ansible roles.
- 👎 Lots of manual work involved in things like app isolation, backups, updates.
## [[Kubernetes]]

### Pros

- 👍 Helm charts are available for some key apps already.
- 👍 Scale all the things.
### Cons

- 👎 Too big -- requires 3rd party tools to run a single-node instance.
- 👎 Not suitable for a small to mid size hosting provider.

## [[Docker-compose]]

### Pros

- 👍 Quick to set up and familiar for many developers.
### Cons

- 👎 Manual work required for process monitoring.
- 👎 Secret storage not available yet.
- 👎 [Swarm is the new best practice](https://github.com/BretFisher/ama/issues/8#issuecomment-367575011).

I'll skip the the "doing it manually" old school version of server + app maintenance.