---
layout: default
title: ZingTo Image Scoring - Image Rating Tool
---

<!-- 核心样式：实现标题+Logo同行、尺寸匹配、排版工整 -->
<style>
  /* 隐藏主题冗余元素 */
  .site-title, .site-description, .page-footer .contact-list { display: none !important; }
  
  /* 标题+Logo容器：flex布局实现同行，垂直居中 */
  .title-logo-container {
    display: flex;
    justify-content: space-between; /* 文字左，Logo右 */
    align-items: center; /* 垂直居中，确保Logo和文字对齐 */
    max-width: 900px;
    margin: 2rem auto;
    padding: 0 1rem;
  }

  /* 标题文字样式：控制字号，匹配Logo高度 */
  .main-title {
    font-size: 1.8rem;
    color: #24292e;
    margin: 0; /* 清除默认间距 */
  }

  /* Logo样式：高度和文字行高一致，宽度自动（避免变形） */
  .title-logo {
    height: 1.8rem; /* 和标题字号一致，实现尺寸匹配 */
    width: auto;
    margin-left: 1rem; /* 与文字保留小间距 */
  }

  /* 页面主容器样式 */
  .page-content {
    max-width: 900px;
    margin: 0 auto;
    padding: 0 1rem 2rem;
    line-height: 1.8;
  }

  /* 模块标题样式 */
  .module-heading {
    font-size: 1.4rem;
    margin: 2rem 0 1rem;
    color: #24292e;
    border-bottom: 1px solid #eee;
    padding-bottom: 0.5rem;
  }

  /* 博文摘要样式 */
  .post-excerpt {
    color: #333;
    margin: 0.5rem 0 1.5rem;
    padding-bottom: 1rem;
    border-bottom: 1px solid #eee;
  }
</style>

<!-- 标题+Logo同行容器 -->
<div class="title-logo-container">
  <h1 class="main-title">ZingTo Image Scoring - Image Rating Tool</h1>
  <!-- Logo图片：行末显示，尺寸匹配文字（需确保图片路径正确） -->
  <img src="{{ site.baseurl }}/assets/images/logo.png" alt="ZingTo Logo" class="title-logo">
</div>

<!-- 页面主内容容器 -->
<div class="page-content">
  <!-- 最新博文模块 -->
  <h2 class="module-heading">📝 最新博文</h2>
  {% if site.posts.size > 0 %}
    {% for post in site.posts limit: 10 %}
      <div class="post-excerpt">
        <strong>{{ post.title }}</strong>
        <p>{{ post.excerpt | strip_html | truncate: 180 }}</p>
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
