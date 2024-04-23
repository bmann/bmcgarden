---
layout: default
title: Home
id: home
permalink: /
---
<style>
  .callout {padding: 0.25em 0.25em 1em 1em; background: #f5f7ff; border-radius: 25px;}
  .wrapper {
    max-width: 46em;
  }

  a.journal-link {
    all: unset;
    cursor: pointer;
  }
  a.journal-link::after {
    all: unset;
  }

</style>
# Hi 👋 Welcome to Boris Mann's Homepage

I'm interested in [[Open Source Licensing]], community, co-operative models. Pooling capital and collaboration. In Canada I help run the [[CoSocial]] Community Co-op. In Vancouver, I'm one of the organizers of [[DWebYVR]]. I like to cook & eat and have a [[FoodWiki]].

The [[Feeds]] page has ways to subscribe.
## [Blog Posts 🖊](../blog/)

  <ul>
    {% for blog in site.posts limit:3 %}
      <li class="blog-entry" style="margin-bottom: 5px;">
        <a class="internal-link" href="..{{ blog.url }}">{{ blog.title }}</a> <time datetime="blog.date | date_to_xmlschema">{{ blog.date | date: "%B %-d, %Y" }}</time>
      </li>
    {% endfor %}
  </ul>

## [Digital Garden 🌱](../notes/)

{% assign notehtml = '' %}
{% assign recentnotes = site.notes | sort: 'last_modified_at' | reverse %}
{% assign notecount = 0 %}
{% for note in recentnotes %}
  {% if note.section != 'journal' %}
    {% assign notehtml = notehtml | append: "<a class='internal-link' href='" | append: note.url | append: "'>" | append: note.title | append: "</a>" %}
    {% assign notecount = notecount | plus:1 %}
    {% if notecount < 10 %}
      {% assign notehtml = notehtml | append: ", " %}
    {% else %}
      {% break %}
    {% endif %}
  {% endif %}
{% endfor %}

These are the ten most recently modified local notes: {{ notehtml }}.

## [Journal Entries 📓](../journal/)

{% assign journalposts = site.journals | reverse %}

  {% assign linksposted = 0 %}
  {% for post in journalposts %}
    {% if post.link %}
<p style="padding-bottom: 0.5em;">{{ post.content | strip_html | truncate: 100 }}&nbsp;<a href="{{ post.url }}" class="journal-link" style="font-size: x-small">#</a><br /><a href="{{ post.link }}">{{ post.link }}</a></p>
    {% assign linksposted = linksposted | plus: 1 %}
    {% endif %}
  {% if linksposted >= 5 %}{% break %}{% endif %}
{% endfor %}

<hr />

My personal Mastodon account is <a href="https://cosocial.ca/@boris" rel="me">@boris@cosocial.ca</a>. Journal items are cross-posted to <a href="https://toolsforthought.social/@boris" rel="me">@boris@toolsforthought.social</a>. All of my social profiles are [listed at bmann.ca](https://bmann.ca).
