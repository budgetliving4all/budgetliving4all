---
layout: default
title: Budget Cooking Tips
description: Practical tips for cutting your grocery bill without sacrificing good food. Real strategies, real prices.
permalink: /budget-tips/
---

<div class="container" style="padding: 48px 20px;">

<h1>Budget Cooking Tips</h1>
<p style="color: var(--text-muted); font-size: 17px; margin-bottom: 36px;">Real strategies to spend less at the grocery store and waste less in the kitchen.</p>

<div class="post-grid">
  {% assign budget_posts = site.posts | where_exp: "post", "post.categories contains 'budget-tips'" %}
  {% if budget_posts.size > 0 %}
    {% for post in budget_posts %}
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
    <p style="color: var(--text-muted);">Guides coming soon — check back shortly.</p>
  {% endif %}
</div>

</div>
