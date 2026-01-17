---
layout: default
title: ZingTo Image Scoring - Image Rating Tool
---

<!-- 完整样式：Logo同行 + 博文超链接 + 整体排版 -->
<style>
  /* 隐藏主题冗余元素 */
  .site-title, .site-description, .page-footer .contact-list { display: none !important; }
  
  /* 标题+Logo同行容器：核心实现同行、行末显示 */
  .title-logo-container {
    display: flex;
    justify-content: space-between; /* 文字左，Logo右（行末） */
    align-items: center; /* 垂直居中，尺寸匹配 */
    max-width: 900px;
    margin: 2rem auto;
    padding: 0 1rem;
  }
  .main-title {
    font-size: 1.8rem;
    color: #24292e;
    margin: 0;
  }
  /* Logo尺寸匹配文字 */
  .title-logo {
    height: 1.8rem; /* 和标题字号一致 */
    width: auto;
    margin-left: 1rem;
  }

  /* 页面主容器 */
  .page-content {
    max-width: 900px;
    margin: 0 auto;
    padding: 0 1rem 2rem;
    line-height: 1.8;
  }

  /* 博文超链接样式（核心：恢复可点击+悬浮下划线） */
  .post-title-link {
    color: #0366d6; /* 蓝色链接色 */
    text-decoration: none;
    font-size: 1.2rem;
    font-weight: 600;
  }
  .post-title-link:hover {
    text-decoration: underline; /* 悬浮下划线，提示可点击 */
  }

  /* 博文摘要+模块标题样式 */
  .post-excerpt {
    color: #333;
    margin: 0.5rem 0 1.5rem;
    padding-bottom: 1rem;
    border-bottom: 1px solid #eee;
  }
  .module-heading {
    font-size: 1.4rem;
    margin: 2rem 0 1rem;
    color: #24292e;
    border-bottom: 1px solid #eee;
    padding-bottom: 0.5rem;
  }
</style>

<!-- 标题+Logo同行区域（保留行末Logo） -->
<div class="title-logo-container">
  <h1 class="main-title">ZingTo Image Scoring - Image Rating Tool</h1>
  <img src="{{ site.baseurl }}/assets/images/kutu.png" alt="ZingTo Logo" class="title-logo">
</div>

<!-- 主内容容器 -->
<div class="page-content">
  <!-- 最新博文模块（恢复超链接核心代码） -->
  <h2 class="module-heading">📝 最新博文</h2>
  {% if site.posts.size > 0 %}
    {% for post in site.posts limit: 10 %}
      <!-- 恢复超链接：点击标题跳转到博文详情页 -->
      <a href="{{ site.baseurl }}{{ post.url }}" class="post-title-link">{{ post.title }}</a>
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
