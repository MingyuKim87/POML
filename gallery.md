---
title: Gallery
permalink: /gallery/
---

<section class="section" style="margin-top:0;">
  <div class="section-header">
    <h1>Gallery</h1>
    <p>Snapshots from lab activities and events.</p>
  </div>

  <div class="gallery-grid">
  {% for image in site.gallery %}
    <figure>
      <img src="{{ image.image }}" alt="{{ image.title }}" />
      <figcaption>{{ image.title }}</figcaption>
    </figure>
  {% endfor %}
  </div>
</section>
