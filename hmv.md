---
layout: default
title: "HackMyVM Writeups"
permalink: /hmv/
---

<!-- Навигация -->
<nav class="site-nav">
  <div class="nav-container">
    <a href="/" class="nav-logo">VoxFox Blog</a>
    <div class="nav-links">
      <a href="/" class="nav-link">Главная</a>
      <a href="/hmv/" class="nav-link active">HMV</a>
      <a href="/htb/" class="nav-link">HTB</a>
      <a href="/thm/" class="nav-link">THM</a>
      <a href="/about/" class="nav-link">Обо мне</a>
    </div>
  </div>
</nav>

<!-- Хлебные крошки -->
<div class="breadcrumbs">
  <div class="breadcrumbs-container">
    <a href="/" class="breadcrumb-link">Главная</a>
    <span class="breadcrumb-separator">/</span>
    <span class="breadcrumb-current">HackMyVM</span>
  </div>
</div>

<main class="page-content">
  <div class="content-container">
    <header class="page-header">
      <h1 class="page-title">HackMyVM Writeups</h1>
      <p class="page-description">Все мои врайтапы по машинам с HackMyVM</p>
    </header>

    <!-- Фильтр по сложности -->
    <div class="filter-section">
      <span class="filter-label">Фильтр по сложности:</span>
      <div class="filter-buttons">
        <button class="filter-btn active" data-filter="all">Все</button>
        <button class="filter-btn" data-filter="easy">Easy</button>
        <button class="filter-btn" data-filter="medium">Medium</button>
        <button class="filter-btn" data-filter="hard">Hard</button>
        <button class="filter-btn" data-filter="insane">Insane</button>
      </div>
    </div>

    <!-- Список постов -->
    <div class="posts-grid" id="posts-grid">
      {% assign hmv_posts = site.posts | where: "categories", "hmv" %}
      {% if hmv_posts.size > 0 %}
        {% for post in hmv_posts %}
          {% assign difficulty = post.difficulty | downcase | default: "easy" %}
          <article class="post-card" data-difficulty="{{ difficulty }}">
            <div class="post-card-content">
              <h2 class="post-title">
                <a href="{{ post.url | relative_url }}">{{ post.title | remove: " - HMV" }}</a>
              </h2>
              
              <div class="post-meta">
                <time class="post-date" datetime="{{ post.date | date_to_xmlschema }}">
                  {{ post.date | date: "%d.%m.%Y" }}
                </time>
                
                <span class="difficulty-badge difficulty-{{ difficulty }}">
                  {{ post.difficulty | default: "Easy" }}
                </span>
              </div>
              
              <div class="post-excerpt">
                {% if post.excerpt %}
                  {{ post.excerpt | strip_html | truncate: 120 }}
                {% else %}
                  Writeup для машины {{ post.title | remove: " - HMV" }}
                {% endif %}
              </div>
              
              <a href="{{ post.url | relative_url }}" class="read-more-link">
                Читать далее
                <svg class="arrow-icon" width="16" height="16" viewBox="0 0 16 16" fill="none">
                  <path d="M6 12L10 8L6 4" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
              </a>
            </div>
          </article>
        {% endfor %}
      {% else %}
        <div class="no-posts">
          <p>Пока нет врайтапов в этой категории. Скоро появятся!</p>
        </div>
      {% endif %}
    </div>
  </div>
</main>

<!-- Скрипт для фильтрации -->
<script>
document.addEventListener('DOMContentLoaded', function() {
  const filterButtons = document.querySelectorAll('.filter-btn');
  const posts = document.querySelectorAll('.post-card');
  
  filterButtons.forEach(button => {
    button.addEventListener('click', function() {
      // Обновляем активный класс у кнопок
      filterButtons.forEach(btn => btn.classList.remove('active'));
      this.classList.add('active');
      
      const filterValue = this.dataset.filter;
      
      // Фильтруем посты
      posts.forEach(post => {
        if (filterValue === 'all') {
          post.style.display = 'block';
        } else {
          const postDifficulty = post.dataset.difficulty;
          if (postDifficulty === filterValue) {
            post.style.display = 'block';
          } else {
            post.style.display = 'none';
          }
        }
      });
      
      // Показываем сообщение, если нет постов
      const visiblePosts = Array.from(posts).filter(p => p.style.display !== 'none');
      const noPostsMessage = document.querySelector('.no-posts');
      
      if (visiblePosts.length === 0) {
        if (!noPostsMessage) {
          const message = document.createElement('div');
          message.className = 'no-posts';
          message.innerHTML = '<p>Нет врайтапов с такой сложностью</p>';
          document.getElementById('posts-grid').appendChild(message);
        }
      } else {
        const existingMessage = document.querySelector('.no-posts:not(.no-posts-permanent)');
        if (existingMessage) existingMessage.remove();
      }
    });
  });
});
</script>

<style>
/* Основные переменные */
:root {
  --bg-primary: #ffffff;
  --bg-secondary: #f8f9fa;
  --text-primary: #2c3e50;
  --text-secondary: #6c757d;
  --accent-color: #3498db;
  --accent-hover: #2980b9;
  --border-color: #e9ecef;
  --card-shadow: 0 2px 4px rgba(0,0,0,0.02);
  --card-shadow-hover: 0 8px 16px rgba(0,0,0,0.05);
}

/* Навигация */
.site-nav {
  background: var(--bg-primary);
  border-bottom: 1px solid var(--border-color);
  padding: 1rem 0;
  position: sticky;
  top: 0;
  z-index: 100;
  backdrop-filter: blur(10px);
  background: rgba(255,255,255,0.95);
}

.nav-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav-logo {
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--text-primary);
  text-decoration: none;
  letter-spacing: -0.02em;
}

.nav-links {
  display: flex;
  gap: 2rem;
}

