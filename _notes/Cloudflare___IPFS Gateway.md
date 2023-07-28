---
---

tags:: #[[IPFS/Gateway]], #saas

- This is slightly stale content. Cloudflare now has this as part of Web3 services, and this gateway service is either free for the Basic package, or $5/month for a paid version
- [[Cloudflare]] has a [Distributed Web Gateway](https://www.cloudflare.com/distributed-web-gateway/) page that covers both [[IPFS]] and [[Ethereum]].
- Here is the extreme TLDR of using their IPFS gateway (if you already have your DNS hosted with Cloudflare):
  
  1. Create a CNAME for your website that points to `cloudflare-ipfs.com` -- in my case for my root domain, `bmannconsulting.com`
  2. Create a TXT record at `_dnslink.bmannconsulting.com`
  3. Enter in `dnslink=/ipns/APPNAME.fission.app` -- from the [[Fission]] [Guide on controlling your own DNS](https://guide.fission.codes/hosting/custom-domains/control-own-dns)
- Unfortunately, Cloudflare automatically has 6 hours of caching set, and no way to automatically purge / refresh cache when using [[IPNS]] in your [[IPFS/DNSLink]]. [Request on the Cloudflare community forum here for cache clear](https://community.cloudflare.com/t/cloudflare-ipfs-gateway-cache-clear/35488).
- For now, setting the #IPFS/DNSLink to use a hash and updating it with [[ipfs deploy]] would be one way to make this work.