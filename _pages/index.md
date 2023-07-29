---
layout: page
title: Home
id: home
permalink: /
---

# Welcome! 🌱

<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  An experimental rebuild of my site running <a href="../notes/digital-garden-jekyll-template/" class="internal-link">Digital Garden Jekyll Template</a>.
</p>

The <a href="../blog/" class="internal-link">Blog</a> and long term <a href="../archive/" class="internal-link">Archive</a> are the same as they have been.

Take a look at <a href="../notes/" class="internal-link">Notes</a> for the graph based notes explorer.

The <a href="../journals/" class="internal-link">Journals</a> are the most raw, including that they are not currently being parsed for wikilinks or backlinks.

## Recent blog posts

  {% assign blogcount = 0 %}
  {% assign bloglimit = 10 %}
  {% assign recentblogs = site.posts | sort: 'date' | reverse %}
  <ul>
    {% for blog in recentblogs %}
        {% if blog.section == 'blog' and blogcount < bloglimit %}
          <li class="blog-entry" style="margin-bottom: 20px;">
            <a class="internal-link" href="{{ blog.url }}">{{ blog.title }}</a>
          </li>
            {% assign blogcount = blogcount | plus: 1 %}
        {% elsif blogcount >= bloglimit %}
            {% break %}
        {% endif %}
    {% endfor %}
  </ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