.nav-link {
  color: var(--text-secondary);
  text-decoration: none;
  font-size: 0.95rem;
  font-weight: 500;
  transition: color 0.2s;
  padding: 0.5rem 0;
  border-bottom: 2px solid transparent;
}

.nav-link:hover {
  color: var(--accent-color);
}

.nav-link.active {
  color: var(--accent-color);
  border-bottom-color: var(--accent-color);
}

/* Хлебные крошки */
.breadcrumbs {
  background: var(--bg-secondary);
  border-bottom: 1px solid var(--border-color);
  padding: 0.75rem 0;
}

.breadcrumbs-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  font-size: 0.9rem;
}

.breadcrumb-link {
  color: var(--accent-color);
  text-decoration: none;
}

.breadcrumb-link:hover {
  text-decoration: underline;
}

.breadcrumb-separator {
  color: var(--text-secondary);
  margin: 0 0.5rem;
}

.breadcrumb-current {
  color: var(--text-primary);
  font-weight: 500;
}

/* Основной контент */
.page-content {
  background: var(--bg-primary);
  min-height: calc(100vh - 200px);
  padding: 3rem 0;
}

.content-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

/* Заголовок страницы */
.page-header {
  margin-bottom: 2.5rem;
}

.page-title {
  font-size: 2.5rem;
  font-weight: 700;
  color: var(--text-primary);
  margin: 0 0 0.5rem 0;
  letter-spacing: -0.02em;
}

.page-description {
  font-size: 1.1rem;
  color: var(--text-secondary);
  margin: 0;
}

/* Секция фильтра */
.filter-section {
  margin-bottom: 2.5rem;
  padding: 1.25rem;
  background: var(--bg-secondary);
  border-radius: 12px;
  display: flex;
  align-items: center;
  gap: 1.5rem;
  flex-wrap: wrap;
}

.filter-label {
  font-weight: 500;
  color: var(--text-primary);
  font-size: 0.95rem;
}

.filter-buttons {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
}

.filter-btn {
  padding: 0.5rem 1.25rem;
  border: 1px solid var(--border-color);
  background: var(--bg-primary);
  color: var(--text-secondary);
  border-radius: 20px;
  font-size: 0.9rem;
  font-weight: 500;
  cursor: pointer;
  transition: all 0.2s;
}

.filter-btn:hover {
  border-color: var(--accent-color);
  color: var(--accent-color);
}

.filter-btn.active {
  background: var(--accent-color);
  border-color: var(--accent-color);
  color: white;
}

/* Сетка постов */
.posts-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
  gap: 1.5rem;
}

/* Карточка поста */
.post-card {
  background: var(--bg-primary);
  border: 1px solid var(--border-color);
  border-radius: 16px;
  overflow: hidden;
  transition: all 0.3s ease;
  box-shadow: var(--card-shadow);
}

.post-card:hover {
  transform: translateY(-4px);
  box-shadow: var(--card-shadow-hover);
  border-color: transparent;
}

.post-card-content {
  padding: 1.75rem;
}

.post-title {
  margin: 0 0 1rem 0;
  font-size: 1.5rem;
  font-weight: 600;
  line-height: 1.3;
}

.post-title a {
  color: var(--text-primary);
  text-decoration: none;
  transition: color 0.2s;
}

.post-title a:hover {
  color: var(--accent-color);
}

.post-meta {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 1rem;
}

.post-date {
  color: var(--text-secondary);
  font-size: 0.9rem;
}

.difficulty-badge {
  padding: 0.25rem 0.75rem;
  border-radius: 20px;
  font-size: 0.75rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.02em;
}

.difficulty-easy {
  background: rgba(46, 204, 113, 0.1);
  color: #27ae60;
  border: 1px solid rgba(46, 204, 113, 0.2);
}

.difficulty-medium {
  background: rgba(241, 196, 15, 0.1);
  color: #f39c12;
  border: 1px solid rgba(241, 196, 15, 0.2);
}

.difficulty-hard {
  background: rgba(231, 76, 60, 0.1);
  color: #c0392b;
  border: 1px solid rgba(231, 76, 60, 0.2);
}

.difficulty-insane {
  background: rgba(155, 89, 182, 0.1);
  color: #8e44ad;
  border: 1px solid rgba(155, 89, 182, 0.2);
}

.post-excerpt {
  color: var(--text-secondary);
  font-size: 0.95rem;
  line-height: 1.6;
  margin-bottom: 1.5rem;
}

.read-more-link {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  color: var(--accent-color);
  text-decoration: none;
  font-size: 0.95rem;
  font-weight: 500;
  transition: gap 0.2s;
}

.read-more-link:hover {
  gap: 0.75rem;
}

.arrow-icon {
  transition: transform 0.2s;
}

.read-more-link:hover .arrow-icon {
  transform: translateX(4px);
}

/* Пустое состояние */
.no-posts {
  grid-column: 1 / -1;
  text-align: center;
  padding: 4rem;
  background: var(--bg-secondary);
  border-radius: 16px;
  color: var(--text-secondary);
}

/* Адаптивность */
@media (max-width: 768px) {
  .nav-container {
    flex-direction: column;
    gap: 1rem;
    padding: 0 1rem;
  }
  
  .nav-links {
    gap: 1rem;
    flex-wrap: wrap;
    justify-content: center;
  }
  
  .filter-section {
    flex-direction: column;
    align-items: flex-start;
    gap: 1rem;
  }
  
  .posts-grid {
    grid-template-columns: 1fr;
  }
  
  .page-title {
    font-size: 2rem;
  }
  
  .content-container {
    padding: 0 1rem;
  }
}

/* Анимации */
@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.post-card {
  animation: fadeIn 0.5s ease forwards;
}
</style>
