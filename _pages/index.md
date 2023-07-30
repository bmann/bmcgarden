---
layout: default
title: Home
id: home
permalink: /
---

# Boris Mann's Homepage

<p style="padding: 3em 2em; background: #f5f7ff; border-radius: 4px;">
  Hi 👋 This is the newest iteration of my homepage and long term archive. I put long form tech blog posts here. 
</p>

## Recent blog posts

  {% assign blogcount = 0 %}
  {% assign bloglimit = 5 %}
  {% assign recentblogs = site.posts | sort: 'date' | reverse %}
  <ul>
    {% for blog in recentblogs %}
        {% if blog.section == 'blog' and blogcount < bloglimit %}
          <li class="blog-entry" style="margin-bottom: 5px;">
            <a class="internal-link" href="{{ blog.url }}">{{ blog.title }}</a>
          </li>
            {% assign blogcount = blogcount | plus: 1 %}
        {% elsif blogcount >= bloglimit %}
            {% break %}
        {% endif %}
    {% endfor %}
  </ul>

  <a href="/blog/" class="internal-link">More »</a>

  <h2>Digital Garden</h2>

<p>As of July 2023, I moved my Digital Garden Notes to their own site. There's a <a class="internal-link" href="/notes/seeds/">Seeds page here</a> with links into various themes and recommended articles.</p>

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
