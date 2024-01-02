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

<p>Browse the local <a class="internal-link" href="../notes/">Notes graph</a>. I have some <a class="internal-link" href="../notes/seeds/">Seeds</a> to get you started.</p>

<p>These are the five most recently modified local notes: {{ notehtml }}.</p>

{% comment %}
<div style="margin-top: 0.5em">
{% assign seednotes = site.notes | where_exp: "note", "note.seed" %}
{% for seednote in seednotes %}
    <div>
      <div style="margin-bottom: 0.5em;">{{ seednote.content }}</div>
      <cite><a href="{{ seednote.link }}">{{ seednote.title }} by {{ seednote.author }}</a></cite>
    </div>
{% endfor %}
</div>
{% endcomment %}

  <h2>Personal microblog</h2>

  Most recent post from my more [personal blog](https://blog.bmannconsulting.com), which is cross-posted to my [[Mastodon]] account <a href="https://cosocial.ca/@boris" rel="me">@boris@cosocial.ca</a>.

  <script type="text/javascript" src="https://micro.blog/sidebar.js?username=boris&count=1"></script>

  <hr />
