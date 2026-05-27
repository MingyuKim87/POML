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
  {% assign workshop_pubs = pubs | where: 'year', year | where: 'category', 'workshop' %}

  {% for pub in main_pubs %}
    <article class="pub-entry">
      <h3 class="pub-title">{{ pub.title }}</h3>
      <p class="muted pub-authors">{{ pub.authors | replace: "Mingyu Kim", "<u>Mingyu Kim</u>" }}</p>
      <p class="pub-venue">{{ pub.venue }}</p>
      {% if pub.paper or pub.code %}
      <p class="pub-links">
        {% if pub.paper %}
          {% if pub.paper contains '://' %}
            <a href="{{ pub.paper }}" target="_blank" rel="noopener">[paper]</a>
          {% else %}
            {{ pub.paper | markdownify | remove: '<p>' | remove: '</p>' }}
          {% endif %}
        {% endif %}
        {% if pub.code %}<a href="{{ pub.code }}" target="_blank" rel="noopener">[code]</a>{% endif %}
      </p>
      {% endif %}
    </article>
  {% endfor %}

  {% if workshop_pubs.size > 0 %}
  <div class="pub-subheading">
    <h3>Workshop</h3>
    <div class="line"></div>
  </div>

  {% for pub in workshop_pubs %}
    <article class="pub-entry">
      <h3 class="pub-title">{{ pub.title }}</h3>
      <p class="muted pub-authors">{{ pub.authors | replace: "Mingyu Kim", "<u>Mingyu Kim</u>" }}</p>
      <p class="pub-venue">{{ pub.venue }}</p>
      {% if pub.paper or pub.code %}
      <p class="pub-links">
        {% if pub.paper %}
          {% if pub.paper contains '://' %}
            <a href="{{ pub.paper }}" target="_blank" rel="noopener">[paper]</a>
          {% else %}
            {{ pub.paper | markdownify | remove: '<p>' | remove: '</p>' }}
          {% endif %}
        {% endif %}
        {% if pub.code %}<a href="{{ pub.code }}" target="_blank" rel="noopener">[code]</a>{% endif %}
      </p>
      {% endif %}
    </article>
  {% endfor %}
  {% endif %}

  {% endfor %}
{% endfor %}
</section>
