---
title: Home
---

<section class="hero">
  <div class="hero-main">
    <div>
      <span class="hero-kicker">Research Laboratory</span>
      <h1>Precision Objects & Machine Learning (POML)</h1>
      <p class="hero-intro">POML develops dependable AI systems for physical environments. We focus on robust perception, multimodal learning, and practical deployment pathways from lab to field.</p>
    </div>
    <p class="hero-meta">Department of Computer Science · KAIST · Daejeon, Republic of Korea</p>
  </div>

  <aside class="hero-aside">
    <h3>Research Highlights</h3>
    <ul class="info-list">
      <li>Reliable perception in uncertain visual conditions</li>
      <li>Human-in-the-loop machine learning</li>
      <li>Data-centric evaluation for deployment safety</li>
    </ul>
  </aside>
</section>

<section class="section">
  <div class="section-header">
    <h2>Latest News</h2>
    <p>Recent lab updates and announcements.</p>
  </div>
  <div class="card-list">
  {% assign sorted_news = site.news | sort: 'date' | reverse %}
  {% for item in sorted_news limit:3 %}
    <article class="card">
      <h3>{{ item.title }}</h3>
      <p class="muted">{{ item.date | date: "%Y-%m-%d" }}</p>
      <p>{{ item.summary }}</p>
    </article>
  {% endfor %}
  </div>
</section>

<section class="section">
  <div class="section-header">
    <h2>Selected Publications</h2>
    <p>Recent representative publications.</p>
  </div>
  <div class="card-list">
  {% assign sorted_pubs = site.publications | sort: 'year' | reverse %}
  {% for pub in sorted_pubs limit:3 %}
    <article class="card">
      <h3>{{ pub.title }}</h3>
      <p class="muted">{{ pub.authors }} ({{ pub.year }})</p>
      <p>{{ pub.venue }}</p>
    </article>
  {% endfor %}
  </div>
</section>
