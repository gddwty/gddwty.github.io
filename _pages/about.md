---
permalink: /
title: "About"
hide_title: true
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

I write about and teach Indonesian politics. I also prepare reports and brief clients on the country's political issues. Much of what I know comes from conversations with my network of sources and from looking at statistical data.

I received my BA from Universitas Gadjah Mada and my PhD in Political Science from Northwestern University, Chicago.

<div class="recent-posts">
<p class="recent-posts__label"><a class="tag" href="{{ '/blog/' | relative_url }}">#fromtheblog</a></p>
{% for post in site.posts limit:2 %}
<p class="recent-posts__item"><a href="{{ post.url | relative_url }}" target="_blank" rel="noopener">{{ post.title }}</a></p>
{% endfor %}
</div>
