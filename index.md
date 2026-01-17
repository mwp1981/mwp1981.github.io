---
layout: default  # 改用default布局，避免home布局自动渲染冗余内容
title: ZingTo Image Scoring - Image Rating Tool  # 仅保留一次标题
---

<!-- 全局样式：隐藏主题默认冗余元素，优化排版 -->
<!-- 仅显示一次标题 -->
  ZingTo Image Scoring - Image Rating Tool

  <!-- 最新博文（确保Liquid语法生效） -->
  📝 最新博文
  {% if site.posts.size > 0 %}
    {% for post in site.posts limit: 10 %}
      {{ post.title }}{{ post.excerpt | strip_html | truncate: 150 }}
    {% endfor %}
  {% else %}
    暂无博文，快来发布你的第一篇内容吧！
  {% endif %}

  <!-- 软件介绍（读取README.md，修复格式错乱） -->
  📖 软件介绍
  {% assign readme = site.pages | where: "name", "README.md" | first %}
  {% if readme %}
    {{ readme.content | markdownify }}
  {% else %}
    未找到软件介绍内容，请检查根目录 README.md 文件是否存在。
  {% endif %}
