---
layout: default
title: Home
id: home
permalink: /
---
<style>
  .microblog_timeline, .callout {padding: 2em 1.5em; background: #f5f7ff;}
</style>
# Hi 👋 Welcome to Boris Mann's Homepage

  <ul>
    {% for blog in site.posts limit:5 %}
      <li class="blog-entry" style="margin-bottom: 5px;">
        <a class="internal-link" href="..{{ blog.url }}">{{ blog.title }}</a> <time>{{ blog.date | date: "%B %-d, %Y" }}</time>
      </li>
    {% endfor %}
  </ul>

  <a href="/blog/" class="internal-link">More »</a>

  <h2>Digital Garden</h2>

{% assign notehtml = '' %}
{% assign recentnotes = site.notes | sort: 'last_modified_at' | reverse %}
{% assign notecount = 0 %}
{% for note in recentnotes %}
  {% if note.section != 'journal' %}
    {% assign notehtml = notehtml | append: "<a class='internal-link' href='" | append: note.url | append: "'>" | append: note.title | append: "</a>" %}
    {% assign notecount = notecount | plus:1 %}
    {% if notecount < 3 %}
      {% assign notehtml = notehtml | append: ", " %}
    {% else %}
      {% break %}
    {% endif %}
  {% endif %}
{% endfor %}

<p>As of July 2023, I moved my Digital Garden Notes to their own site. There's a <a class="internal-link" href="../notes/seeds/">Seeds page</a> with links into various themes and recommended articles, or you can browse the minimal <a class="internal-link" href="../notes/">Notes graph</a>.</p>

<p>These are the three most recently modified notes: {{ notehtml }}.</p>

<div style="margin-top: 0.5em">
{% assign seednotes = site.notes | where_exp: "note", "note.seed" %}
{% for seednote in seednotes %}
    <div>
      <div style="margin-bottom: 0.5em;">{{ seednote.content }}</div>
      <cite><a href="{{ seednote.link }}">{{ seednote.title }} by {{ seednote.author }}</a></cite>
    </div>
{% endfor %}
</div>

  <h2>Personal microblog</h2>

  Most recent post from my more [personal blog »](https://blog.bmannconsulting.com)

  <script type="text/javascript" src="https://micro.blog/sidebar.js?username=boris&count=1"></script>

  <hr />


<style>
  .wrapper {
    max-width: 46em;
  }
  .microblog_post {
    padding: 0px 30px 10px 20px;
  }
</style>
