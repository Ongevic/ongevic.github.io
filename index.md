---
layout: default
title: "Home"
---

<div class="hero-section">
  <div class="container">
    <div class="hero-content">
      <img src="{{ site.baseurl }}/assets/images/profile.jpg" alt="Your Name" class="profile-image">
      <h1>Your Name</h1>
      <p class="subtitle">Research Scientist | Your Field</p>
      <p class="description">
        Welcome to my research website! I'm passionate about [your research area] 
        and currently working on [brief description of current work].
      </p>
      <div class="hero-buttons">
        <a href="#research" class="btn btn-primary">View Research</a>
        <a href="#publications" class="btn btn-secondary">Publications</a>
        <a href="#contact" class="btn btn-outline">Contact Me</a>
      </div>
    </div>
  </div>
</div>

<section id="about" class="section">
  <div class="container">
    <h2>About Me</h2>
    <div class="about-content">
      <div class="about-text">
        <p>
          I am a [your position] at [your institution], specializing in [your research areas]. 
          My work focuses on [brief description of your research interests and goals].
        </p>
        <p>
          I received my [degree] from [university] in [year], and have been working on 
          [specific research projects or areas] since then.
        </p>
        <div class="research-interests">
          <h3>Research Interests</h3>
          <ul>
            <li>Research Area 1</li>
            <li>Research Area 2</li>
            <li>Research Area 3</li>
            <li>Research Area 4</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="research" class="section">
  <div class="container">
    <h2>Current Research</h2>
    <div class="research-grid">
      {% for project in site.projects limit:3 %}
      <div class="research-card">
        <h3>{{ project.title }}</h3>
        <p>{{ project.excerpt }}</p>
        <a href="{{ project.url }}" class="read-more">Learn More →</a>
      </div>
      {% endfor %}
    </div>
    <div class="text-center">
      <a href="/projects" class="btn btn-primary">View All Projects</a>
    </div>
  </div>
</section>

<section id="publications" class="section">
  <div class="container">
    <h2>Recent Publications</h2>
    <div class="publications-list">
      {% for publication in site.publications limit:5 %}
      <div class="publication-item">
        <h3>{{ publication.title }}</h3>
        <p class="authors">{{ publication.authors }}</p>
        <p class="venue">{{ publication.venue }}, {{ publication.year }}</p>
        {% if publication.doi %}
        <a href="https://doi.org/{{ publication.doi }}" class="doi-link" target="_blank">DOI</a>
        {% endif %}
      </div>
      {% endfor %}
    </div>
    <div class="text-center">
      <a href="/publications" class="btn btn-primary">View All Publications</a>
    </div>
  </div>
</section>

<section id="contact" class="section">
  <div class="container">
    <h2>Contact</h2>
    <div class="contact-info">
      <div class="contact-item">
        <i class="fas fa-envelope"></i>
        <a href="mailto:{{ site.email }}">{{ site.email }}</a>
      </div>
      <div class="contact-item">
        <i class="fab fa-github"></i>
        <a href="https://github.com/yourusername" target="_blank">GitHub</a>
      </div>
      <div class="contact-item">
        <i class="fab fa-linkedin"></i>
        <a href="https://linkedin.com/in/yourusername" target="_blank">LinkedIn</a>
      </div>
      <div class="contact-item">
        <i class="fas fa-map-marker-alt"></i>
        <span>Your Institution, City, Country</span>
      </div>
    </div>
  </div>
</section> 