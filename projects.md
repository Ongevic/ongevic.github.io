---
layout: default
title: "Research Projects"
---

<div class="page-header">
  <div class="container">
    <h1>Research Projects</h1>
    <p>Current and completed research projects in theoretical syntax, language acquisition, and experimental linguistics.</p>
  </div>
</div>

<section class="section">
  <div class="container">
    <div class="projects-grid">
      {% for project in site.projects %}
      <div class="project-card">
        <div class="project-content">
          <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
          <p class="project-excerpt">{{ project.excerpt }}</p>
          <div class="project-meta">
            <span class="project-date">{{ project.date | date: "%Y" }}</span>
          </div>
          <a href="{{ project.url }}" class="read-more">Learn More →</a>
        </div>
      </div>
      {% endfor %}
    </div>
  </div>
</section>

<style>
.page-header {
    background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
    color: white;
    padding: 4rem 0;
    text-align: center;
}

.page-header h1 {
    margin: 0 0 1rem 0;
    font-size: 2.5rem;
}

.page-header p {
    margin: 0;
    font-size: 1.1rem;
    opacity: 0.9;
}

.projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    gap: 2rem;
    margin-top: 2rem;
}

.project-card {
    background: var(--card-bg);
    border-radius: 12px;
    padding: 2rem;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    border: 1px solid var(--border-color);
}

.project-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
}

.project-content h3 {
    margin: 0 0 1rem 0;
    color: var(--primary-color);
}

.project-content h3 a {
    color: inherit;
    text-decoration: none;
}

.project-content h3 a:hover {
    color: var(--secondary-color);
}

.project-excerpt {
    color: var(--text-secondary);
    line-height: 1.6;
    margin-bottom: 1.5rem;
}

.project-meta {
    margin-bottom: 1.5rem;
}

.project-date {
    background: var(--primary-color);
    color: white;
    padding: 0.25rem 0.75rem;
    border-radius: 20px;
    font-size: 0.85rem;
    font-weight: 500;
}

.read-more {
    color: var(--primary-color);
    text-decoration: none;
    font-weight: 600;
    transition: color 0.2s ease;
}

.read-more:hover {
    color: var(--secondary-color);
}
</style>
