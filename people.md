---
title: People
permalink: /people/
---

<section class="section" style="margin-top:0;">
  <div class="section-header">
    <h1>People</h1>
    <p>Current members and collaborators.</p>
  </div>

  {% assign grouped = site.people | sort: 'order' | group_by: 'role' %}
  {% for group in grouped %}
  <h2>{{ group.name }}</h2>
  <div class="people-grid" style="margin-bottom:1.2rem;">
    {% for member in group.items %}
    <article class="member-card">
      <img class="member-photo" src="{{ member.photo | default: '/assets/images/people/placeholder.svg' | relative_url }}" alt="{{ member.name }}" />
      <h3>{{ member.name }}</h3>
      <p class="member-position">{{ member.position }}</p>
      <p class="member-email"><a href="mailto:{{ member.email }}">{{ member.email }}</a></p>
      {% if member.keywords %}
      <p class="member-keywords">{{ member.keywords | slice: 0, 3 | join: ", " }}</p>
      {% endif %}
      {% if member.webpage %}
      <p class="member-webpage"><a href="{{ member.webpage }}" target="_blank" rel="noopener">Webpage</a></p>
      {% endif %}
    </article>
    {% endfor %}
  </div>
  {% endfor %}
</section>
