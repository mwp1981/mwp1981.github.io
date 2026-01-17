---
layout: default
title: ZingTo Image Scoring - Image Rating Tool
---

<style>
  .site-title, .site-description, .page-footer .contact-list { display: none !important; }
  .page-content {
    max-width: 900px;
    margin: 0 auto;
    padding: 2rem 1rem;
    line-height: 1.8;
  }
  .post-title-link {
    color: #0366d6;
    text-decoration: none;
    font-size: 1.2rem;
    font-weight: 600;
  }
  .post-title-link:hover {
    text-decoration: underline;
  }
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

<div class="page-content">
  <h1 style="text-align: center; margin: 2rem 0;">ZingTo Image Scoring - Image Rating Tool</h1>

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
