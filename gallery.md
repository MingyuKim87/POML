---
title: Gallery
permalink: /gallery/
---

<section class="section" style="margin-top:0;">
  <div class="section-header">
    <h1>Gallery</h1>
  </div>

  {% assign gallery_list = site.gallery | sort: 'date' %}
  <div class="gallery-grid" style="margin-bottom:1.3rem;">
    {% for image in gallery_list %}
      <figure class="gallery-entry">
        <img src="{{ image.image }}" alt="{{ image.title }}" />
        <figcaption>{{ image.title }}</figcaption>
        {% if image.detail %}
        <p class="member-keywords gallery-detail">{{ image.detail }}</p>
        {% endif %}
      </figure>
    {% endfor %}
  </div>
</section>
