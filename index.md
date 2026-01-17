---
layout: default  # 保持无冗余布局，避免标题重复
title: ZingTo Image Scoring - Image Rating Tool
---

<!-- 全局样式：统一排版，保持上下文流畅 -->
<!-- 唯一标题，保持页面顶部简洁 -->
  ZingTo Image Scoring - Image Rating Tool<!-- 最新博文模块（保留现有效果，优化间距让上下文更流畅） -->
  📝 最新博文
  {% if site.posts.size > 0 %}
    {% for post in site.posts limit: 10 %}
      {{ post.title }}{{ post.excerpt | strip_html | truncate: 180 }}
    {% endfor %}
  {% else %}
    暂无博文，快来发布你的第一篇内容吧！
  {% endif %}

  <!-- 软件介绍模块（核心修复：改用静态文件读取 README.md） -->
  📖 软件介绍
  {% assign readme_file = site.static_files | where: "name", "README.md" | first %}
  {% if readme_file %}
    <!-- 读取根目录 README.md 内容并渲染，保持格式一致 -->
    {% capture readme_content %}{% include_relative README.md %}{% endcapture %}
    {{ readme_content | markdownify }}
  {% else %}
    
      ⚠️ 未找到 README.md 文件，请确认：
      1. 文件位于根目录（与 index.md 同级）；
      2. 文件名严格为 README.md（区分大小写，不可为 readme.md 等变体）；
      3. 文件已成功提交至 GitHub 仓库。
    
  {% endif %}
