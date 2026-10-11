---
title: Home
---

<section class="hero hero-single">
  <div class="hero-main">
    <div>
      <h1>Applied and Probabilistic Machine Learning Lab.</h1>
      <p class="hero-intro">Our lab develops probabilistic AI methods for industrial and manufacturing problems, spanning theoretical foundations through real-world applications. In these settings, model failures can lead to substantial losses and negative consequences, making uncertainty, robustness, and reliability central requirements rather than optional properties. We study how to remove unsafe distributions, construct robust generative and foundation models, and enable trustworthy learning and serving when domain-specific data are available. Our research brings together diffusion and flow matching, Bayesian post-training, multimodal and 3D reasoning, and foundation-model adaptation. Across these areas, we aim to translate principled probabilistic modeling into safe, controllable, and practical AI systems for industry.</p>
    </div>

    <div>
      <h3>Research Focus</h3>
      <ul class="info-list">
        <li><strong>Probabilistic Generative Modeling:</strong> diffusion, flow matching, and neural processes</li>
        <li><strong>Safe and Controllable Generative AI:</strong> negative guidance and inference-time steering</li>
        <li><strong>Reliable Foundation Model Adaptation:</strong> Bayesian post-training and generalization</li>
        <li><strong>Multimodal and 3D Intelligence:</strong> vision-language learning and neural representations</li>
        <li><strong>Industrial Applications:</strong> industrial foundation models and visual reasoning</li>
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
