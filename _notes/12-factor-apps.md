---
title: 12 Factor App
link: https://12factor.net
date: 2021-01-24
published: 2011-06-03
---

A foundational piece of writing about how to architect applications in the modern era, written by the [[Heroku]] founders in 2011/2012. Published at [12factor.net](https://12factor.net).

From the Introduction:

> In the modern era, software is commonly delivered as a service: called web apps, or software-as-a-service. The twelve-factor app is a methodology for building software-as-a-service apps that:
> 
> * Use declarative formats for setup automation, to minimize time and cost for new developers joining the project;
> * Have a clean contract with the underlying operating system, offering maximum portability between execution environments;
> * Are suitable for deployment on modern cloud platforms, obviating the need for servers and systems administration;
> * Minimize divergence between development and production, enabling continuous deployment for maximum agility;
> * And can scale up without significant changes to tooling, architecture, or development practices.
> 
> The twelve-factor methodology can be applied to apps written in any programming language, and which use any combination of backing services (database, queue, memory cache, etc).

From the Background section:

> Our motivation is to raise awareness of some systemic problems we’ve seen in modern application development, to provide a shared vocabulary for discussing those problems, and to offer a set of broad conceptual solutions to those problems with accompanying terminology. The format is inspired by Martin Fowler’s books [Patterns of Enterprise Application Architecture and Refactoring](https://books.google.com/books/about/Patterns_of_enterprise_application_archi.html?id=FyWZt5DdvFkC).

Source is [on Github](https://github.com/heroku/12factor). Created by @AdamWiggins, contributions from:

> James Lindenbaum, Mark McGranaghan, Chris Stolt, Ryan Daigle, Mark Imbriaco, Keith Rarick, Will Leinweber, Jesper Jørgensen, James Ward, Adam Seligman, Phil Hagelberg, Jon Mountjoy, Matthew Turland, Daniel Jomphe, Mattt Thompson, Anand Narasimhan, Lucas Fais, Pete Hodgson