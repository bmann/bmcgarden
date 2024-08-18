---
aliases:
  - BUSL
title: Business Source LIcense
tags:
  - licensing
  - opensource
link: https://mariadb.com/bsl11/
---
Created by MariaDB, and the license text is copyrighted by them, and "Business Source License" is a trademark of MariaDB.

> The Business Source License (this document, or the “License”) is not an Open Source license. However, the Licensed Work will eventually be made available under an Open Source License, as stated in this License.

I've added links and a few of the items from the [[Business Source License/FAQ]] and the [[Business Source License/MariaDB FAQ]] that have useful explanations.

I went to see if [[Kyle Mitchell]] had written anything on BSL, and it's only mentioned in an aside:

> One way to clear such a high bar is to make a ton of new value, all the time, at a relentless pace. The **Business Source License** and other time-delay release pacts implement exactly that kind of commitment in legal terms. Business-wise, it’s a treadmill. Stand still, you fall off the back. - [Kyle Mitchell, Changeblog, Sept 2019](https://writing.kemitchell.com/2019/09/05/Changeblog.html)
## Adopting BSL FAQ

From MariaDB, [Adopting and Developing BSL Software](https://mariadb.com/bsl-faq-adopting/)

> Business Source License (BSL) was created by David Axmark and Michael Widenius to provide a mutually beneficial balance between the user benefits of true Open Source software that is free of cost and provides open access to all of the product code for modification, distribution, etc., and the sustainability needs of software developers to continue delivering product innovation and maintenance.
> 
> The BSL is structured to allow free and open usage for the majority of use cases, and only requires a commercial license by those who use the software above a certain threshold, which is typically indicative of an environment that is delivering significant value to a business.
> 
> BSL gives users complete access to the source code so users can modify, distribute and enhance it. It also guarantees a path for the software to become Open Source over time so that users will never be locked into a single vendor. These features help preserve the critical freedom aspects of Open Source (as defined by the [[OSI]] in the [[Open Source Definition]]) while enabling a viable business model for professional software developers.
> 
> This FAQ is designed to address questions for any developer, or any company, interested in working on BSL software or adopting BSL for their own business.

### What is Business Source License (BSL)?

> BSL is a new alternative to Closed Source or Open Core licensing models. Under BSL, the source code is freely available from the start and it is guaranteed to become Open Source at a certain point in time (i.e., the Change Date). Usage below a specific level in the BSL is always completely free. Usage above the specified level requires a license from the vendor until the Change Date, at which point all usage becomes free.

### What is the purpose of BSL?

> To create a license that strikes a balance between being able to run a financially viable software company while still supporting the original tenets of Open Source, such as empowering all software developers to be part of the innovation cycle – giving them open access to the code so they can modify or distribute the software by making the entire source code available from the start. Ultimately, we hope that BSL will create more Open Source software.

## MariaDB BSL FAQ

<https://mariadb.com/bsl-faq-mariadb/>

### How is the BSL different from Open Core?

> [[Open Core]] offers some code under Open Source terms, but non-core code is not under Open Source terms, is not available in source form, cannot be modified and compiled, cannot be contributed to, and will never be Open Source. By using Open Core software, like with closed source code, you are locked to one vendor. With BSL, as compared to Open Core, the source code is available from the start, can be modified and compiled, contributions are encouraged, the product will become fully Open Source after a period of time and remains free for non-production use. The importance of the eventual Open Source is that users are free from vendor lock-in. If the vendor decides to stop contributing to the code, users have open access and can modify, update and extend as needed.

### How is the BSL different from dual GPL/commercial licensing?

When using [[dual licensing]] with [[GPL]], companies must pay for a commercial license to use the software with their closed source code. With BSL, the companies are only paying for the software if they want to make production use of the software. ==From a vendor perspective, GPL dual licensing only works for infrastructure products that other companies want to deeply embed in their product. BSL works for any kind of software product.==

### How is BSL different from the Fair Source License ?

> The [[Fair Source License]] uses the number of users as a limitation, which makes sense for some types of software such as stand-alone applications, but not for all. BSL limitations are more general and can vary from project to project by including an Additional Use Grant, depending on what makes sense for a balance between free usage and paid usage. In addition, BSL code is guaranteed to become Open Source software after a certain specified time.

## Hashicorp BSL

<https://www.hashicorp.com/bsl>

[[Hashicorp]]'s parameters for the BSL, paraphrased into plain english:

* Additional Use Grant says that production use is allowed, except if it is competitive with HashiCorp's products.

- After 4 years, the release becomes available under [[Mozilla Public License]]
