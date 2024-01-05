---
layout: default
title: Home
id: home
permalink: /
---
<style>
  .microblog_timeline, .callout {padding: 0.25em 0.25em 1em 1em; background: #f5f7ff; border-radius: 25px;}
  .wrapper {
    max-width: 46em;
  }

  time {
    
  }

  a.journal-link {
    all: unset;
    cursor: pointer;
    text-decoration: underline;
    
  }
  a.journal-link::after {
    all: unset;
  }

</style>
# Hi 👋 Welcome to Boris Mann's Homepage

<p>I'm interested in [[Open Source Licensing]], community, co-operative models. Pooling capital and collaboration. I'm the founder of [[Fission]]. In Canada I help run the [[CoSocial]] Community Co-op. In Vancouver, I'm one of the organizers of [[DWebYVR]]. I like to cook & eat and have a [[FoodWiki]].</p>

{% comment %}
  <ul>
    {% for blog in site.posts limit:5 %}
      <li class="blog-entry" style="margin-bottom: 5px;">
        <a class="internal-link" href="..{{ blog.url }}">{{ blog.title }}</a> <time>{{ blog.date | date: "%B %-d, %Y" }}</time>
      </li>
    {% endfor %}
  </ul>

  <a href="/blog/" class="internal-link">More »</a>
{% endcomment %}

  <h2>Digital Garden 🌱</h2>

{% assign notehtml = '' %}
{% assign recentnotes = site.notes | sort: 'last_modified_at' | reverse %}
{% assign notecount = 0 %}
{% for note in recentnotes %}
  {% if note.section != 'journal' %}
    {% assign notehtml = notehtml | append: "<a class='internal-link' href='" | append: note.url | append: "'>" | append: note.title | append: "</a>" %}
    {% assign notecount = notecount | plus:1 %}
    {% if notecount < 5 %}
      {% assign notehtml = notehtml | append: ", " %}
    {% else %}
      {% break %}
    {% endif %}
  {% endif %}
{% endfor %}

Browse the local <a class="internal-link" href="../notes/">Notes graph</a>.

These are the five most recently modified local notes: {{ notehtml }}.

## Journal Entries

The last few days of [Journal](/journal) entries:

{% comment %}<!-- https://stackoverflow.com/questions/46672231/in-jekyll-how-to-show-posts-from-last-week -->{% endcomment %}
  {% assign timeframe = 172800 %}
<ul style="list-style-type: none;">
  {% for post in site.journals %}
    {% assign post_in_seconds = post.date | date: "%s" | plus: 0 %}
    {% assign recent_posts = "now" | date: "%s" | minus: timeframe  %}

    {% if post_in_seconds > recent_posts %}
<li style="padding-bottom: 0.5em;"><a href="{{ post.url }}" class="journal-link"><time datetime="page.date | date_to_xmlschema">{{ post.date | date: '%A %l:%M%P' }}</time></a>&nbsp;{{ post.content | strip_html | truncatewords: 30 }}&nbsp;</li>
    {% endif %}
{% endfor %}
</ul>

<hr />

<!-- 
<a href="https://cosocial.ca/@boris" rel="me">@boris@cosocial.ca</a>
<a href="https://toolsforthought.social/@boris" rel="me">@boris@toolsforthought.social</a>
--> 
