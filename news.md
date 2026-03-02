---
title: News
permalink: /news/
---

<section class="section" style="margin-top:0;">
  <div class="section-header">
    <h1>News</h1>
    <p>Announcements, events, and achievements.</p>
  </div>

  {% assign news_list = site.news | sort: 'date' | reverse %}
  {% for item in news_list %}
  <article class="card" style="margin-bottom:0.8rem;">
    <h3>{{ item.title }}</h3>
    <p class="muted">{{ item.date | date: "%Y-%m-%d" }}</p>
    <p>{{ item.summary }}</p>
  </article>
  {% endfor %}
</section>
