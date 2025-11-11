---
layout: page
title: Projects
---

<div class="projects-grid">
  {% for project in site.projects %}
    <div class="project-card">
      <a href="{{ project.url | relative_url }}">
        {% if project.image %}
          <img src="{{ site.baseurl }}/_projects/images/{{ project.image }}" alt="{{ project.title }}">
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
}

.project-card p {
  margin: 0.5rem 1rem 1rem 1rem;
  color: #666;
  font-size: 0.9rem;
}

.project-card a {
  text-decoration: none;
  color: inherit;
  display: block;
}
</style>
