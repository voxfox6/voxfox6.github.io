---
layout: default
title: "Инструменты и методология"
permalink: /tools/
---

<div class="breadcrumbs" style="margin-bottom: 2rem;">
  <a href="/">Главная</a> / <span>Инструменты</span>
</div>

<h1>🧰 Инструменты и методология</h1>
<p style="color: var(--muted-text); margin-bottom: 2rem;">Заметки, FAQ, шпаргалки и наработки по инструментам пентеста</p>

<!-- Быстрая навигация по категориям -->
<div class="tools-nav" style="margin-bottom: 2rem; display: flex; gap: 0.5rem; flex-wrap: wrap;">
  <a href="#recon" class="tools-nav-link" style="padding: 0.3rem 1rem; background: var(--bg-secondary); border: 1px solid var(--border); border-radius: 20px; color: var(--text); text-decoration: none; font-size: 0.9rem;">🔍 Разведка</a>
  <a href="#web" class="tools-nav-link" style="padding: 0.3rem 1rem; background: var(--bg-secondary); border: 1px solid var(--border); border-radius: 20px; color: var(--text); text-decoration: none; font-size: 0.9rem;">🌐 Веб</a>
  <a href="#exploit" class="tools-nav-link" style="padding: 0.3rem 1rem; background: var(--bg-secondary); border: 1px solid var(--border); border-radius: 20px; color: var(--text); text-decoration: none; font-size: 0.9rem;">⚡ Эксплуатация</a>
  <a href="#privesc" class="tools-nav-link" style="padding: 0.3rem 1rem; background: var(--bg-secondary); border: 1px solid var(--border); border-radius: 20px; color: var(--text); text-decoration: none; font-size: 0.9rem;">⬆️ Повышение привилегий</a>
  <a href="#methodology" class="tools-nav-link" style="padding: 0.3rem 1rem; background: var(--bg-secondary); border: 1px solid var(--border); border-radius: 20px; color: var(--text); text-decoration: none; font-size: 0.9rem;">📋 Методология</a>
  <a href="#faq" class="tools-nav-link" style="padding: 0.3rem 1rem; background: var(--bg-secondary); border: 1px solid var(--border); border-radius: 20px; color: var(--text); text-decoration: none; font-size: 0.9rem;">❓ FAQ</a>
</div>

