---
layout: default
title: Meal Prep Guides
description: Step-by-step meal prep guides for beginners and budget cooks. Learn to batch cook, save time, and cut your grocery bill.
permalink: /meal-prep/
---

<div class="container" style="padding: 48px 20px;">

<h1>Meal Prep Guides</h1>
<p style="color: var(--text-muted); font-size: 17px; margin-bottom: 36px;">Practical batch cooking guides — from beginner basics to full weekly plans.</p>

<div class="post-grid">
  {% assign meal_prep_posts = site.posts | where_exp: "post", "post.categories contains 'meal-prep'" %}
  {% if meal_prep_posts.size > 0 %}
    {% for post in meal_prep_posts %}
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
