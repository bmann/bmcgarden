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
- 👎 Bit of a [black box](https://en.wikipedia.org/wiki/Black_box).

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