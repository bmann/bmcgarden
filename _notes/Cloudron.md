---
---
[Cloudron](https://www.cloudron.io/?refcode=b90d0ee382ac47ba) is a complete solution for running apps on your own server.

It fits into a category of [[selfhosting]] -- you provide the server either at home or in the cloud, and  Cloudron helps you manage the entire server including installing and updating apps, managing DNS, running email, backups, operating system updates, user accounts, and so on.

The [about page](https://www.cloudron.io/about.html) also uses the term [[private cloud]].

It's designed to run on Ubuntu LTS versions. 

I run [[Commons Computer]] as my personal Cloudron instance.
## License
The Cloudron code itself is source-available, with a [subscription license](https://www.cloudron.io/legal/license.html) required if you want to self host more than 2 apps and have full access to all features like email.

The team creates, contributes to, and directly supports a [number of open source packages](https://www.cloudron.io/opensource.html). All of the app packages that are deployed on Cloudron are open source.

A number of app packages they support installing (e.g. Atlassian Confluence, Outline, Cal.com) have various non-commercial / subscription required licenses as well.
## Cost

* Cloudron license: $15/month, paid annually
* Backup: $5USD/month
* Hosting: $11USD/month

Total: $31USD per month, $372USD per year.

For many services like email ($5-$10/user/month), file sharing ($5-$10/user/month), calendaring ($5-$10/user/month), you can quickly see that ~5 users.

That does assume someone willing to do basic Cloudron admin. You don't need to use the command line, but you do need to be familiar with DNS, email, and other services with API keys and relatively technical settings.
### Backup

[[Digital Ocean]] has [Spaces storage starting at $5](https://www.digitalocean.com/products/spaces) for up to 250GB. [Cloudron lists all of the storage providers they support](https://docs.cloudron.io/backups/).
### Hosting
#### OVH Bare Metal Servers
For [[CoSocial]], I wanted to keep hosting in Canada. OVH has a data center in Quebec and low cost bare metal servers.

Example OVH for $29.99CAD/month
* Intel Xeon E3-1245v2 - 4 c / 8 t - 3.4 GHz / 3.8 GHz
* Memory: 32 GB DDR3
* Storage: 2 x 480 GB SSD SATA Soft RAID

A bare metal server will be able to host many more apps than a VPS, but it's also a single point of failure: if something goes wrong with the hardware of that server, that's your problem.

#### Hostinger VPS

![[hostinger-vps-plans-screenshot.png]]

For the difference in price, I'd recommend at least the KVM 4 with 16GB RAM. Those are USD prices. You can use my referral code for one-click Cloudron installs on a [Hostinger VPS](https://hostinger.com?REFERRALCODE=1BORIS58)
#### Home Hosting
I'd love to try running a Cloudron install at home, but it all seems quite a bit trickier. You're still looking at a ~$500 mini server purchase, which is like 2 - 3 years of VPS hosting costs!

### DNS and Domains

You'll need at least one domain name and more likely will have at least 2, so add another $10 - $30 per year in domain registration fees.

Cloudron will automatically [manage all your DNS settings for you](https://docs.cloudron.io/domains/) if you add them using a registrar that supports API access.
### Email

For production services of things like mailing lists, you may have trouble with deliverability of self-hosted email. You can [setup SMTP relay](https://docs.cloudron.io/email/#relay-outbound-mails) from a number of different providers. Any provider that provides SMTP services will work.

There are some apps (like Ghost) that [require Mailgun](https://docs.cloudron.io/apps/ghost/#bulk-emails) for their subscription services.

Example starter pricing: Postmark $15USD/month, Mailgun is free for up to 10,000 emails and the first paid plan is $35USD/month for up to 50K emails.

## Apps
The [Cloudron store lists all the apps they support](https://www.cloudron.io/store/index.html). It uses [[Docker]] images to package apps, but then runs centrally managed services like database, redis, files, email, etc.

## Things to use Cloudron for

Discourse

Mastodon

Nextcloud

Email

