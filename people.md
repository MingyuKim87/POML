---
title: People
permalink: /people/
---

<section class="section" style="margin-top:0;">
  <div class="section-header">
    <h1>People</h1>
  </div>

  {% assign principal_investigator_role = site.people | where: 'role', 'Principal Investigator' | where_exp: 'person', "person.template != true" %}
  {% assign faculty_role = site.people | where: 'role', 'Faculty' | where_exp: 'person', "person.template != true" %}
  {% assign principal_investigator = principal_investigator_role | concat: faculty_role | sort: 'order' %}
  {% assign graduate_students = site.people | where: 'role', 'Graduate Students' | where_exp: 'person', "person.template != true" | sort: 'order' %}
  {% assign undergraduate_students = site.people | where: 'role', 'Undergraduate Students' | where_exp: 'person', "person.template != true" | sort: 'order' %}

  {% if principal_investigator.size > 0 %}
  <h2>Principal Investigator</h2>
  <div class="people-grid" style="margin-bottom:1.2rem;">
    {% for member in principal_investigator %}
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
  {% endif %}

  {% if graduate_students.size > 0 %}
  <h2>Graduate Students</h2>
  <div class="people-grid" style="margin-bottom:1.2rem;">
    {% for member in graduate_students %}
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
  {% endif %}

  {% if undergraduate_students.size > 0 %}
  <h2 class="undergraduate-heading">Undergraduate Students</h2>
  <div class="people-grid" style="margin-bottom:1.2rem;">
    {% for member in undergraduate_students %}
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
  {% endif %}
</section>
