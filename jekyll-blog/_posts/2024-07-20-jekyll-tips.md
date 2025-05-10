---
layout: post
title: "Jekyll魔导书"
categories: tech
image: /assets/images/jekyll-logo.png
---

## 🧙♀️ 三大实用技巧
```liquid
{% raw %}{% assign sorted_posts = site.posts | sort: 'date' | reverse %}
{% for post in sorted_posts limit:3 %}
  <div class="post-card {{ post.categories }}">
    <h3>{{ post.title }}</h3>
    <img src="{{ post.image }}" alt="缩略图">
  </div>
{% endfor %}{% endraw %}