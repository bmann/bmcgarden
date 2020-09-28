---
title: Jekyll
---

## Set env variable PAGES_REPO_NWO to build on [[Netlify]]

Set the environment variable ```PAGES_REPO_NWO``` to a repo such as ```spadebuilders/EIPs``` if you want to have Jekyll sites build on Netlify.

## Posts by Year

```
{% raw %}
{% for post in site.posts %}
  {% capture current_year %}{{ post.date | date: "%Y" }}{% endcapture %}
  {% if current_year != previous_year %}
    {% unless forloop.first %}
      </ul>
    {% endunless %}
    <h2>{{ current_year }}</h2>
    <ul>
    {% assign previous_year = current_year %}
  {% endif %}
  <li><a href="{{ post.url }}" class="internal-link">{{ post.title }}</a></li>

  {% if forloop.last %}
    </ul>
  {% endif %}
{% endfor %}
{% endraw %}
```

## Reducing Jekyll Build Times

By Colin Garvey at [[Forestry]] https://forestry.io/blog/how-i-reduced-my-jekyll-build-time-by-61/

## Using CommonMark GHPages Markdown Processor

Using GH-flavoured CommonMark instead of kramdown

In the `Gemfile`:
```
gem "jekyll-commonmark-ghpages"
```

In the `_config.yml` file:

```
markdown: CommonMarkGhPages

commonmark:
  options: ["SMART", "FOOTNOTES"]
  extensions: ["strikethrough", "autolink", "table"]

plugins:
  - jekyll-commonmark-ghpages
```

Autolink is key -- means you can just past addresses and they'll be linked automatically.