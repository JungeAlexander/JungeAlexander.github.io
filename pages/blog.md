---
layout: page
title: blog
description: Website created by Alexander Junge with GitHub Pages
---

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.date | date_to_long_string }} - {{ post.title }}</a>
      <small>{{ post.excerpt }}</small>
    </li>
  {% endfor %}
</ul>
