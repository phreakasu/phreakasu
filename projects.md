---
layout: page
title: Projects
---

<div class="projects-grid">
  {% for project in site.projects %}
    <div class="project-card">
      <a href="{{ project.url | relative_url }}">
        {% if project.image %}
          <img src="{{ site.baseurl }}/assets/images/{{ project.image }}" alt="{{ project.title }}">
        {% endif %}
        <h3>{{ project.title }}</h3>
        {% if project.date %}
          <span class="project-year">({{ project.date | date: "%Y" }})</span>
        {% endif %}
        {% if project.excerpt %}
          <p>{{ project.excerpt }}</p>
        {% endif %}
      </a>
    </div>
  {% endfor %}
</div>
