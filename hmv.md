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
          <h2>
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </h2>
          <div class="post-meta">
            <time datetime="{{ post.date | date_to_xmlschema }}">
              {{ post.date | date: "%d.%m.%Y" }}
            </time>
            
            <!-- блок со сложностью -->
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
    gap: 10px 15px;  /* отступ между элементами */
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
</style>
