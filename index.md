---
title: Home
---

<section class="hero hero-single">
  <div class="hero-main">
    <div>
      <h1>Probabilistic Machine Learning Lab</h1>
      <p class="hero-intro">Our lab develops probabilistic methods to model both safe and unsafe distributions, with a focus on controlling generation toward safe outcomes. We study diffusion and flow-matching frameworks for image, video, and language models, and are extending these ideas to action models. We are also deeply interested in fine-tuning foundation models, including vision-language models and large language models, while mitigating overfitting.</p>
    </div>

    <div>
      <h3>Research Highlights</h3>
      <ul class="info-list">
        <li>Safe AI grounded in probabilistic modeling</li>
        <li>Mitigating overfitting during post-training of foundation models</li>
        <li>Probabilistic approaches for generative modeling</li>
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
