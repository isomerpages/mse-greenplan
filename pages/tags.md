---
layout: default
title: Tags
permalink: /tags/
---

<h1>Tags</h1>

{% for tag in site.data.tags %}
  <h2>{{ tag.name }}</h2>
  <ul>
    {% for post in site.posts %}
      {% if post.tags contains tag.slug %}
        <li>
          <a href="{{ post.url }}">{{ post.title }}</a>
        </li>
      {% endif %}
    {% endfor %}
  </ul>
{% endfor %}
