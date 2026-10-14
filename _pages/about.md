---
permalink: /
title: "About"
hide_title: true
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

I write about and teach Indonesian politics. I also prepare reports and brief clients on the country's political issues, at both the national and subnational levels. Much of what I know comes from conversations with people who have skin in the game and from careful work with statistical data.

I received my BA from Universitas Gadjah Mada and my PhD in Political Science from Northwestern University, Chicago.

<div class="recent-posts">
{% for post in site.posts limit:2 %}
<p class="recent-posts__item"><a href="{{ post.url | relative_url }}" target="_blank" rel="noopener">{{ post.title }}</a> <span class="recent-posts__date">· {{ post.date | date: "%-d %B %Y" }}</span></p>
{% endfor %}
</div>
