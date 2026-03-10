---
layout: default
title: "HackTheBox Writeups"
permalink: /htb/
---

<div class="breadcrumbs" style="margin-bottom: 2rem;">
  <a href="/">Главная</a> / <span>HackTheBox</span>
</div>

<h1>HackTheBox Writeups</h1>
<p style="color: var(--muted-text); margin-bottom: 2rem;">Все мои врайтапы по машинам с HackTheBox</p>

<!-- Фильтр по сложности -->
<div class="filter-section" style="margin-bottom: 2rem;">
  <span style="margin-right: 1rem; color: var(--text);">Сложность:</span>
  <div style="display: inline-flex; gap: 0.5rem; flex-wrap: wrap;">
    <button class="filter-btn active" data-filter="all">Все</button>
    <button class="filter-btn" data-filter="easy">Easy</button>
    <button class="filter-btn" data-filter="medium">Medium</button>
    <button class="filter-btn" data-filter="hard">Hard</button>
    <button class="filter-btn" data-filter="insane">Insane</button>
  </div>
</div>

<div class="posts-list" id="posts-list">
  {% assign htb_posts = site.posts | where: "categories", "htb" %}
  {% if htb_posts.size > 0 %}
    {% for post in htb_posts %}
      {% assign difficulty = post.difficulty | downcase | default: "easy" %}
      <div class="post-item" data-difficulty="{{ difficulty }}" style="margin-bottom: 2rem; padding-bottom: 1rem; border-bottom: 1px solid var(--border);">
        <h2 style="margin-bottom: 0.25rem;">
          <a href="{{ post.url | relative_url }}" style="color: var(--text); text-decoration: none;">{{ post.title | remove: " - HTB" }}</a>
        </h2>
        
        <div style="display: flex; gap: 1rem; align-items: center; margin-bottom: 0.5rem; font-size: 0.9rem; color: var(--muted-text);">
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d.%m.%Y" }}</time>
          <span class="difficulty-badge difficulty-{{ difficulty }}" style="padding: 0.15rem 0.6rem; border-radius: 12px; font-size: 0.75rem; font-weight: 500; text-transform: uppercase;">
            {{ post.difficulty | default: "Easy" }}
          </span>
        </div>
        
        <p style="color: var(--text); margin-bottom: 0.5rem;">
          {% if post.excerpt %}
            {{ post.excerpt | strip_html | truncate: 160 }}
          {% endif %}
        </p>
        
        <a href="{{ post.url | relative_url }}" style="color: var(--accent); text-decoration: none; font-size: 0.9rem;">Читать далее →</a>
      </div>
    {% endfor %}
  {% else %}
    <p style="color: var(--muted-text); text-align: center; padding: 2rem;">Пока нет врайтапов в этой категории. Скоро появятся!</p>
  {% endif %}
</div>


<script>
document.addEventListener('DOMContentLoaded', function() {
  const filterButtons = document.querySelectorAll('.filter-btn');
  const posts = document.querySelectorAll('.post-item');
  
  filterButtons.forEach(button => {
    button.addEventListener('click', function() {
      filterButtons.forEach(btn => btn.classList.remove('active'));
      this.classList.add('active');
      
      const filter = this.dataset.filter;
      
      posts.forEach(post => {
        if (filter === 'all' || post.dataset.difficulty === filter) {
          post.style.display = 'block';
        } else {
          post.style.display = 'none';
        }
      });
    });
  });
});
</script>


<style>
.filter-btn {
  background: transparent;
  border: 1px solid var(--border);
  color: var(--text);
  padding: 0.3rem 1rem;
  border-radius: 20px;
  cursor: pointer;
  font-size: 0.9rem;
  transition: all 0.2s;
}

.filter-btn:hover {
  border-color: var(--accent);
  color: var(--accent);
}

.filter-btn.active {
  background: var(--accent);
  border-color: var(--accent);
  color: var(--bg);
}

.difficulty-badge {
  display: inline-block;
}

.difficulty-easy {
  background: rgba(72, 187, 120, 0.15);
  color: #68d391;
  border: 1px solid rgba(72, 187, 120, 0.3);
}

.difficulty-medium {
  background: rgba(237, 137, 54, 0.15);
  color: #f6ad55;
  border: 1px solid rgba(237, 137, 54, 0.3);
}

.difficulty-hard {
  background: rgba(245, 101, 101, 0.15);
  color: #fc8181;
  border: 1px solid rgba(245, 101, 101, 0.3);
}

.difficulty-insane {
  background: rgba(159, 122, 234, 0.15);
  color: #b794f4;
  border: 1px solid rgba(159, 122, 234, 0.3);
}

.breadcrumbs {
  color: var(--muted-text);
  font-size: 0.9rem;
}

.breadcrumbs a {
  color: var(--accent);
  text-decoration: none;
}

.breadcrumbs a:hover {
  text-decoration: underline;
}

:root {
  --accent: #9f7aea;
}

[data-theme="dark"] {
  --accent: #b794f4;
}
</style>
