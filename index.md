---
layout: default
title: Home
---

<section class="hero">
  <div class="container">
    <h1>Welcome to The Coffeen</h1>
    <p class="tagline">☕ Your cozy blog for coffee, code & creative thinking ☕</p>
    <p class="intro">
      From the smoothest flat whites to the harshest instant fixes, we review and muse over it all — one cup at a time.
    </p>
  </div>
</section>

<section class="latest-posts">
  <div class="container">
    <h2>Latest Brews <span class="bean-icon">🌱</span></h2>
    <ul class="post-list">
      {% for post in site.posts limit:3 %}
        <li class="post-item">
          <h3>☕ <a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
          <small>{{ post.date | date: "%B %d, %Y" }}</small>
          <p>{{ post.excerpt | strip_html | truncate: 160 }}</p>
        </li>
      {% endfor %}
    </ul>
  </div>
</section>
