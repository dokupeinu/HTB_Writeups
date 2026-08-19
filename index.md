---
layout: default
title: Home
---
<section class="hero">
  <div class="eyebrow">PENETRATION TESTING / HTB</div>
  <h1>HTB Writeups</h1>
  <p>Hack The Box machines and labs documented with the techniques and commands used.</p>
</section>

<section>
  <h2 class="section-title">Latest writeups</h2>
  <div class="writeup-list">
    {% assign posts = site.writeups | sort: 'date' | reverse %}
    {% for post in posts limit:10 %}
      <a class="card" href="{{ post.url | relative_url }}">
        <h2>{{ post.title }}</h2>
        <p>{{ post.description }}</p>
        <div class="card-meta">
          {% if post.os %}<span>{{ post.os }}</span>{% endif %}
          {% if post.difficulty %}<span>{{ post.difficulty }}</span>{% endif %}
          <span>{{ post.date | date: "%d %b %Y" }}</span>
        </div>
      </a>
    {% else %}
      <div class="callout">No writeups published yet.</div>
    {% endfor %}
  </div>
</section>
