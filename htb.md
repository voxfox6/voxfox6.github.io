---
layout: default
title: "HackTheBox Writeups"
permalink: /htb/
---

<div class="page-content">
  <h1>HackTheBox Writeups</h1>
  <p class="page-description">Все мои врайтапы по машинам с HackTheBox</p>

  <div class="posts-list">
    {% assign htb_posts = site.posts | where: "categories", "htb" %}
    {% if htb_posts.size > 0 %}
      {% for post in htb_posts %}
        <article class="post-item">
          <h2>
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </h2>
          <div class="post-meta">
            <time datetime="{{ post.date | date_to_xmlschema }}">
              {{ post.date | date: "%d.%m.%Y" }}
            </time>
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

<!-- чувак ты думал здесь чтото будет? -->
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
  }
  
  .post-tags {
    margin-left: 10px;
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
