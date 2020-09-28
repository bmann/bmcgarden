--- 
layout: post
title: Weather Block
created: 1047572160
categories: 
- BMC
- Ottawa
- PHP
---
As you can see, I've added a weather block, showing everyone how cold it really is here in Ottawa. It's actually written from scratch by me, which I'm rather proud of.

Basically, it checks a local cache to see if the weather has been updated in the last hour. If not, it downloads the appropriate Environment Canada webpage and parses it for information (right now, just the current conditions).

These items are wrapped in just two functions -- getWeather and displayWeather. I really should have written it in <a href="http://www.php.net/manual/en/language.oop.php">OO PHP</a>, as I've been doing for lots of stuff lately, but it started as just a quick hack.

If you want a little PHP function to display weather on your site, <a href="http://www.bmannconsulting.com/module.php?mod=user&op=view&id=1">contact me</a> and I can send you a copy of the source.
