---
title: InterPlanetary File System (IPFS)
---

IPFS is the InterPlanetary File System.

As mentioned in the [[Colophon]], this site is published to IPFS using the [[Fission]] Github Action. The action builds the static representation from the Markdown source using [[Jekyll]], calculates a top level [[CID]] hash aka Content IDentitifier, updates the [[DNSLink]] for the bmannconsulting.com domain, and has the Fission server cache a copy.

You can see that the DNSLink for the domain using this DNS checker <https://dnsrecords.io/_dnslink.bmannconsulting.com>, which in turn is just an alias to a Fission app, which has the actual hash <https://dnsrecords.io/_dnslink.bmcgarden.fission.app>.[^dnsrecords] You can take the CID that you find there, of the form `bafybeicxxtumkkha75i26livxe5a3iqklqfo42d7qytk2f4ob37bs3jpqa` and plug that in anywhere that understands IPFS and get the contents of that cyberboats page.

[^dnsrecords]: DNS Records is a great service! An online DNS checker / explorer. It also does social previews in things like Slack or Discord chat, so a great way to just type in a link and get the results in the preview <https://dnsrecords.io/>

You can peek at the IPFS file system underneath, by linking to one of the annual blog folders, like 2020 blog posts <https://bmannconsulting.com/blog/2020/>. Since we're browsing in there, we can also get the CID for the <a href="{{ "/blog/2020/01/03/cyberboats/" | relative_link }}">cyberboats</a> blog post, and plug it into any other gateway, like the [[Web3Storage]] one: <https://bafybeicz677flygp3v6zei4xkt3pcp6npuwk5dp2awqq3hxnxhgukhrpky.ipfs.dweb.link/> [^unstyled]

[^unstyled]: Yeah, this is unstyled, because it's trying to fetch a CSS file that is no longer referenced correctly. I could hardcode it to use the full path, but then it will point to a different version of the stylesheet. To figure out!

InterPlanetary Naming Service (IPNS) can use a name that points to IPFS hashes. This website you're browsing now is already being served over Fission's IPFS Gateway. If you're running [[Brave]], it can cache and browse sites, so you'd actually be able to browse it through localhost.

Since we already looked at Web3Storage, let's browse via IPNS using their gateway. You'll see <a href="https://w3s.link/ipns/bmannconsulting.com" target="_ipfs">w3s.link/ipns/bmannconsulting.com</a> redirect to <a href="https://bmannconsulting-com.ipns.dweb.link/" target="_ipfs">bmannconsulting-com.ipns.dweb.link</a>