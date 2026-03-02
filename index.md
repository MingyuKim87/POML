---
title: Home
---

<section class="hero hero-single">
  <div class="hero-main">
    <div>
      <h1>Probabilistic Machine Learning</h1>
      <p class="hero-intro">Our lab develops probabilistic methodologies that can faithfully model both safe and unsafe distributions. In addition to diffusion/flow matching for image, video, and language models, we are even exploring action models. We are also highly interested in fine-tuning foundation models, including vision-language models and large language models, and in preventing overfitting.</p>
    </div>

    <div>
      <h3>Research Highlights</h3>
      <ul class="info-list">
        <li>Reliable perception in uncertain visual conditions</li>
        <li>Human-in-the-loop machine learning</li>
        <li>Data-centric evaluation for deployment safety</li>
      </ul>
    </div>

    <p class="hero-meta">AI, Kookmin University, Seoul, Republic of Korea</p>
  </div>
</section>

<section class="section">
  <div class="section-header">
    <h2>Latest News</h2>
  </div>
  {% assign sorted_news = site.news | sort: 'date' | reverse %}
  {% for item in sorted_news limit:3 %}
    <article class="news-entry">
      <h3>{{ item.title }}</h3>
      <p class="member-keywords news-detail">{{ item.summary }}</p>
    </article>
  {% endfor %}
</section>