<!-- Секция: Разведка -->
<section id="recon" class="tools-section" style="margin-bottom: 3rem;">
  <h2 style="display: flex; align-items: center; gap: 0.5rem; border-bottom: 1px solid var(--border); padding-bottom: 0.5rem;">
    <span>🔍 Разведка (Recon)</span>
  </h2>
  
  <div class="tools-grid" style="display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 1.5rem; margin-top: 1.5rem;">
    <!-- Карточка инструмента -->
    <div class="tool-card" style="background: var(--bg-secondary); border: 1px solid var(--border); border-radius: 12px; padding: 1.25rem;">
      <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 0.75rem;">
        <h3 style="margin: 0; font-size: 1.2rem;">Nmap</h3>
        <span style="font-size: 0.75rem; padding: 0.2rem 0.6rem; background: var(--accent); color: var(--bg); border-radius: 12px;">must know</span>
      </div>
      <p style="color: var(--text); font-size: 0.95rem; margin-bottom: 1rem;">Сканирование портов, обнаружение сервисов, NSE скрипты</p>
      <div style="display: flex; gap: 0.5rem; margin-bottom: 1rem; flex-wrap: wrap;">
        <span style="font-size: 0.8rem; padding: 0.2rem 0.5rem; background: var(--bg-tertiary); border-radius: 4px;">#scanning</span>
        <span style="font-size: 0.8rem; padding: 0.2rem 0.5rem; background: var(--bg-tertiary); border-radius: 4px;">#network</span>
      </div>
      <a href="/tools/nmap" style="color: var(--accent); text-decoration: none; font-size: 0.9rem;">Заметки →</a>
    </div>

    <!-- Карточка инструмента -->
    <div class="tool-card" style="background: var(--bg-secondary); border: 1px solid var(--border); border-radius: 12px; padding: 1.25rem;">
      <h3 style="margin: 0 0 0.75rem 0; font-size: 1.2rem;">Feroxbuster</h3>
      <p style="color: var(--text); font-size: 0.95rem; margin-bottom: 1rem;">Перебор директорий и файлов на веб-серверах</p>
      <div style="display: flex; gap: 0.5rem; margin-bottom: 1rem; flex-wrap: wrap;">
        <span style="font-size: 0.8rem; padding: 0.2rem 0.5rem; background: var(--bg-tertiary); border-radius: 4px;">#fuzzing</span>
        <span style="font-size: 0.8rem; padding: 0.2rem 0.5rem; background: var(--bg-tertiary); border-radius: 4px;">#web</span>
      </div>
      <a href="/tools/feroxbuster" style="color: var(--accent); text-decoration: none; font-size: 0.9rem;">Заметки →</a>
    </div>

    <!-- Карточка инструмента -->
    <div class="tool-card" style="background: var(--bg-secondary); border: 1px solid var(--border); border-radius: 12px; padding: 1.25rem;">
      <h3 style="margin: 0 0 0.75rem 0; font-size: 1.2rem;">Gobuster</h3>
      <p style="color: var(--text); font-size: 0.95rem; margin-bottom: 1rem;">Альтернатива Feroxbuster, DNS/subdomain bruteforce</p>
      <div style="display: flex; gap: 0.5rem; margin-bottom: 1rem; flex-wrap: wrap;">
        <span style="font-size: 0.8rem; padding: 0.2rem 0.5rem; background: var(--bg-tertiary); border-radius: 4px;">#dns</span>
        <span style="font-size: 0.8rem; padding: 0.2rem 0.5rem; background: var(--bg-tertiary); border-radius: 4px;">#subdomains</span>
      </div>
      <a href="/tools/gobuster" style="color: var(--accent); text-decoration: none; font-size: 0.9rem;">Заметки →</a>
    </div>
  </div>
</section>

<!-- Секция: Веб -->
<section id="web" class="tools-section" style="margin-bottom: 3rem;">
  <h2 style="display: flex; align-items: center; gap: 0.5rem; border-bottom: 1px solid var(--border); padding-bottom: 0.5rem;">
    <span>🌐 Веб-уязвимости</span>
  </h2>
  
  <div class="tools-grid" style="display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 1.5rem; margin-top: 1.5rem;">
    <!-- Карточка инструмента -->
    <div class="tool-card" style="background: var(--bg-secondary); border: 1px solid var(--border); border-radius: 12px; padding: 1.25rem;">
      <h3 style="margin: 0 0 0.75rem 0; font-size: 1.2rem;">SQLMap</h3>
      <p style="color: var(--text); font-size: 0.95rem; margin-bottom: 1rem;">Автоматизация поиска и эксплуатации SQL-инъекций</p>
      <div style="display: flex; gap: 0.5rem; margin-bottom: 1rem; flex-wrap: wrap;">
        <span style="font-size: 0.8rem; padding: 0.2rem 0.5rem; background: var(--bg-tertiary); border-radius: 4px;">#sql</span>
        <span style="font-size: 0.8rem; padding: 0.2rem 0.5rem; background: var(--bg-tertiary); border-radius: 4px;">#injection</span>
      </div>
      <a href="/tools/sqlmap" style="color: var(--accent); text-decoration: none; font-size: 0.9rem;">Заметки →</a>
    </div>

    <!-- Карточка методологии -->
    <div class="tool-card methodology-card" style="background: linear-gradient(135deg, var(--bg-secondary) 0%, var(--bg-tertiary) 100%); border: 1px solid var(--border); border-radius: 12px; padding: 1.25rem; border-left: 3px solid var(--accent);">
      <div style="display: flex; align-items: center; gap: 0.5rem; margin-bottom: 0.75rem;">
        <span style="font-size: 1.5rem;">📝</span>
        <h3 style="margin: 0; font-size: 1.2rem;">LFI to RLS</h3>
      </div>
      <p style="color: var(--text); font-size: 0.95rem; margin-bottom: 1rem;">Цепочка атаки: Local File Inclusion → RCE через log poisoning</p>
      <div style="display: flex; gap: 0.5rem; margin-bottom: 1rem; flex-wrap: wrap;">
        <span style="font-size: 0.8rem; padding: 0.2rem 0.5rem; background: var(--bg-tertiary); border-radius: 4px;">#methodology</span>
        <span style="font-size: 0.8rem; padding: 0.2rem 0.5rem; background: var(--bg-tertiary); border-radius: 4px;">#lfi</span>
      </div>
      <a href="/tools/lfi-methodology" style="color: var(--accent); text-decoration: none; font-size: 0.9rem;">Читать →</a>
    </div>
  </div>
