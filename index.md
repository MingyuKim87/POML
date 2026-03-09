---
title: Home
---

<section class="hero hero-single">
  <div class="hero-main">
    <div>
      <h1>Probabilistic Machine Learning Lab</h1>
      <p class="hero-intro">Our lab develops probabilistic methods for modeling both safe and unsafe distributions in AI, with the goal of controlling generation toward safe and reliable outcomes. Our research centers on diffusion and flow-matching frameworks for image, video, and language models, and we are actively extending these ideas to action models. We also study the fine-tuning of foundation models, including vision-language models and large language models, with particular attention to mitigating overfitting. Across these areas, trustworthiness and reliability serve as core principles shaping our research.</p>
    </div>

    <div>
      <h3>Research Highlights</h3>
      <ul class="info-list">
        <li>Probabilistic approaches for generative AI</li>
        <li>Safe AI grounded in probabilistic modeling</li>
        <li>Mitigating overfitting during post-training of foundation models</li>
      </ul>
    </div>

    <p class="hero-meta">Department of AI, Kookmin University, Seoul, Republic of Korea</p>
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
