---
layout: blog           # keeps header/footer/nav styling
title: Posts
permalink: /blog/         # final URL will be /blog/
---

<h1>All posts</h1>
<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <span class="post-date">{{ post.date | date: "%Y-%m-%d" }}</span>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
