---
layout: page
title: Projects
---

<div class="projects-grid">
  {% assign sorted_projects = site.projects | sort: 'date' | reverse %}
  {% for project in sorted_projects %}
    <div class="project-card">
      <a href="{{ project.url | relative_url }}">
        {% if project.image %}
          <img src="{{ site.baseurl }}/public/assets/projects/{{ project.image }}" alt="{{ project.title }}">
        {% endif %}
        <h3>{{ project.title }}</h3>
        {% if project.date %}
          <span class="project-year">({{ project.date | date: "%Y" }})</span>
        {% endif %}
      </a>
    </div>
  {% endfor %}
</div>

<style>
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.project-card {
  border: 1px solid #eee;
  border-radius: 8px;
  overflow: hidden;
  transition: transform 0.2s, box-shadow 0.2s;
}

.project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.15);
}

.project-card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  margin: 0;
}

.project-card h3 {
  margin: 1rem 1rem 0.5rem 1rem;
  color: #303030;
}

.project-year {
  color: #999;
  font-size: 0.9rem;
  margin-left: 1rem;
  margin-bottom: 1rem;
  display: block;
}

.project-card a {
  text-decoration: none;
  color: inherit;
  display: block;
}
</style>
