---
layout: default
title: ZingTo Image Scoring - Image Rating Tool
---

<!-- 基础样式：保证链接可点击、排版工整 -->
<style>
  /* 隐藏主题冗余元素 */
  .site-title, .site-description, .page-footer .contact-list { display: none !important; }
  /* 正文容器样式 */
  .page-content {
    max-width: 900px;
    margin: 0 auto;
    padding: 2rem 1rem;
    line-height: 1.8;
  }
  /* 博文标题链接样式（关键：让链接显眼且可点击） */
  .post-title-link {
    color: #0366d6; /* 蓝色链接色，符合网页习惯 */
    text-decoration: none;
    font-size: 1.2rem;
    font-weight: 600;
  }
  .post-title-link:hover {
    text-decoration: underline; /* 鼠标悬浮加下划线，提示可点击 */
  }
  /* 博文摘要样式 */
  .post-excerpt {
    color: #333;
    margin: 0.5rem 0 1.5rem;
    padding-bottom: 1rem;
    border-bottom: 1px solid #eee;
  }
  /* 模块标题样式 */
  .module-heading {
    font-size: 1.4rem;
    margin: 2rem 0 1rem;
    color: #24292e;
    border-bottom: 1px solid #eee;
    padding-bottom: 0.5rem;
  }
</style>

<div class="page-content">
  <!-- 页面主标题 -->
  <h1 style="text-align: center; margin: 2rem 0;">ZingTo Image Scoring - Image Rating Tool</h1>

  <!-- 最新博文模块（核心：给标题加超链接） -->
  <h2 class="module-heading">📝 最新博文</h2>
  {% if site.posts.size > 0 %}
    {% for post in site.posts limit: 10 %}
      <!-- 博文标题超链接：href指向博文详情页（Jekyll 标准路径） -->
      <a href="{{ site.baseurl }}{{ post.url }}" class="post-title-link">{{ post.title }}</a>
      <!-- 博文摘要 -->
      <div class="post-excerpt">
        {{ post.excerpt | strip_html | truncate: 180 }}
      </div>
    {% endfor %}
  {% else %}
    <p style="color: #6a737d;">暂无博文，快来发布你的第一篇内容吧！</p>
  {% endif %}

  <!-- 软件介绍模块 -->
  <h2 class="module-heading">📖 软件介绍</h2>
  {% assign readme_file = site.static_files | where: "name", "README.md" | first %}
  {% if readme_file %}
    {% capture readme_content %}{% include_relative README.md %}{% endcapture %}
    {{ readme_content | markdownify }}
  {% else %}
    <div style="padding: 1rem; border: 1px solid #ffdce0; background: #fff8f9; color: #dc3545; border-radius: 4px;">
      ⚠️ 未找到 README.md 文件，请确认：
      1. 文件位于根目录（与 index.md 同级）；
      2. 文件名严格为 README.md（区分大小写）；
      3. 文件已成功提交至 GitHub 仓库。
    </div>
  {% endif %}
</div>
