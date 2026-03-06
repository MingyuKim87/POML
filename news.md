---
title: News
permalink: /news/
---

<section class="section" style="margin-top:0;">
  <div class="section-header">
    <h1>News</h1>
  </div>

  {% assign news_list = site.news | sort: 'date' | reverse %}
  {% assign previous_year = '' %}

  {% for item in news_list %}
    {% assign item_year = item.date | date: "%Y" %}
    {% if item_year >= '2026' %}
      {% if item_year != previous_year %}
      <div class="pub-year-heading">
        <h2>{{ item_year }}</h2>
        <div class="line"></div>
      </div>
      {% assign previous_year = item_year %}
      {% endif %}

      <article class="news-entry">
        <h3>{{ item.title }}</h3>
        <p class="member-keywords news-detail">{{ item.summary }}</p>
      </article>
    {% endif %}
  {% endfor %}
</section>
