---
permalink: /
title: "About"
hide_title: true
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

I write about and teach Indonesian politics. I also prepare reports and brief clients in private on the country's national and local politics. Much of what I know comes from conversations with people who have skin in the game and from careful work with statistical data.

I received my BA from Universitas Gadjah Mada (UGM) and my PhD in Political Science from Northwestern University, Chicago.

<div class="recent-posts">
<p class="recent-posts__label">Recent blog posts</p>
{% for post in site.posts limit:2 %}
<p class="recent-posts__item"><a href="{{ post.url | relative_url }}" target="_blank" rel="noopener">{{ post.title }}</a> <span class="recent-posts__date">· {{ post.date | date: "%-d %B %Y" }}</span></p>
{% endfor %}
</div>
