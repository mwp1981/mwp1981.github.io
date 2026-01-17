---
layout: default
title: ZingTo Image Scoring - Image Rating Tool
---

ZingTo Image Scoring - Image Rating Tool<!-- 最新博文模块 -->
  📝 最新博文
  {% if site.posts.size > 0 %}
    {% for post in site.posts limit: 10 %}
     {{ post.title }}{{ post.excerpt | strip_html | truncate: 180 }}
    {% endfor %}
  {% else %}
    暂无博文，快来发布你的第一篇内容吧！
  {% endif %}

  <!-- 软件介绍模块（移除无效注释，优化内容过滤） -->
  📖 软件介绍
  {% assign readme_file = site.static_files | where: "name", "README.md" | first %}
  {% if readme_file %}
    {% capture readme_content %}{% include_relative README.md %}{% endcapture %}
    {{ readme_content | markdownify }}
  {% else %}
    
      ⚠️ 未找到 README.md 文件，请确认：
      1. 文件位于根目录（与 index.md 同级）；
      2. 文件名严格为 README.md（区分大小写）；
      3. 文件已成功提交至 GitHub 仓库。

  {% endif %}
