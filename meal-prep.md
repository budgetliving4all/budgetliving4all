---
layout: default
title: Meal Prep Guides
description: Step-by-step meal prep guides for beginners and budget cooks.
permalink: /meal-prep/
---
<div class="container">
  <div class="page-header">
    <h1>Meal Prep Guides</h1>
    <p>Batch cooking guides that work on a real schedule and a real budget.</p>
  </div>
  <div class="page-body">
    <div class="post-grid">
      {% assign cat_posts = site.posts | where_exp: "post", "post.categories contains 'meal-prep'" %}
      {% if cat_posts.size > 0 %}
        {% for post in cat_posts %}
        <article class="post-card">
          {% if post.image %}<a href="{{ post.url | relative_url }}"><img src="{{ post.image | relative_url }}" alt="{{ post.image_alt | default: post.title }}" class="post-card-image" loading="lazy" /></a>{% endif %}
          <div class="post-card-body">
            <h3 class="post-card-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
            <p class="post-card-excerpt">{{ post.excerpt | strip_html | truncate: 120 }}</p>
            <div class="post-card-meta"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%b %-d, %Y" }}</time>{% if post.read_time %} · {{ post.read_time }} min read{% endif %}</div>
          </div>
        </article>
        {% endfor %}
      {% else %}
        <p style="color: var(--text-muted);">Guides coming soon.</p>
      {% endif %}
    </div>
  </div>
</div>
