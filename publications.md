---
title: Publications
permalink: /publications/
---

<section class="section" style="margin-top:0;">
  <div class="section-header">
    <h1>Publications</h1>
  </div>

  {% assign pubs = site.publications | sort: 'year' | reverse %}
  {% assign years = pubs | map: 'year' | uniq %}

  {% for year in years %}
  <div class="pub-year-heading">
    <h2>{{ year }}</h2>
    <div class="line"></div>
  </div>

  {% for pub in pubs %}
    {% if pub.year == year %}
      {% unless pub.category == 'workshop' %}
        {% include publication-entry.html pub=pub %}
      {% endunless %}
    {% endif %}
  {% endfor %}

  {% capture workshop_entries %}
    {% for pub in pubs %}
      {% if pub.year == year %}
        {% if pub.category == 'workshop' %}
          {% include publication-entry.html pub=pub %}
        {% endif %}
      {% endif %}
    {% endfor %}
  {% endcapture %}
  {% assign workshop_entries = workshop_entries | strip %}

  {% if workshop_entries != '' %}
  <div class="pub-subheading">
    <h3>Workshop</h3>
    <div class="line"></div>
  </div>

  {{ workshop_entries }}
  {% endif %}

  {% endfor %}
</section>
