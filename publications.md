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
  <article class="card" style="margin-bottom:0.8rem;">
    <h3>{{ pub.title }}</h3>
    <p class="muted">{{ pub.authors }} ({{ pub.year }})</p>
    <p>{{ pub.venue }}</p>
    {% if pub.link %}<p><a href="{{ pub.link }}" target="_blank" rel="noopener">Paper Link</a></p>{% endif %}
  </article>
  {% endfor %}
</section>
