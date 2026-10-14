---
permalink: /
title: "About"
hide_title: true
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

I study Indonesian politics, and have done so for well over a decade. I also prepare reports for international NGOs and brief private clients on the country's national and local politics, mostly off the record. Much of what I know comes from years of conversations with the people who practise it.

Occasionally I write for *The Jakarta Post*, and I teach at a graduate school in Jakarta.

I received my PhD in Political Science from Northwestern University in 2021.

<div class="recent-posts">
<p class="recent-posts__label">Recent blog posts</p>
{% for post in site.posts limit:2 %}
<p class="recent-posts__item"><a href="{{ post.url | relative_url }}" target="_blank" rel="noopener">{{ post.title }}</a> <span class="recent-posts__date">· {{ post.date | date: "%-d %B %Y" }}</span></p>
{% endfor %}
</div>
