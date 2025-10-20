---
layout: default
title: Voyage Logs & Updates
permalink: /blog/
---

<div class="blog-index">
  <h1>Blog: From the Helm</h1>
  <p class="blog-subtitle">Real-time dispatches from our Allures 45.9 hacks, AI experiments, and expedition with kids wisdom.</p>

  {% if site.posts.size > 0 %}
    {% for post in site.posts limit: 5 %}
      <article class="post-teaser">
        <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        <p class="post-meta">{{ post.date | date: "%B %d, %Y" }}</p>
        <div class="post-excerpt">
          {{ post.content | strip_html | truncatewords: 30 }}
        </div>
        <a href="{{ post.url | relative_url }}" class="read-more">Read More →</a>
      </article>
    {% endfor %}
  {% else %}
    <p>No posts yet—stay tuned for our first voyage log!</p>
  {% endif %}
</div>
