---
layout: blog
title: "HackTheBox врайтапы"
permalink: /htb/
---

{% for post in site.categories.htb %}
  <article class="post-item">
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d.%m.%Y" }}</time>
    <p>{{ post.excerpt | strip_html | truncate: 200 }}</p>
  </article>
{% endfor %}
