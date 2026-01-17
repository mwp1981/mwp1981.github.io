---
layout: home  # 必须用 --- 包裹YAML头，否则布局和变量失效
title: ZingTo Image Scoring - Image Rating Tool
---

## 📝 最新博文
{: .page-heading }

{% for post in site.posts limit: 10 %}
  {{ post.title }}{{ post.excerpt | strip_html | truncate: 150 }}
{% endfor %}

## 📖 软件介绍
{: .page-heading }

{% comment %} 自动读取根目录 README.md 并渲染 {% endcomment %}
{% for file in site.pages %}
  {% if file.name == 'README.md' %}
    {{ file.content | markdownify }}
  {% endif %}
{% endfor %}
