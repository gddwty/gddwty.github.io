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

I study Indonesian politics and write reports for NGOs and policymakers. Much of what I know comes from conversations with my network of sources and from looking at statistical data.

I love reading [Balinese history](/blog/wijk-kampoeng-bandjar/){:target="_blank" rel="noopener"}, mostly anthropology and archaeology, and I find the island's colonial and precolonial past fascinating. Perhaps it runs in the family: I come from a long line of mountain priests, the [Kubayan](/blog/elder-brother-of-the-king/){:target="_blank" rel="noopener"}, with obligations to our temples and to the holy mountain of Batukaru.

If you'd like to connect, I'm on <a class="inline-pill" href="https://www.linkedin.com/in/gde-dwitya-141127286/" target="_blank" rel="noopener"><i class="fab fa-linkedin" aria-hidden="true"></i> LinkedIn</a>.

</div>

<div class="recent-posts">
<p class="recent-posts__label"><a class="tag" href="{{ '/blog/' | relative_url }}">#fromtheblog</a></p>
{% for post in site.posts limit:4 %}
<p class="recent-posts__item"><a href="{{ post.url | relative_url }}" target="_blank" rel="noopener">{{ post.title }}</a></p>
{% endfor %}
</div>
