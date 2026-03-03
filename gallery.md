---
title: Gallery
permalink: /gallery/
---

<section class="section" style="margin-top:0;">
  <div class="section-header">
    <h1>Gallery</h1>
  </div>

  {% assign gallery_list = site.gallery | sort: 'date' | reverse %}
  {% assign previous_year = '' %}

  {% for image in gallery_list %}
    {% assign image_year = image.date | date: "%Y" %}
    {% if image_year != previous_year %}
    <div class="pub-year-heading">
      <h2>{{ image_year }}</h2>
      <div class="line"></div>
    </div>
    <div class="gallery-grid" style="margin-bottom:1.3rem;">
    {% assign previous_year = image_year %}
    {% endif %}

      <figure class="gallery-entry">
        <img src="{{ image.image }}" alt="{{ image.title }}" />
        <figcaption>{{ image.title }}</figcaption>
        {% if image.detail %}
        <p class="member-keywords gallery-detail">{{ image.detail }}</p>
        {% endif %}
      </figure>

    {% assign next_index = forloop.index %}
    {% assign next_item = gallery_list[next_index] %}
    {% if next_item == nil %}
    </div>
    {% else %}
    {% assign next_year = next_item.date | date: "%Y" %}
    {% if next_year != image_year %}
    </div>
    {% endif %}
    {% endif %}
  {% endfor %}
</section>
