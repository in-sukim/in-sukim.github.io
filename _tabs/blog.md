---
layout: page
title: Blog
icon: fas fa-blog
order: 3
---

<div class="post-list">
  {% for post in site.posts %}
    {% if post.categories contains 'blog' %}
      <article class="post-item">
        <h2 class="post-title">
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h2>
        <div class="post-meta">
          <span class="post-date">{{ post.date | date: "%Y-%m-%d" }}</span>
        </div>
      </article>
    {% endif %}
  {% endfor %}
</div>
