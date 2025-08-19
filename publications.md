---
layout: default
title: "Publications"
---

<div class="page-header">
  <div class="container">
    <h1>Publications</h1>
    <p>Academic publications in theoretical syntax, language acquisition, and experimental linguistics.</p>
  </div>
</div>

<section class="section">
  <div class="container">
    <div class="publications-list">
      {% for publication in site.publications %}
      <div class="publication-item">
        <div class="publication-content">
          <h3><a href="{{ publication.url }}">{{ publication.title }}</a></h3>
          <p class="authors">{{ publication.authors }}</p>
          <p class="venue">{{ publication.venue }}, {{ publication.year }}</p>
          {% if publication.doi %}
          <a href="https://doi.org/{{ publication.doi }}" class="doi-link" target="_blank">DOI</a>
          {% endif %}
          <a href="{{ publication.url }}" class="read-more">Read Abstract →</a>
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

.publications-list {
    max-width: 900px;
    margin: 0 auto;
}

.publication-item {
    background: var(--card-bg);
    border-radius: 12px;
    padding: 2rem;
    margin-bottom: 2rem;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    border: 1px solid var(--border-color);
}

.publication-item:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
}

.publication-content h3 {
    margin: 0 0 1rem 0;
    color: var(--primary-color);
}

.publication-content h3 a {
    color: inherit;
    text-decoration: none;
}

.publication-content h3 a:hover {
    color: var(--secondary-color);
}

.authors {
    font-weight: 600;
    color: var(--text-color);
    margin-bottom: 0.5rem;
}

.venue {
    color: var(--text-secondary);
    font-style: italic;
    margin-bottom: 1rem;
}

.doi-link {
    display: inline-block;
    background: var(--primary-color);
    color: white;
    padding: 0.5rem 1rem;
    border-radius: 6px;
    text-decoration: none;
    font-size: 0.9rem;
    margin-right: 1rem;
    transition: background-color 0.2s ease;
}

.doi-link:hover {
    background: var(--secondary-color);
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