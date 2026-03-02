---
title: News
permalink: /news/
---

<section class="section" style="margin-top:0;">
  <div class="section-header">
    <h1>News</h1>
  </div>

  {% assign news_list = site.news | sort: 'date' | reverse %}
  {% for item in news_list %}
  <article style="margin-bottom:1.2rem; border-bottom:1px solid var(--line); padding-bottom:0.9rem;">
    <h3>{{ item.title }}</h3>
    <p class="muted">{{ item.date | date: "%Y-%m-%d" }}</p>
    <p>{{ item.summary }}</p>
  </article>
  {% endfor %}
</section>
