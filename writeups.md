---
layout: default
title: Writeups
---

<div class="post">
  <div class="eyebrow">ARCHIVE</div>
  <h1>Writeups</h1>
  <div class="writeup-list">
    {% assign posts = site.writeups | sort: 'date' | reverse %}
    {% for post in posts %}
      <a class="card" href="{{ post.url | relative_url }}">
        <h2>{{ post.title }}</h2>
        <p>{{ post.description }}</p>
        <div class="card-meta">
          {% if post.os %}<span>{{ post.os }}</span>{% endif %}
          {% if post.difficulty %}<span>{{ post.difficulty }}</span>{% endif %}
          <span>{{ post.date | date: "%d %b %Y" }}</span>
        </div>
      </a>
    {% endfor %}
  </div>
</div>
