---
layout: default
title: Kitchen Gear Reviews
description: Honest reviews of budget-friendly kitchen tools and meal prep gear. We only recommend things worth buying.
permalink: /reviews/
---

<div class="container" style="padding: 48px 20px;">

<h1>Kitchen Gear Reviews</h1>
<p style="color: var(--text-muted); font-size: 17px; margin-bottom: 36px;">Honest, budget-focused reviews of containers, appliances, and tools worth your money.</p>

<div class="post-grid">
  {% assign review_posts = site.posts | where_exp: "post", "post.categories contains 'reviews'" %}
  {% if review_posts.size > 0 %}
    {% for post in review_posts %}
    <article class="post-card">
      {% if post.image %}
      <a href="{{ post.url | relative_url }}">
        <img src="{{ post.image | relative_url }}" alt="{{ post.image_alt | default: post.title }}" class="post-card-image" loading="lazy" />
      </a>
      {% endif %}
      <div class="post-card-body">
        <h3 class="post-card-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <p class="post-card-excerpt">{{ post.excerpt | strip_html | truncate: 120 }}</p>
        <div class="post-card-meta">
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%b %-d, %Y" }}</time>
          {% if post.read_time %} · {{ post.read_time }} min read{% endif %}
        </div>
      </div>
    </article>
    {% endfor %}
  {% else %}
    <p style="color: var(--text-muted);">Reviews coming soon — check back shortly.</p>
  {% endif %}
</div>

</div>