</section>

<!-- Секция: Повышение привилегий -->
<section id="privesc" class="tools-section" style="margin-bottom: 3rem;">
  <h2 style="display: flex; align-items: center; gap: 0.5rem; border-bottom: 1px solid var(--border); padding-bottom: 0.5rem;">
    <span>⬆️ Повышение привилегий</span>
  </h2>
  
  <div class="tools-grid" style="display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 1.5rem; margin-top: 1.5rem;">
    <!-- Карточка чеклиста -->
    <div class="tool-card checklist-card" style="background: var(--bg-secondary); border: 1px solid var(--border); border-radius: 12px; padding: 1.25rem;">
      <div style="display: flex; align-items: center; gap: 0.5rem; margin-bottom: 0.75rem;">
        <span style="font-size: 1.5rem;">✅</span>
        <h3 style="margin: 0; font-size: 1.2rem;">Linux Privesc Checklist</h3>
      </div>
      <p style="color: var(--text); font-size: 0.95rem; margin-bottom: 1rem;">Что проверять: sudo -l, SUID, capabilities, cron, PATH</p>
      <div style="display: flex; gap: 0.5rem; margin-bottom: 1rem; flex-wrap: wrap;">
        <span style="font-size: 0.8rem; padding: 0.2rem 0.5rem; background: var(--bg-tertiary); border-radius: 4px;">#linux</span>
        <span style="font-size: 0.8rem; padding: 0.2rem 0.5rem; background: var(--bg-tertiary); border-radius: 4px;">#checklist</span>
      </div>
      <a href="/tools/linux-privesc" style="color: var(--accent); text-decoration: none; font-size: 0.9rem;">Открыть →</a>
    </div>

    <!-- Карточка инструмента -->
    <div class="tool-card" style="background: var(--bg-secondary); border: 1px solid var(--border); border-radius: 12px; padding: 1.25rem;">
      <h3 style="margin: 0 0 0.75rem 0; font-size: 1.2rem;">LinPEAS</h3>
      <p style="color: var(--text); font-size: 0.95rem; margin-bottom: 1rem;">Автоматизированный поиск путей повышения привилегий</p>
      <div style="display: flex; gap: 0.5rem; margin-bottom: 1rem; flex-wrap: wrap;">
        <span style="font-size: 0.8rem; padding: 0.2rem 0.5rem; background: var(--bg-tertiary); border-radius: 4px;">#automation</span>
        <span style="font-size: 0.8rem; padding: 0.2rem 0.5rem; background: var(--bg-tertiary); border-radius: 4px;">#enumeration</span>
      </div>
      <a href="/tools/linpeas" style="color: var(--accent); text-decoration: none; font-size: 0.9rem;">Заметки →</a>
    </div>
  </div>
</section>

