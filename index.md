---
layout: default
title: "The Year of 3K"
---

<h1>The Year of 3K</h1>

<p style="font-size: 1.1rem; color: var(--cream-300); margin-bottom: 2rem;">
  Systems, code, and the shapes things take when nobody's watching.
</p>

<ul class="post-list">
  {% for post in site.posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
  </li>
  {% endfor %}
</ul>
