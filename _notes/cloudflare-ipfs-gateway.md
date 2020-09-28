---
title: Cloudflare IPFS Gateway
---

[[Cloudflare]] has a [Distributed Web Gateway](https://www.cloudflare.com/distributed-web-gateway/) page that covers both [[IPFS]] and [[Ethereum]].

Here is the extreme TLDR of using their IPFS gateway (if you already have your DNS hosted with Cloudflare):

1. Create a CNAME for your website that points to `cloudflare-ipfs.com` -- in my case for my root domain, `bmannconsulting.com`
2. Create a TXT record at `_dnslink.bmannconsulting.com`
3. Enter in `dnslink=/ipns/APPNAME.fission.app` -- from the [[Fission]] [Guide on controlling your own DNS](https://guide.fission.codes/hosting/custom-domains/control-own-dns)

Unfortunately, Cloudflare automatically has 6 hours of caching set, and no way to automatically purge / refresh cache when using [[IPNS]] in your [[DNSLink]]. [Request on the Cloudflare community forum here for cache clear](https://community.cloudflare.com/t/cloudflare-ipfs-gateway-cache-clear/35488).

For now, setting the DNSLink to use a hash and updating it with [[ipfs deploy]] would be one way to make this work.