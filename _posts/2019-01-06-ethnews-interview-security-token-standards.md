---
layout: post
categories:
  - Interview
tags:
  - ETHNews
  - security tokens
  - Ethereum
  - ERC1400
comments: true
title: "ETHNews Email Interview about Security Token Standards"
excerpt: "Trent Rhode from ETHNews sent me some questions around security token standards, so I wrote up a bunch of background."
---
_[Trent Rhode from ETHNews](https://www.ethnews.com/author/trent-rhode) emailed me a bunch of questions around security token standards. I wrote up a bunch of background and answered his questions_

_The article was published on January 1st with a few quotes from what I wrote: [Moving Digital Securities Forward In 2019: Addressing Standards Interoperability](https://www.ethnews.com/moving-digital-securities-forward-in-2019-addressing-standards-interoperability)_

_A correction to that article -- Polymath may be using ST20 as a marketing term, but are spearheading the ERC1400 described below_

---

> Can you please spell your full name and professional title you'd like to be referred to as?

Boris Mann, Co-founder, Head of Community & Operations, [Special Projects & Decentralized Engineering Company](https://spade.builders)
 
> What is your interest and experience with security tokens, and what is your experience with securities and investments in general?

My previous company, [Finhaven](https://finhaven.com), is building a security token issuance platform. I did early work starting in 2017 around security tokens on Ethereum, including workshops and regulatory feedback in Canada.

I have a history around investing & advising early stage startups. I founded the first startup accelerator in Canada, ran a small seed fund for several years, and helped create a [standard set of startup investment documents for Canada](https://www.nacocanada.com/commondocs) with the National Angel Capital Organization.

Today, working on low-level standards and infrastructure for the Ethereum ecosystem, I'm mainly interested in supporting the standardization process.

Several security token standards have been proposed, including ones such as the ERC1400 family (see [thesecuritytokenstandard.org](https://thesecuritytokenstandard.org/)), that rely on the [FISSION Codes](https://fission.codes) standard that my cofounder Brooke has proposed.

> Jamie Finn, co-founder and president of Securitize, said we only need ERC-20 for security tokens. How is this possible? Don't we need other capabilities beyond what ERC-20 can do, which would create a new standard?

ERC20 is an example of an application layer smart contract standard. These application layer standards rely mainly on convention and adoption, as they are not enforced by Ethereum clients. The true EIPs generally define changes to the Ethereum system that require coordination and a hard fork to deploy. _(Note: this is an aside but may be important to understand. The last sentence about EIPs could be cut)._

The way that application layer standards are currently defined in the Ethereum Improvement Proposal (EIP) process, many of them can be combined. So, you can have a token that conforms to the ERC20 standard, but includes additional features that make it compliant with other standards. As an example, the ERC1400 proposal uses ERC20[^erc1400erc20] as its base (which it recently decided to do rather than the more modern & secure ERC777 which hasn't been widely adopted yet, and whose standard isn't final).

I don't know if Securitize has submitted any proposed standards. They might be looking for technical standards outside of the Ethereum ecosystem, which is certainly possible.

[^erc1400erc20]: for reference, this is the [very technical EIP process illustrated by ERC1400 being based on ERC20](https://github.com/ethereum/EIPs/issues/1411#issuecomment-445898706) but may be useful background for you in understanding how EIPs can depend on each other and tokens can be composed of several standards.

> Regarding this thread: [ethmagicians//erc-1462-base-security-token/1501](https://ethereum-magicians.org/t/erc-1462-base-security-token/1501)
>
> You wrote it is your belief that "there is going to need to be broad technical interoperability, as well as regulatory interoperability."
>
> Could you please explain this a bit further? What do you see as the key technical interoperability that is needed, and how would you explain this in more detail to a lay person?

Just like the ERC20 standard caused an explosion of tokens because of support in development tools, exchanges, wallets, and everything in between, broad technical interoperability of security tokens would mean that many users and market participants would work with the standard.

Today, stock markets are effectively defined stock exchange by stock exchange, or at most country by country. I think the most interesting role for tokenized securities is when they are global day one. Half of the issue is technical interoperability, the other half is regulatory.

I wish it were as simple as VHS vs Betamax, but it's like we have 100 versions of Betamax, across multiple different public blockchains. The forward momentum in security token standards for Ethereum really only heated up in September of this year with the submission of ERC1400. Seeing the activity, various other players quickly also submitted standards proposals. Some of them ended up joining the ERC1400, others still want something simpler or different.

> You also said that you agree on keeping regulatory things separate. Can you explain what you mean by this?

I've heard stories of lawyers defining token interfaces, and so far security tokens have been hand built code by code, and regulatory country by country. I think that regulatory needs and use cases should inform the technical design, but that technical interoperability will be helpful in defining regulatory interactions.

> Regarding: "I still think that over-focusing on ERC20 is a mistake – vs. pulling the bandaid off and getting broad movement to 777 along with standards like this".
>
> Why do you think focusing on ERC20 is a mistake? What would it look like to use standards like 777 for security tokens?

Many people outside of technical working groups have been exposed to ERC20 -- and other standards like the ERC721 Non-Fungible Token made famous by Crypto Kitties.

I've seen a number of people name standards after a particular Ethereum ERC. This is a mistake. We are always upgrading and improving technology, and need to keep track of versions -- but we can't have innovation stop at a single number.

It would be like calling HTTP from May 1996 after its IETF RFC 1945[^ietf1945] -- which has in turn has had dozens of improvements in the form of other RFCs, and today Google and others are working on HTTP2 and HTTP3.

[^ietf1945]: The [original RFC where HTTP was defined, RFC 1945](https://tools.ietf.org/html/rfc1945).

This is of course hard to explain to non technical users, especially those who haven't been exposed to open source or standards work.

So the message is, ERC20 is a particular standard created very early in the development of the Ethereum smart contract and blockchain system. It became a marketing term.

Newer standards like ERC777 will continue to evolve. We've learned already, and will continue to learn, so I want to see more focus on newer standards.

And, kind of an aside, players in the ecosystem like exchanges have been underinvesting in technology. It hasn't been in their interest to have to upgrade their systems to support new standards. And wallets and so on -- in a system that's still evolving very quickly, everyone has to do work together. And, the vast majority of the code is open source, so it's not like we're asking these ecosystem players to have to invent this new technology, just implement it.

> Do you feel there at too many security standards popping up? Please briefly elaborate on what you would see as a solution, if so. If not, please elaborate on why not.

As I mentioned above, there has now been a "land rush" of submitting standards. Do I wish people would wake up and figure out how to work together? Yes.

What I have realized is that there was an early rush of people releasing open source code. But open source code is not the same thing as a standard. What forum is being used to add a little bit of governance to evolve standards jointly? Can different companies implement the standard without having to copy and paste the code? If yes, then you've written up a specification that can be used as a standard.

The ERC process in Ethereum does not mandate usage, but it is does have a basic model of governance that a group of people and companies can collaborate around.

I think the various groups offering up security token standards need to understand that this isn't a business or marketing win. The entire industry will win when they understand that a standards process is the most important.

Especially if we want this to fit into #DeFi -- having it work just on one issuance platform or one exchange isn't going to work. And that "winning" doesn't look like "owning" ERC20, but rather partnerships, interoperability, and regulatory alignment.

Lots of the finance people in the space don't understand open source, never mind standards, so I expect this to shake out over time.

Winning looks more like developer relations at the technical layer. Producing high quality standards, supported by reference open source implementations that can be plugged into wallets and exchanges. Of course there will be competition even around winning standards, but we are going to have to get to a standard.
