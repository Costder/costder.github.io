--- 
layout: default
title: "Joshua Herron — Systems Builder"
---

<h2>Posts</h2>

<ul class="post-list">
  {% for post in site.posts %}
  <li>
    <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <p>{{ post.description | default: post.excerpt | strip_html | truncate: 140 }}</p>
  </li>
  {% endfor %}
</ul>
