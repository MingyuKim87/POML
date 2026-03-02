---
title: Gallery
permalink: /gallery/
---

<section class="section" style="margin-top:0;">
  <div class="section-header">
    <h1>Gallery</h1>
  </div>

  <div class="gallery-grid">
  {% for image in site.gallery %}
    <figure>
      <img src="{{ image.image }}" alt="{{ image.title }}" />
      <figcaption class="gallery-title">{{ image.title }}</figcaption>
      {% if image.detail %}<p class="gallery-detail">{{ image.detail }}</p>{% endif %}
    </figure>
  {% endfor %}
  </div>
</section>
