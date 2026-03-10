---
layout: default
title: "HackMyVM Writeups"
permalink: /hmv/
---

<!-- Простая навигация -->
<div style="max-width: 800px; margin: 20px auto; padding: 15px 20px; background: #f8f9fa; border-radius: 8px; text-align: center;">
  <a href="/" style="color: #495057; text-decoration: none; padding: 5px 15px; margin: 0 5px; border-radius: 20px; display: inline-block;">🏠 Главная</a>
  <span style="color: #adb5bd; margin: 0 5px;">|</span>
  <a href="/hmv/" style="color: white; text-decoration: none; padding: 5px 15px; margin: 0 5px; border-radius: 20px; display: inline-block; background: #007bff; font-weight: 500;">HMV</a>
  <a href="/htb/" style="color: #495057; text-decoration: none; padding: 5px 15px; margin: 0 5px; border-radius: 20px; display: inline-block;">HTB</a>
  <a href="/thm/" style="color: #495057; text-decoration: none; padding: 5px 15px; margin: 0 5px; border-radius: 20px; display: inline-block;">THM</a>
  <span style="color: #adb5bd; margin: 0 5px;">|</span>
  <a href="/about/" style="color: #495057; text-decoration: none; padding: 5px 15px; margin: 0 5px; border-radius: 20px; display: inline-block;">👤 Обо мне</a>
</div>

<!-- Хлебные крошки (упрощенные) -->
<div style="max-width: 800px; margin: 10px auto 20px; padding: 8px 20px; background: #f1f3f5; border-radius: 6px; font-size: 0.95rem;">
  <a href="/" style="color: #007bff; text-decoration: none;">Главная</a>
  <span style="color: #868e96; margin: 0 8px; font-size: 1.2rem;">›</span>
  <span style="color: #495057; font-weight: 500;">HackMyVM</span>
</div>

<div class="page-content" style="max-width: 800px; margin: 0 auto; padding: 20px;">
  <h1>HackMyVM Writeups</h1>
  <p style="color: #666; margin-bottom: 30px;">Все мои врайтапы по машинам с HackMyVM</p>

  <div style="display: flex; flex-direction: column; gap: 30px;">
    {% assign hmv_posts = site.posts | where: "categories", "hmv" %}
    {% if hmv_posts.size > 0 %}
      {% for post in hmv_posts %}
        <article style="border-bottom: 1px solid #eee; padding-bottom: 25px;">
          <h2 style="margin: 0 0 10px 0;">
            <a href="{{ post.url | relative_url }}" style="color: #333; text-decoration: none;">{{ post.title }}</a>
          </h2>
          
          <div style="font-size: 0.9em; color: #666; margin-bottom: 15px; display: flex; flex-wrap: wrap; gap: 10px 15px; align-items: center;">
            <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d.%m.%Y" }}</time>
            
            {% if post.difficulty %}
              {% assign diff = post.difficulty | downcase %}
              {% if diff == "easy" %}
                <span style="padding: 3px 10px; border-radius: 20px; font-weight: 600; font-size: 0.85em; text-transform: uppercase; background-color: #4caf50; color: white; display: inline-block;">Сложность: Easy</span>
              {% elsif diff == "medium" %}
                <span style="padding: 3px 10px; border-radius: 20px; font-weight: 600; font-size: 0.85em; text-transform: uppercase; background-color: #ff9800; color: white; display: inline-block;">Сложность: Medium</span>
              {% elsif diff == "hard" %}
                <span style="padding: 3px 10px; border-radius: 20px; font-weight: 600; font-size: 0.85em; text-transform: uppercase; background-color: #f44336; color: white; display: inline-block;">Сложность: Hard</span>
              {% elsif diff == "insane" %}
                <span style="padding: 3px 10px; border-radius: 20px; font-weight: 600; font-size: 0.85em; text-transform: uppercase; background-color: #9c27b0; color: white; display: inline-block;">Сложность: Insane</span>
              {% endif %}
            {% endif %}
            
            {% if post.tags.size > 0 %}
              <span style="display: flex; flex-wrap: wrap; gap: 5px; align-items: center;">
                Теги: 
                {% for tag in post.tags %}
                  <span style="background: #f0f0f0; padding: 2px 8px; border-radius: 3px; font-size: 0.9em;">{{ tag }}</span>
                  {% unless forloop.last %}, {% endunless %}
                {% endfor %}
              </span>
            {% endif %}
          </div>
          
          <div style="margin-bottom: 15px; line-height: 1.6;">
            {{ post.excerpt | strip_html | truncate: 300 }}
          </div>
          
          <a href="{{ post.url | relative_url }}" style="color: #007bff; text-decoration: none; font-weight: 500;">Читать далее →</a>
        </article>
      {% endfor %}
    {% else %}
      <p style="color: #999; font-style: italic; text-align: center; padding: 40px;">Пока нет врайтапов в этой категории. Скоро появятся!</p>
    {% endif %}
  </div>
</div>
