---
---

link:: https://hackernoon.com/why-the-fuss-about-serverless-4370b1596da0
author:: [[Simon Wardley]]
tags:: #article, #serverless, #[[Hackernoon]]
published:: [[Nov 23rd, 2016]]

- Quotes
	- Today, we use the term micro services to describe this separation of functions and provision as web services. We’re moving away from the monolith program containing all the functions to a world of separated and discrete functions. A utility platform just enables this and abstracts the whole underlying process from the developer.
	- I built a small trading platform in a day or so because I was able to re-use so many functions created by others. I didn’t have to worry about building a platform and the concept of a server, capacity planning and all that “yak shaving” was far from my mind. The efficiency, speed of agility and speed of development are just a given. However, these changes are not really the exciting parts. ==The killer, the gotcha is the billing by the function.==
	- Billing by the function not only enables me to see what is being used but also to quickly identify costly areas of my program. I would often find that one function was causing the majority of the cost because of the way I had coded it. My way of retrieving trades in my program was literally killing me with cost. I could see it, I could quickly direct investment into improving that one costly function and reduce the overall cost. Monitoring by cost of function changes the way we work — well, it changed me and I’m pretty sure this will impact all of you.
	-