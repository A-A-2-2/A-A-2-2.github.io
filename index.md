---
layout: default
title: Home
---

<ul class="post-list">
{% for post in site.posts %}
  <li class="post-item">
    <a class="post-title" href="{{ post.url }}">{{ post.title }}</a>

    <div class="post-meta">
      <span class="post-date">{{ post.date | date: "%Y-%m-%d" }}</span>

      {% if post.categories and post.categories.size > 0 %}
        <span class="post-cats">
          {% for c in post.categories %}
            <span class="post-cat">{{ c }}</span>
          {% endfor %}
        </span>
      {% endif %}
    </div>
  </li>
{% endfor %}
</ul>
