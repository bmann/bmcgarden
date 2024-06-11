---
permalink: /notes/opensource/
aliases:
  - Open Source
---
I like to tell people about my [[Three Definitions of Open Source]] as context. 

I’m interested in [[Commons Funding]] and [[Open Source Licensing]], but most especially [[Commons Based Peer Production]]: how to work together to produce and maintain things. Open source code and related open data goods are very common, but peer production and [[co-op]] structures can and should be applied to many more things.

Related notes:
<!-- tagged with open source, but not an app -->

<ul>
{% for post in site.notes %}
{% if post.tags contains "opensource" %}
{% unless post.tags contains "app" %}
<li><a href="{{ post.url }}" class="internal-link">{{ post.title }}</a></li>
{% endunless %}
{% endif %}
{% endfor %}
</ul>