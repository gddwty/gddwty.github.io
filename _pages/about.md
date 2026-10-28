---
permalink: /
title: "About"
hide_title: true
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<div class="bio" markdown="1">

I write about Indonesian politics and brief policymakers. Much of what I know comes from conversations with my network of sources and from looking at statistical data.

If you'd like to connect, I'm on <a class="inline-pill" href="https://www.linkedin.com/in/gde-dwitya-141127286/" target="_blank" rel="noopener"><i class="fab fa-linkedin" aria-hidden="true"></i> LinkedIn</a>.

</div>

<div class="recent-posts">
<p class="recent-posts__label"><a class="tag" href="{{ '/blog/' | relative_url }}">#fromtheblog</a></p>
{% assign home_posts = site.posts | where_exp: "p", "p.list_last != true" %}{% for post in home_posts limit:4 %}
<p class="recent-posts__item"><a href="{{ post.url | relative_url }}" target="_blank" rel="noopener">{{ post.title }}</a></p>
{% endfor %}
</div>
