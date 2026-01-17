---
layout: home  # 沿用 minima 主题的首页布局，保持样式统一
title: ZingTo Image Scoring - Image Rating Tool
---

## 📝 最新博文
{: .page-heading }

{% for post in site.posts limit: 10 %}  # 读取所有博文，限制最多显示10篇
  {{ post.title }}{{ post.excerpt | strip_html | truncate: 150 }}
{% endfor %}

## 📖 软件介绍
{: .page-heading }

{% comment %} 自动读取 README.md 内容并渲染 {% endcomment %}
{% for file in site.pages %}
  {% if file.name == 'README.md' %}
    {{ file.content | markdownify }}
  {% endif %}
{% endfor %}
