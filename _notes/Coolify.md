---
tags:
  - selfhosting
  - PaaS
link: https://coolify.io
github: https://github.com/coollabsio/coolify
---
Website: <https://coolify.io>

> An open-source & self-hostable Heroku / Netlify / Vercel alternative.

More PaaS-like, git push to deploy.

Backups to any S3-compatible storage.

Paid cloud version, pricing starts at $5/month https://app.coolify.io/

From github README:

> The recommended way to use Coolify is to have one server for Coolify and one (or more) for the resources you are deploying. A server is around 4-5$/month.
> 
> By subscribing to the cloud version, you get the Coolify server for the same price, but with:
> 
> - High-availability
> - Free email notifications
> - Better support
> - Less maintenance for you

Note: the [pricing](https://coolify.io/pricing) is gated on managing a number of other servers to deploy to: you have to “bring your own server”.

## Build Packs Supported

> Coolify uses [[Nixpacks]] as build pack by default. Nixpacks detect what kind of application are you trying to deploy and builds it accordingly.

- Nixpacks
- Dockerfile
- Docker Image

## Apps

<https://coolify.io/docs/one-click-services>


See also: [[CapRover]]