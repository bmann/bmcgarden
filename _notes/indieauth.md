---
title: IndieAuth
link: https://indieauth.net/
tags:
    - identity
    - OAuth
    - IndieWeb
---

IndieAuth is an [[IndieWeb]] component that lets you sign in to things using your own website. The main instance is at <https://indieauth.com>, and the spec is at <https://indieauth.net/>. Created and maintained by @aaronpk

From the spec:

> IndieAuth is a decentralized identity protocol built on top of [[OAuth]] 2.0.
>
> This allows individual websites like someone's [[WordPress]], [[Mastodon]], or [[Gitea]] server to become its own identity provider, and can be used to sign in to other instances. Both users and applications are identified by URLs, avoiding the need for getting API keys or making new accounts.

From the .com:

> IndieAuth.com provides an IndieAuth server for your website that authenticates you using your existing social accounts. First you link from your website to one or more authentication providers such as GitHub or a PGP key, then when you enter your domain name in the web sign-in form on websites that support IndieAuth, you can sign in without using a password.

I currently use my Github account to login. More third-party services used to work (like Twitter), but don't anymore. I've been meaning to explore the private key support, but really, it's very specifically [PGP support](https://indieauth.com/pgp).