<!-- Секция: FAQ -->
<section id="faq" class="tools-section" style="margin-bottom: 3rem;">
  <h2 style="display: flex; align-items: center; gap: 0.5rem; border-bottom: 1px solid var(--border); padding-bottom: 0.5rem;">
    <span>❓ Часто задаваемые вопросы</span>
  </h2>
  
  <div class="faq-list" style="margin-top: 1.5rem;">
    <details class="faq-item" style="margin-bottom: 1rem; padding: 1rem; background: var(--bg-secondary); border: 1px solid var(--border); border-radius: 8px;">
      <summary style="font-weight: 600; color: var(--text); cursor: pointer;">Что делать если не открывается reverse shell?</summary>
      <div style="margin-top: 0.75rem; color: var(--text); font-size: 0.95rem;">
        <p>Проверь:</p>
        <ul style="margin-left: 1.5rem;">
          <li>Правильно ли указан IP и порт</li>
          <li>Запущен ли listener (nc -lvnp PORT)</li>
          <li>Не блокирует ли фаервол</li>
          <li>Попробуй другой шелл (bash, python, nc)</li>
        </ul>
      </div>
    </details>

    <details class="faq-item" style="margin-bottom: 1rem; padding: 1rem; background: var(--bg-secondary); border: 1px solid var(--border); border-radius: 8px;">
      <summary style="font-weight: 600; color: var(--text); cursor: pointer;">Как передать файлы на целевую машину?</summary>
      <div style="margin-top: 0.75rem; color: var(--text); font-size: 0.95rem;">
        <p>Способы:</p>
        <ul style="margin-left: 1.5rem;">
          <li>Python HTTP server: python3 -m http.server</li>
          <li>wget/curl на целевой машине</li>
          <li>nc - передача файлов через netcat</li>
          <li>base64 кодирование для передачи через echo</li>
        </ul>
      </div>
    </details>
  </div>
</section>

<!-- Секция: Недавние обновления -->
<section class="recent-updates" style="margin-top: 3rem; padding: 1.5rem; background: var(--bg-secondary); border-radius: 12px;">
  <h3 style="margin-top: 0; margin-bottom: 1rem;">📌 Недавние обновления</h3>
  <ul style="list-style: none; padding: 0; margin: 0;">
    <li style="padding: 0.5rem 0; border-bottom: 1px solid var(--border); display: flex; gap: 1rem;">
      <span style="color: var(--muted-text); font-size: 0.9rem;">10.03.2026</span>
      <span>Добавлена методология LFI → RCE</span>
    </li>
    <li style="padding: 0.5rem 0; border-bottom: 1px solid var(--border); display: flex; gap: 1rem;">
      <span style="color: var(--muted-text); font-size: 0.9rem;">09.03.2026</span>
      <span>Обновлен чеклист Linux Privesc</span>
    </li>
    <li style="padding: 0.5rem 0; display: flex; gap: 1rem;">
      <span style="color: var(--muted-text); font-size: 0.9rem;">08.03.2026</span>
      <span>Добавлены шпаргалки по Feroxbuster</span>
    </li>
  </ul>
</section>

<!-- Стили для страницы Tools -->
<style>
.tools-nav-link:hover {
  background: var(--accent) !important;
  color: var(--bg) !important;
  border-color: var(--accent) !important;
}

.tool-card {
  transition: transform 0.2s, box-shadow 0.2s;
}

.tool-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  border-color: var(--accent) !important;
}

.faq-item summary {
  list-style: none;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.faq-item summary::-webkit-details-marker {
  display: none;
}

.faq-item summary::before {
  content: "▶";
  color: var(--accent);
  font-size: 0.8rem;
  transition: transform 0.2s;
}

.faq-item[open] summary::before {
  transform: rotate(90deg);
}

:root {
  --accent: #66c0f0;
  --bg-secondary: #1a1e24;
  --bg-tertiary: #252b33;
}

[data-theme="dark"] {
  --bg-secondary: #1a1e24;
  --bg-tertiary: #252b33;
}

[data-theme="light"] {
  --bg-secondary: #f5f5f5;
  --bg-tertiary: #eaeaea;
}
</style>
