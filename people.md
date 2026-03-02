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
  <div class="card-list" style="margin-bottom:1.2rem;">
    {% for member in group.items %}
    <article class="card">
      <h3>{{ member.name }}</h3>
      <p class="muted">{{ member.position }}</p>
      <p>{{ member.interests }}</p>
      <p><a href="mailto:{{ member.email }}">{{ member.email }}</a></p>
    </article>
    {% endfor %}
  </div>
  {% endfor %}
</section>
