---
title: Home
---

<section class="hero hero-single">
  <div class="hero-main">
    <div>
      <h1>Probabilistic Machine Learning Lab.</h1>
      <p class="hero-intro">Our lab develops probabilistic methods for modeling both safe and unsafe distributions in AI, with the goal of controlling generation toward safe and reliable outcomes. Our research centers on diffusion and flow-matching frameworks for image, video, and language models, and we are actively extending these ideas to action models. We also study the fine-tuning of foundation models, including vision-language models and large language models, with particular attention to mitigating overfitting. Across these areas, trustworthiness and reliability serve as core principles shaping our research.</p>
    </div>

    <div>
      <h3>Research Focus</h3>
      <ul class="info-list">
        <li><strong>Probabilistic Generative Modeling:</strong> diffusion, flow matching, and neural processes</li>
        <li><strong>Safe and Controllable Generative AI:</strong> negative guidance and inference-time steering</li>
        <li><strong>Reliable Foundation Model Adaptation:</strong> Bayesian post-training and generalization</li>
        <li><strong>Multimodal and 3D Intelligence:</strong> vision-language learning and neural representations</li>
      </ul>
    </div>

    <p class="hero-meta">Department of AI, Kookmin University, Seoul, Republic of Korea</p>
  </div>
</section>

<section class="home-calendar-link" aria-labelledby="home-calendar-title">
  <div>
    <p id="home-calendar-title" class="home-calendar-title"><strong>Calendar</strong></p>
    <p>Check Mingyu's monthly availability before arranging a meeting.</p>
  </div>
  <a class="calendar-link-button" href="{{ '/calendar/' | relative_url }}">View calendar <span aria-hidden="true">&rarr;</span></a>
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
