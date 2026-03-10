---
layout: default
title: "HackMyVM Writeups"
permalink: /hmv/
---

<div class="page-content">
  <h1>HackMyVM Writeups</h1>
  <p class="page-description">Все мои врайтапы по машинам с HackMyVM</p>

  <div class="posts-list">
    {% assign hmv_posts = site.posts | where: "categories", "hmv" %}
    {% if hmv_posts.size > 0 %}
      {% for post in hmv_posts %}
        <article class="post-item">
          <h2>---
layout: default
title: "HackMyVM Writeups"
permalink: /hmv/
---

<!-- Простая навигация (как в Варианте 2) -->
<div class="site-navigation">
  <a href="/" class="nav-link">🏠 Главная</a>
  <span class="nav-separator">|</span>
  <a href="/hmv/" class="nav-link active">HMV</a>
  <a href="/htb/" class="nav-link">HTB</a>
  <a href="/thm/" class="nav-link">THM</a>
  <span class="nav-separator">|</span>
  <a href="/about/" class="nav-link">👤 Обо мне</a>
</div>

<!-- ХЛЕБНЫЕ КРОШКИ (НОВЫЕ) -->
<div class="breadcrumbs">
  <a href="/" class="breadcrumb-link">Главная</a>
  <span class="breadcrumb-separator">›</span>
  <span class="breadcrumb-current">HackMyVM</span>
</div>

<div class="page-content">
  <h1>HackMyVM Writeups</h1>
  <p class="page-description">Все мои врайтапы по машинам с HackMyVM</p>

  <div class="posts-list">
    {% assign hmv_posts = site.posts | where: "categories", "hmv" %}
    {% if hmv_posts.size > 0 %}
      {% for post in hmv_posts %}
        <article class="post-item">
          <h2>
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </h2>
          <div class="post-meta">
            <time datetime="{{ post.date | date_to_xmlschema }}">
              {{ post.date | date: "%d.%m.%Y" }}
            </time>
            
            <!-- БЛОК СО СЛОЖНОСТЬЮ -->
            {% if post.difficulty %}
              <span class="post-difficulty difficulty-{{ post.difficulty | downcase }}">
                Сложность: {{ post.difficulty }}
              </span>
            {% endif %}
            
            {% if post.tags.size > 0 %}
              <span class="post-tags">
                Теги: 
                {% for tag in post.tags %}
                  <span class="tag">{{ tag }}</span>
                  {% unless forloop.last %}, {% endunless %}
                {% endfor %}
              </span>
            {% endif %}
          </div>
          <div class="post-excerpt">
            {{ post.excerpt | strip_html | truncate: 300 }}
          </div>
          <a href="{{ post.url | relative_url }}" class="read-more">Читать далее →</a>
        </article>
      {% endfor %}
    {% else %}
      <p class="no-posts">Пока нет врайтапов в этой категории. Скоро появятся!</p>
    {% endif %}
  </div>
</div>

<style>
  /* Стили для навигации (как было) */
  .site-navigation {
    max-width: 800px;
    margin: 20px auto;
    padding: 15px 20px;
    background: #f8f9fa;
    border-radius: 8px;
    text-align: center;
  }
  
  .nav-link {
    color: #495057;
    text-decoration: none;
    padding: 5px 15px;
    margin: 0 5px;
    border-radius: 20px;
    transition: all 0.3s;
    display: inline-block;
  }
  
  .nav-link:hover {
    background: #007bff;
    color: white;
  }
  
  .nav-link.active {
    background: #007bff;
    color: white;
    font-weight: 500;
  }
  
  .nav-separator {
    color: #adb5bd;
    margin: 0 5px;
  }
  
  /* НОВЫЕ СТИЛИ ДЛЯ ХЛЕБНЫХ КРОШЕК */
  .breadcrumbs {
    max-width: 800px;
    margin: 10px auto 20px;
    padding: 10px 20px;
    background: #f1f3f5;
    border-radius: 6px;
    font-size: 0.95rem;
  }
  
  .breadcrumb-link {
    color: #007bff;
    text-decoration: none;
  }
  
  .breadcrumb-link:hover {
    text-decoration: underline;
  }
  
  .breadcrumb-separator {
    color: #868e96;
    margin: 0 8px;
    font-size: 1.2rem;
    font-weight: 300;
  }
  
  .breadcrumb-current {
    color: #495057;
    font-weight: 500;
  }
  
  /* Остальные стили (как были) */
  .page-content {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
  }
  
  .page-description {
    color: #666;
    margin-bottom: 30px;
  }
  
  .posts-list {
    display: flex;
    flex-direction: column;
    gap: 30px;
  }
  
  .post-item {
    border-bottom: 1px solid #eee;
    padding-bottom: 25px;
  }
  
  .post-item h2 {
    margin: 0 0 10px 0;
  }
  
  .post-item h2 a {
    color: #333;
    text-decoration: none;
  }
  
  .post-item h2 a:hover {
    color: #007bff;
  }
  
  .post-meta {
    font-size: 0.9em;
    color: #666;
    margin-bottom: 15px;
    display: flex;
    flex-wrap: wrap;
    gap: 10px 15px;
    align-items: center;
  }
  
  .post-difficulty {
    padding: 3px 10px;
    border-radius: 20px;
    font-weight: 600;
    font-size: 0.85em;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    display: inline-block;
  }
  
  .difficulty-easy {
    background-color: #4caf50;
    color: white;
  }
  
  .difficulty-medium {
    background-color: #ff9800;
    color: white;
  }
  
  .difficulty-hard {
    background-color: #f44336;
    color: white;
  }
  
  .difficulty-insane {
    background-color: #9c27b0;
    color: white;
  }
  
  .post-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 5px;
    align-items: center;
  }
  
  .tag {
    background: #f0f0f0;
    padding: 2px 8px;
    border-radius: 3px;
    font-size: 0.9em;
  }
  
  .post-excerpt {
    margin-bottom: 15px;
    line-height: 1.6;
  }
  
  .read-more {
    color: #007bff;
    text-decoration: none;
    font-weight: 500;
  }
  
  .read-more:hover {
    text-decoration: underline;
  }
  
  .no-posts {
    color: #999;
    font-style: italic;
    text-align: center;
    padding: 40px;
  }
  
  @media screen and (max-width: 600px) {
    .nav-link {
      display: block;
      margin: 5px 0;
    }
    .nav-separator {
      display: none;
    }
    
    /* Адаптация хлебных крошек для мобильных */
    .breadcrumbs {
      font-size: 0.85rem;
      padding: 8px 15px;
    }
  }
</style>
