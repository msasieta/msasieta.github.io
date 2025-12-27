---
layout: page
title: Notes on recent papers
permalink: /blog/
---

<div class="post-list">
  {% for post in site.posts %}
    <article class="post-card">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <div class="meta">
        <span>{{ post.date | date: "%b %-d, %Y" }}</span>
        {% if post.tags %}
          <span> · {{ post.tags | join: ", " }}</span>
        {% endif %}
        {% if post.paper_url %}
          <span> · <a href="{{ post.paper_url }}" target="_blank" rel="noopener">paper</a></span>
        {% endif %}
      </div>

      <p>{{ post.excerpt | strip_html | truncate: 220 }}</p>
    </article>
  {% endfor %}
</div>
