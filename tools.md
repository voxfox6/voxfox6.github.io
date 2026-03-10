---
layout: default
title: "Tools"
permalink: /tools/
---

<div class="breadcrumbs" style="margin-bottom: 2rem; font-size: 0.9rem; color: var(--muted-text);">
  <a href="/" style="color: var(--accent); text-decoration: none;">Главная</a> / <span>Tools</span>
</div>

<h1>Tools</h1>
<p style="color: var(--muted-text); margin-bottom: 2.5rem;">Заметки, шпаргалки и методология</p>

<!-- Разведка -->
<section style="margin-bottom: 2.5rem;">
  <h2 style="font-size: 1.5rem; font-weight: 500; margin-bottom: 1.5rem; color: var(--text);">Разведка</h2>
  
  <div style="display: flex; flex-direction: column; gap: 1.5rem;">
    <!-- Nmap -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="/tools/nmap" style="color: var(--accent); text-decoration: none; font-weight: 500;">nmap</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">сканирование портов, NSE скрипты</span>
      </div>
    </div>
    
    <!-- Feroxbuster -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="/tools/feroxbuster" style="color: var(--accent); text-decoration: none; font-weight: 500;">feroxbuster</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">перебор директорий</span>
      </div>
    </div>
    
    <!-- Gobuster -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="/tools/gobuster" style="color: var(--accent); text-decoration: none; font-weight: 500;">gobuster</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">dns, subdomains</span>
      </div>
    </div>
    
    <!-- FFUF -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="/tools/ffuf" style="color: var(--accent); text-decoration: none; font-weight: 500;">ffuf</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">fuzzing</span>
      </div>
    </div>
  </div>
</section>

<!-- Веб -->
<section style="margin-bottom: 2.5rem;">
  <h2 style="font-size: 1.5rem; font-weight: 500; margin-bottom: 1.5rem; color: var(--text);">Веб</h2>
  
  <div style="display: flex; flex-direction: column; gap: 1.5rem;">
    <!-- SQLMap -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="/tools/sqlmap" style="color: var(--accent); text-decoration: none; font-weight: 500;">sqlmap</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">sql инъекции</span>
      </div>
    </div>
    
    <!-- LFI Methodology -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="/tools/lfi" style="color: var(--accent); text-decoration: none; font-weight: 500;">lfi</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">Local File Inclusion</span>
      </div>
    </div>
    
    <!-- XSS -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="/tools/xss" style="color: var(--accent); text-decoration: none; font-weight: 500;">xss</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">Cross-Site Scripting</span>
      </div>
    </div>
  </div>
</section>

<!-- Повышение привилегий -->
<section style="margin-bottom: 2.5rem;">
  <h2 style="font-size: 1.5rem; font-weight: 500; margin-bottom: 1.5rem; color: var(--text);">Повышение привилегий</h2>
  
  <div style="display: flex; flex-direction: column; gap: 1.5rem;">
    <!-- Linux Privesc -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="/tools/linux-privesc" style="color: var(--accent); text-decoration: none; font-weight: 500;">linux checklist</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">sudo, suid, capabilities</span>
      </div>
    </div>
    
    <!-- LinPEAS -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="/tools/linpeas" style="color: var(--accent); text-decoration: none; font-weight: 500;">linpeas</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">автоматизация</span>
      </div>
    </div>
    
    <!-- Windows Privesc -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="/tools/windows-privesc" style="color: var(--accent); text-decoration: none; font-weight: 500;">windows checklist</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">winpeas, acl, service permissions</span>
      </div>
    </div>
    
    <!-- Wildcards -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="/tools/wildcards" style="color: var(--accent); text-decoration: none; font-weight: 500;">wildcards</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">tar, chown, rsync</span>
      </div>
    </div>
  </div>
</section>

<!-- Операционные системы -->
<section style="margin-bottom: 2.5rem;">
  <h2 style="font-size: 1.5rem; font-weight: 500; margin-bottom: 1.5rem; color: var(--text);">Операционные системы</h2>
  
  <div style="display: flex; flex-direction: column; gap: 1.5rem;">
    <!-- Linux -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="/tools/linux" style="color: var(--accent); text-decoration: none; font-weight: 500;">linux</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">базовые команды, трюки</span>
      </div>
    </div>
    
    <!-- Windows -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="/tools/windows" style="color: var(--accent); text-decoration: none; font-weight: 500;">windows</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">cmd, powershell, ad</span>
      </div>
    </div>
  </div>
