---
tags:
  - opensource
  - licensing
---

> The [[wikilinks]] on this page go to my main Digital Garden notes, linking to further related notes and articles.

Licensing, and "open source" licensing in particular, is something I've spent a lot of time on.

I am not a lawyer, but had to self-educate in the early 2000s as part of participating in the rise of open source, especially within the [[Drupal]] and broader PHP-based software community.

Starting around 2018, I began to look at emerging licenses and changes in open source licenses. I have learned a huge amount from [[Kyle Mitchell]]. I highly recommend subscribing to his blog <a href="https://writing.kemitchell.com" title="Kyle Mitchell's Blog /dev/lawyer - law, technology, and the space between">writing.kemitchell.com</a>.

My premise is that we are seeing an evolution beyond the [[OSI]] approved licenses, which they like to call the true open source definition [[OSD]]. The driver for this is that many for-profit companies are taking from openly licensed projects but not giving back. In particular, the [[hypercloud]] providers creating hosted versions and making a lot of revenue, and not even contributing to maintenance of the core software that is being used, never mind any fairness around revenue sharing.

## Licenses

I'm often asked what license should a project pick. The easy answer from me is MIT or Apache, both permissive licenses. But licensing is not a business model. Can choice of license be used to block certain users, or require them to contribute? Yes!

Included in this evolution is a whole class of ethical licenses (some terms around restricting what types of users or use cases the software can be used for) and non-commercial or fair licenses (some conditions that users of the code need to contribute back). None of these are OSI-approved to date. With open source now used by commercial companies around the globe, and getting open source maintainers paid still being an unsolved problem, many are turning to these classes of licenses. While at the same time being yelled at by people who say "it's not really open source unless it's OSI approved, don't call it that".

Pick [[Parity]] if you want all users to contribute back changes. Pick [[Prosperity]] if you want commercial users to pay for a license.

The [[Big Time License]] is a less restrictive version of Prosperity: for small business and non-commercial users of all kinds, it functions as classic open source software for free, no-charge usage and contribution. For larger companies, a license needs to be paid for. Or, granted in exchange for active maintenance contributions!

### Parity License

<https://paritylicense.com/> [[Parity]]

Open, share-alike (or rather, "parity") license aka copyleft, where software may not be used closed source. [[GPL]] or [[AGPL]] held by a single company often is used this way as well -- where they can selectively sell a proprietary license so that companies can pay if they don't want to share source code.

### Prosperity License

<https://prosperitylicense.com/> [[Prosperity]]

Non-commercial license, where the software may be used for any purpose except for-profit. For profit companies need to buy a license.

### [[Big Time License]]

<https://bigtimelicense.com> 

> A public license that makes software free for noncommercial and small-business use, with a guarantee that fair, reasonable, and nondiscriminatory paid-license terms will be available for everyone else

> Purpose: These terms let you use and share this software for noncommercial purposes and in small business for free, while also guaranteeing that paid licenses for big businesses will be available on fair, reasonable, and nondiscriminatory terms.

A non-commercial license that carves out a further, explicit exception for small businesses to use the software at no charge. So only "Big Time" users need to get a license.

### Business Source License

<https://mariadb.com/bsl11/> [[BSL]]

Created by MariaDB, and the license text is copyrighted by them, and "Business Source License" is a trademark of MariaDB.

> The Business Source License (this document, or the “License”) is not an Open Source license. However, the Licensed Work will eventually be made available under an Open Source License, as stated in this License.

I have extensive links at [[BSL]], including the version that [[Hashicorp]] uses. Hashicorp has chosen a 4 year term after which the code becomes [[MPL]] licensed.

### Cryptographic Autonomy License

<https://opensource.org/license/cal-1-0/> [[CAL]]

> Purpose: This License gives You unlimited permission to use and modify the software to which it applies (the “Work”), either as-is or in modified form, for Your private purposes, while protecting the owners and contributors to the software from liability.

> This License also strives to protect the freedom and autonomy of third parties who receive the Work from you. If any non-affiliated third party receives any part, aspect, or element of the Work from You, this License requires that You provide that third party all the permissions and materials needed to independently use and modify the Work without that third party having a loss of data or capability due to your actions.

CAL is pretty unique because it's a permissive license with a catch, that goes beyond the [[AGPL]], where the users of the software are required to be given everything that is needed to "use and modify" the software. Basically, anything you need to host the software has to be supplied. This restriction, of maintaining user autonomy, did pass the [[OSI]] approval process in February 2019.

### Cross License Collaboratives

<https://xlcollaborative.com/> [[XLC]]

> Maintain your projects’ licenses and create shared moneymaking opportunity without any company, foundation, or dictator.

Labeled as [[XLC]] for short, Kyle Mitchell has [written a couple of posts about XLC back in 2019](https://writing.kemitchell.com/series/cross-license-collaboratives).

I'm going to quote the [landing page for the XLC in full](https://xlcollaborative.com/):

> Cross license collaboratives are co-op-like networks of contributors to online projects that can…
>
> * change the license terms for their projects democratically, without getting permission from every contributor
> * gift or sell commercial licenses and other licenses, sharing proceeds equally
> * welcome new contributors from all over the world
> …all without the overhead of a company, foundation, or other legal organization.
>
> Contributors can start a collaborative for their project by adopting a new kind of plain-language contributor license agreement. You can read the latest version online or browse other formats and versions.
>
> Unlike other contributor license agreements, the cross license collaborative agreement is _decentralized_ and _peer-to-peer_. No single contributor or organization gets any special licensing powers. Rather, every contributor licenses _every other contributor_, subject to rules about how new licensing decisions will be made.

There is also an [XLC introduction with some illustrations](https://xlcollaborative.com/introduction). From that page is this useful paragraph about how you can combine XLC with one of the previous licenses, to share licensing revenue:

> Cross license collaborative governance rules also require sharing of any proceeds related to licensing. If the collaborative makes its project available under a share-alike or noncommercial licensing, and then chooses to sell an exception for closed or commercial use, they must share the license fee with all contributors.

What is not specified in this license is quite how to recognize new contributors, how to share value. aka all the hard stuff. But I _love_ this conceptually. It's "co-op like" without the overhead of creating a formal co-op organization rooted in some particular jurisdiction. "An open source peer co-op" might be a good short form, where "collaborative" is probably the right word so it doesn't trick people into thinking it is a co-op.

## Conclusions

Ideologically, I prefer permissive licenses. But, seemingly, we need to go to non-commercial licenses like [[Big Time License]] in order to preserve the ability to charge licenses to large corporations.

I have some other thoughts about [[Permissive Licenses and Fenced Community]].
## Blog Posts & Presentations

A variety of blog posts & presentations on the concepts around open source and evolving licenses:

* June 2024, Presentation: [[Open Source Beyond Licensing - The Evolution Ahead]]
* August 2020, Blog [Public vs Common Goods in Open Source](https://blog.bmannconsulting.com/2020/08/11/public-vs-common.html)
* July 2020, Presentation: [Open Source: Licensing, Business Models, Community](https://talk.fission.codes/t/open-source-licensing-community-and-business-models-outlier-ventures-basecamp/786)
* October 2019, Presentation: [Open Source Licensing Evolution](https://noti.st/bmann/aOkl8w/open-source-licensing-evolution)
* April 2019, Presentation: [Open Source Licenses, Peer Production & Non Code Contributions](https://noti.st/bmann/BJ0zvs/open-source-licenses-peer-production-non-code-contributions)
