---
layout: page
title: Notes
permalink: /blog/
---

<div class="post-list">
  {% for post in site.posts %}
    <article class="post-card">
      <h3>
        <a href="{{ post.url | relative_url }}">
          {{ post.title }}
        </a>
      </h3>

      <p class="meta">
        {{ post.date | date: "%b %-d, %Y" }}
        {% if post.paper_url %}
          · <a href="{{ post.paper_url }}" target="_blank" rel="noopener">paper</a>
        {% endif %}
      </p>

      <p>
        {{ post.excerpt | strip_html | truncate: 200 }}
      </p>
    </article>
  {% endfor %}
</div>
