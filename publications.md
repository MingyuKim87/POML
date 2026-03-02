---
title: Publications
permalink: /publications/
---

<section class="section" style="margin-top:0;">
  <div class="section-header">
    <h1>Publications</h1>
    <p>Peer-reviewed works and selected outcomes.</p>
  </div>

  {% assign pubs = site.publications | sort: 'year' | reverse %}
  {% for pub in pubs %}
  <article class="card publication-card" style="margin-bottom:0.55rem;">
    <h3>{{ pub.title }}</h3>
    <p class="muted pub-authors">{{ pub.authors }}</p>
    <p class="pub-venue">{{ pub.venue }}</p>
    {% if pub.paper or pub.code %}
    <p class="pub-links">
      {% if pub.paper %}<a href="{{ pub.paper }}" target="_blank" rel="noopener">paper</a>{% endif %}
      {% if pub.paper and pub.code %} · {% endif %}
      {% if pub.code %}<a href="{{ pub.code }}" target="_blank" rel="noopener">code</a>{% endif %}
    </p>
    {% endif %}
  </article>
  {% endfor %}
</section>