</section>

<!-- Интересные тулзы -->
<section style="margin-bottom: 2.5rem;">
  <h2 style="font-size: 1.5rem; font-weight: 500; margin-bottom: 1.5rem; color: var(--text);">Интересные тулзы</h2>
  
  <div style="display: flex; flex-direction: column; gap: 1.5rem;">
    <!-- Chisel -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="/tools/chisel" style="color: var(--accent); text-decoration: none; font-weight: 500;">chisel</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">туннели, прокси</span>
      </div>
    </div>
    
    <!-- Ligolo-ng -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="/tools/ligolo" style="color: var(--accent); text-decoration: none; font-weight: 500;">ligolo-ng</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">pivoting</span>
      </div>
    </div>
    
    <!-- Impacket -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="/tools/impacket" style="color: var(--accent); text-decoration: none; font-weight: 500;">impacket</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">psexec, wmiexec, secretsdump</span>
      </div>
    </div>
  </div>
</section>

<!-- Методология -->
<section style="margin-bottom: 2.5rem;">
  <h2 style="font-size: 1.5rem; font-weight: 500; margin-bottom: 1.5rem; color: var(--text);">Методология</h2>
  
  <div style="display: flex; flex-direction: column; gap: 1.5rem;">
    <!-- Reverse Shells -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="/tools/reverse-shells" style="color: var(--accent); text-decoration: none; font-weight: 500;">reverse shells</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">bash, python, nc, php</span>
      </div>
    </div>
    
    <!-- File Transfers -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="/tools/file-transfers" style="color: var(--accent); text-decoration: none; font-weight: 500;">file transfers</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">wget, curl, nc, base64</span>
      </div>
    </div>
    
    <!-- Pivoting -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="/tools/pivoting" style="color: var(--accent); text-decoration: none; font-weight: 500;">pivoting</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">ssh, socks, ligolo</span>
      </div>
    </div>
  </div>
</section>

<!-- Обучение и полезные ссылки -->
<section style="margin-bottom: 2.5rem;">
  <h2 style="font-size: 1.5rem; font-weight: 500; margin-bottom: 1.5rem; color: var(--text);">Обучение и ссылки</h2>
  
  <div style="display: flex; flex-direction: column; gap: 1.5rem;">
    <!-- HackTheBox -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="https://www.hackthebox.com" target="_blank" rel="noopener" style="color: var(--accent); text-decoration: none; font-weight: 500;">hackthebox</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">лаборатория</span>
      </div>
    </div>
    
    <!-- TryHackMe -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="https://tryhackme.com" target="_blank" rel="noopener" style="color: var(--accent); text-decoration: none; font-weight: 500;">tryhackme</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">обучение с нуля</span>
      </div>
    </div>
    
    <!-- HackMyVM -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="https://hackmyvm.eu" target="_blank" rel="noopener" style="color: var(--accent); text-decoration: none; font-weight: 500;">hackmyvm</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">испанские машины</span>
      </div>
    </div>
    
    <!-- PayloadAllTheThings -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="https://github.com/swisskyrepo/PayloadsAllTheThings" target="_blank" rel="noopener" style="color: var(--accent); text-decoration: none; font-weight: 500;">payloads all the things</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">шпаргалки</span>
      </div>
    </div>
    
    <!-- GTFOBins -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="https://gtfobins.github.io" target="_blank" rel="noopener" style="color: var(--accent); text-decoration: none; font-weight: 500;">gtfobins</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">бинарники для privesc</span>
      </div>
    </div>
    
    <!-- LOLBAS -->
    <div style="display: flex; align-items: baseline; gap: 1rem;">
      <span style="color: var(--accent); font-family: monospace;">→</span>
      <div style="flex: 1;">
        <a href="https://lolbas-project.github.io" target="_blank" rel="noopener" style="color: var(--accent); text-decoration: none; font-weight: 500;">lolbas</a>
        <span style="color: var(--muted-text); margin-left: 1rem; font-size: 0.9rem;">windows living off land</span>
      </div>
    </div>
  </div>
</section>

<!-- Подвал с заметкой -->
<hr style="border: none; border-top: 1px solid var(--border); margin: 3rem 0 2rem;">
<p style="color: var(--muted-text); font-size: 0.9rem; font-style: italic;">
  ⚡ Раздел постоянно пополняется. Если чего-то не хватает — будет добавлено.
</p>
