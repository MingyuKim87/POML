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

  {% assign main_pubs = pubs | where: 'year', year | where_exp: 'item', "item.category != 'workshop'" %}
  {% assign lead_pubs = main_pubs | where_exp: 'item', "item.authorship != 'coauthor'" %}
  {% assign coauthored_pubs = main_pubs | where: 'authorship', 'coauthor' | sort: 'coauthor_order' %}
  {% assign ordered_main_pubs = lead_pubs | concat: coauthored_pubs %}
  {% assign workshop_pubs = pubs | where: 'year', year | where: 'category', 'workshop' %}

  {% for pub in ordered_main_pubs %}
    {% include publication-entry.html pub=pub %}
  {% endfor %}

  {% if workshop_pubs.size > 0 %}
  <div class="pub-subheading">
    <h3>Workshop</h3>
    <div class="line"></div>
  </div>

  {% for pub in workshop_pubs %}
    {% include publication-entry.html pub=pub %}
  {% endfor %}
  {% endif %}

  {% endfor %}

</section>
