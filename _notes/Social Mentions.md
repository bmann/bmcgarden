---
title: Social Mentions
---

Many different tools support Social Mentions -- _@name_ typed into a message or a document or a chat, which usually sets off a notification to the person being mentioned.

[[Jekyll]] has a plugin where you can link mentions https://github.com/jekyll/jekyll-mentions -- but it only works for one network.

Since I consistently want to link to things on [[AllTheBestRecipes]] or Twitter or Github, I'm going to make a simple [Jekyll data file](https://jekyllrb.com/docs/datafiles/) called `entities.yml` where I can define these links.

It will look a little something like this:

```yaml
- name: Coho
  link: https://allthebest.recipes/t/coho-commissary-coffee/346
- name: allthebestrecipes
  link: https://allthebest.recipes
  instagram: https://instagram.com/allthebestrecipes
  twitter: ATBRecipes
```