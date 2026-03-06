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
    <article class="pub-entry">
      <h3 class="pub-title">{{ pub.title }}</h3>
      <p class="muted pub-authors">{{ pub.authors }}</p>
      <p class="pub-venue">{{ pub.venue }}</p>
      {% if pub.paper or pub.code %}
      <p class="pub-links">
        {% if pub.paper %}<a href="{{ pub.paper }}" target="_blank" rel="noopener">[paper]</a>{% endif %}
        {% if pub.paper and pub.code %} {% endif %}
        {% if pub.code %}<a href="{{ pub.code }}" target="_blank" rel="noopener">[code]</a>{% endif %}
      </p>
      {% endif %}
    </article>
    {% endif %}
  {% endfor %}
  {% endfor %}
</section>
