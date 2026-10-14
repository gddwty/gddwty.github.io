---
permalink: /blog/
title: "Blog"
hide_title: true
author_profile: true
redirect_from:
  - /blog/sorted-or-mixed/
  - /blog/old-cleavages-new-maps/
---

{% for post in site.posts %}
<article class="archive__item" style="margin-bottom: 2em;">
  <h2 class="archive__item-title" style="margin-top: 0;"><a href="{{ post.url | relative_url }}" target="_blank" rel="noopener">{{ post.title }}</a></h2>
  <p class="page__meta" style="margin: 0 0 0.5em;">{{ post.date | date: "%-d %B %Y" }}</p>
  {% if post.excerpt %}<p class="archive__item-excerpt">{{ post.excerpt | markdownify | strip_html | truncate: 300 }}</p>{% endif %}
</article>
{% endfor %}
