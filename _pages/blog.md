---
permalink: /blog/
title: "Blog"
hide_title: true
author_profile: false
redirect_from:
  - /blog/sorted-or-mixed/
  - /blog/old-cleavages-new-maps/
---

{% assign all_topics = "" | split: "" %}{% for post in site.posts %}{% for t in post.topics %}{% assign all_topics = all_topics | push: t %}{% endfor %}{% endfor %}{% assign topics = all_topics | uniq %}
<div class="blog-layout">
<nav class="blog-topics" aria-label="Topics">
  <a class="tag is-active" href="#" data-topic="">#all</a>
  {% capture counted %}{% for t in topics %}{% assign n = 0 %}{% for x in all_topics %}{% if x == t %}{% assign n = n | plus: 1 %}{% endif %}{% endfor %}{{ n | prepend: "000" | slice: -3, 3 }}|{{ t }};{% endfor %}{% endcapture %}
  {% assign sorted = counted | split: ";" | sort | reverse %}
  {% for row in sorted %}{% assign parts = row | split: "|" %}{% if parts[1] %}<a class="tag" href="#{{ parts[1] }}" data-topic="{{ parts[1] }}">#{{ parts[1] }}</a>
  {% endif %}{% endfor %}
</nav>
<div class="blog-list">
{% assign regular = site.posts | where_exp: "p", "p.list_last != true" %}{% assign last = site.posts | where_exp: "p", "p.list_last == true" %}{% assign ordered = regular | concat: last %}
{% for post in ordered %}
<article class="archive__item blog-item" data-topics="{{ post.topics | join: ' ' }}">
  <h2 class="archive__item-title" style="margin-top: 0;"><a href="{{ post.url | relative_url }}" target="_blank" rel="noopener">{{ post.title }}</a></h2>
  <p class="page__meta" style="margin: 0 0 0.5em;">{{ post.date | date: "%-d %B %Y" }}</p>
  {% if post.excerpt %}<p class="archive__item-excerpt">{{ post.excerpt | markdownify | strip_html | truncate: 300 }}</p>{% endif %}
</article>
{% endfor %}
</div>
</div>

<script>
(function () {
  var links = document.querySelectorAll('.blog-topics a');
  var items = document.querySelectorAll('.blog-item');
  function show(topic) {
    links.forEach(function (a) { a.classList.toggle('is-active', a.getAttribute('data-topic') === topic); });
    items.forEach(function (el) {
      var t = ' ' + el.getAttribute('data-topics') + ' ';
      el.style.display = (!topic || t.indexOf(' ' + topic + ' ') !== -1) ? '' : 'none';
    });
  }
  links.forEach(function (a) {
    a.addEventListener('click', function (e) {
      e.preventDefault();
      var topic = a.getAttribute('data-topic');
      show(topic);
      history.replaceState(null, '', topic ? '#' + topic : location.pathname);
    });
  });
  var start = decodeURIComponent(location.hash.slice(1));
  if (start) show(start);
})();
</script>
