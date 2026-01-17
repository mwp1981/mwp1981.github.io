---
layout: default
title: ZingTo Image Scoring - Image Rating Tool
---

<!-- 整合所有样式：Logo + 基础排版 + 博文超链接 -->
<style>
  /* 隐藏主题冗余元素 */
  .site-title, .site-description, .page-footer .contact-list { display: none !important; }
  
  /* Logo样式：居中显示，控制大小 */
  .site-logo {
    display: block;
    margin: 0 auto 2rem; /* 居中，与标题间距2rem */
    width: 180px; /* Logo宽度，可自行调整（如200px） */
    height: auto; /* 防止图片变形 */
  }

  /* 页面主容器样式 */
  .page-content {
    max-width: 900px;
    margin: 0 auto;
    padding: 2rem 1rem;
    line-height: 1.8;
  }

  /* 博文标题超链接样式（可点击、悬浮下划线） */
  .post-title-link {
    color: #0366d6;
    text-decoration: none;
    font-size: 1.2rem;
    font-weight: 600;
  }
  .post-title-link:hover {
    text-decoration: underline;
  }

  /* 博文摘要样式（分隔线+间距） */
  .post-excerpt {
    color: #333;
    margin: 0.5rem 0 1.5rem;
    padding-bottom: 1rem;
    border-bottom: 1px solid #eee;
  }

  /* 模块标题样式（下划线+间距） */
  .module-heading {
    font-size: 1.4rem;
    margin: 2rem 0 1rem;
    color: #24292e;
    border-bottom: 1px solid #eee;
    padding-bottom: 0.5rem;
  }
</style>

<div class="page-content">
  <!-- 1. Logo（需先上传图片到仓库，路径对应下方src） -->
  <img src="{{ site.baseurl }}/assets/images/kutu.png" alt="ZingTo Image Scoring Logo" class="site-logo">

  <!-- 2. 页面主标题 -->
  <h1 style="text-align: center; margin: 1rem 0 2rem;">ZingTo Image Scoring - Image Rating Tool</h1>

  <!-- 3. 最新博文模块（带超链接） -->
  <h2 class="module-heading">📝 Latest Blog Posts</h2>
  {% if site.posts.size > 0 %}
    {% for post in site.posts limit: 10 %}
      <a href="{{ site.baseurl }}{{ post.url }}" class="post-title-link">{{ post.title }}</a>
      <div class="post-excerpt">
        {{ post.excerpt | strip_html | truncate: 180 }}
      </div>
    {% endfor %}
  {% else %}
    <p style="color: #6a737d;">No blog posts yet. Publish your first post now!</p>
  {% endif %}

  <!-- 4. 软件介绍模块（读取README.md） -->
  <h2 class="module-heading">📖 Software Introduction</h2>
  {% assign readme_file = site.static_files | where: "name", "README.md" | first %}
  {% if readme_file %}
    {% capture readme_content %}{% include_relative README.md %}{% endcapture %}
    {{ readme_content | markdownify }}
  {% else %}
    <div style="padding: 1rem; border: 1px solid #ffdce0; background: #fff8f9; color: #dc3545; border-radius: 4px;">
      ⚠️ README.md file not found. Please confirm:
      1. The file is in the root directory (same level as index.md);
      2. The file name is strictly "README.md" (case-sensitive);
      3. The file has been successfully committed to the GitHub repository.
    </div>
  {% endif %}
</div>
