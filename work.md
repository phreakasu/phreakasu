---
layout: page
title: Work
---

<div class="work-sections-grid">
  <div class="work-card">
    <a href="/work/projects">
      <div class="work-icon">🔧</div>
      <h3>Projects</h3>
      <p>Engineering projects</p>
    </a>
  </div>

  <div class="work-card">
    <a href="/work/research">
      <div class="work-icon">🔬</div>
      <h3>Research</h3>
      <p>Academic research and publications</p>
    </a>
  </div>
</div>

<style>
.work-sections-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 320px));
  gap: 2rem;
  margin: 2rem 0;
  justify-content: start;
}

.work-card {
  border: 1px solid #eee;
  border-radius: 8px;
  padding: 2rem;
  transition: transform 0.2s, box-shadow 0.2s;
  text-align: center;
}

.work-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.15);
}

.work-icon {
  font-size: 3rem;
  margin-bottom: 1rem;
}

.work-card h3 {
  margin: 0.5rem 0;
  color: #303030;
}

.work-card p {
  color: #666;
  margin: 0.5rem 0 0 0;
  font-size: 0.9rem;
}

.work-card a {
  text-decoration: none;
  color: inherit;
  display: block;
}
</style>
