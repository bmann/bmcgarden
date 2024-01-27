---
permalink: /notes/opensource/
aliases:
  - Open Source
---

I like to tell people about my [[Three Definitions of Open Source]] as context. 

I’m interested in [[Commons Funding]] and [[Open Source Licensing]], but most especially [[Commons Based Peer Production]]: how to work together to build.

Notes tagged with open source:

<ul>
{% for note in site.notes %}
{% if post.tags contains “opensource” %}
<li><a href="{{ post.url }}" class="internal-note">{{ post.title }}</a></li>
{% endif %}
{% endfor %}
</ul>