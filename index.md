---
layout: default
title: ZingTo Image Scoring - Image Rating Tool | Professional Image Scoring Software
description: ZingTo Image Scoring is a local-first AI-powered desktop image rating tool with frame capture and photo-to-video features. Learn tutorials and updates here.
keywords: ZingTo Image Scoring, Image Rating Tool, AI Image Scoring, Desktop Image Scoring Software, Frame Capture Tool
---

<!-- SEO关键：语义化标签 + 结构化数据 + 基础样式 -->
<html lang="en"> <!-- 明确语言，帮助Google识别 -->
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- SEO核心Meta标签：Google优先抓取 -->
  <title>{{ page.title }}</title>
  <meta name="description" content="{{ page.description }}">
  <meta name="keywords" content="{{ page.keywords }}">
  <!-- 规范链接：避免重复内容（GitHub Pages多域名风险） -->
  <link rel="canonical" href="https://mwp1981.github.io/">
  <!-- 结构化数据：帮助Google理解页面类型（博客+软件介绍） -->
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "WebSite",
    "name": "ZingTo Image Scoring",
    "url": "https://mwp1981.github.io/",
    "description": "{{ page.description }}",
    "publisher": {
      "@type": "Organization",
      "name": "ZingTo Image Scoring",
      "logo": {
        "@type": "ImageObject",
        "url": "https://mwp1981.github.io/assets/images/kutu.png"
      }
    }
  }
  </script>
  <!-- 基础样式：保证页面可读，SEO也看重用户体验 -->
  <style>
    body { font-family: Arial, sans-serif; line-height: 1.8; color: #333; max-width: 900px; margin: 0 auto; padding: 1rem; }
    h1, h2 { color: #24292e; border-bottom: 1px solid #eee; padding-bottom: 0.5rem; }
    a { color: #0366d6; text-decoration: none; }
    a:hover { text-decoration: underline; }
    .post-item { margin: 1.5rem 0; padding-bottom: 1rem; border-bottom: 1px solid #eee; }
    .logo { height: 3.6rem; width: auto; margin-left: 1rem; }
    .title-container { display: flex; justify-content: space-between; align-items: center; margin: 2rem 0; }
  </style>
</head>
<body>
  <!-- 语义化头部：帮助Google识别核心标题+Logo -->
  <header class="title-container">
    <h1>ZingTo Image Scoring - Image Rating Tool</h1>
    <!-- Logo添加alt属性（SEO关键：图片可被Google索引） -->
    <img src="https://mwp1981.github.io/assets/images/kutu.png" alt="ZingTo Image Scoring Logo" class="logo">
  </header>

  <!-- 主内容区：语义化标签，Google优先抓取 -->
  <main>
    <!-- 最新博文模块（恢复超链接，内部链接提升SEO） -->
    <section>
      <h2>📝 Latest Blog Posts</h2>
      {% if site.posts.size > 0 %}
        {% for post in site.posts limit: 10 %}
          <div class="post-item">
            <!-- 博文标题超链接：内部链接+关键词锚文本 -->
            <a href="{{ site.baseurl }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
            <p>{{ post.excerpt | strip_html | truncate: 180 }}</p>
          </div>
        {% endfor %}
      {% else %}
        <p>No blog posts yet. Stay tuned for tutorials and updates on ZingTo Image Scoring!</p>
      {% endif %}
    </section>

    <!-- 软件介绍模块（核心内容，植入关键词） -->
    <section>
      <h2>📖 Software Introduction</h2>
      {% assign readme_file = site.static_files | where: "name", "README.md" | first %}
      {% if readme_file %}
        {% capture readme_content %}{% include_relative README.md %}{% endcapture %}
        {{ readme_content | markdownify }}
      {% else %}
        <div style="padding: 1rem; border: 1px solid #ffdce0; background: #fff8f9; color: #dc3545; border-radius: 4px;">
          ⚠️ README.md file not found. Please confirm:
          1. File is in root directory (same level as index.md);
          2. File name is strictly "README.md" (case-sensitive);
          3. File is committed to GitHub repository.
        </div>
      {% endif %}
    </section>
  </main>

  <!-- 页脚：补充联系/版权，提升信任度 -->
  <footer style="margin-top: 3rem; padding-top: 1rem; border-top: 1px solid #eee; text-align: center;">
    <p>© 2026 ZingTo Image Scoring - All Rights Reserved</p>
    <p><a href="https://mwp1981.github.io/">Home</a></p>
  </footer>
</body>
</html>
