---
layout: default
title: Portfolio
---

<section class="hero">
  <div class="hero__content">
    <p class="eyebrow">Portfolio</p>
    <h1>Interactive projects, prototypes, and digital experiments.</h1>
    <p class="lead">
      This site is built so each project can live in its own Markdown file, with images and short videos stored in a resource folder inside <code>assets/resources/</code>.
    </p>
    <div class="hero__actions">
      <a class="button" href="#projects">Browse projects</a>
      <a class="button button--secondary" href="https://github.com/akris19">View GitHub</a>
    </div>
  </div>
</section>

<section class="section" id="projects">
  <div class="section__intro">
    <p class="eyebrow">Selected Work</p>
    <h2>Projects</h2>
    <p>Every card below is generated from the <code>_projects</code> collection, so adding a new Markdown file creates a new project page automatically.</p>
  </div>

  {% assign projects = site.projects | sort: "order" %}
  {% if projects.size > 0 %}
  <div class="project-grid">
    {% for project in projects %}
    <a class="project-card" href="{{ project.url | relative_url }}">
      <div class="project-card__meta">
        <span>{{ project.year | default: "Project" }}</span>
        {% if project.status %}
        <span>{{ project.status }}</span>
        {% endif %}
      </div>
      <h3>{{ project.title }}</h3>
      <p>{{ project.summary | default: project.excerpt | strip_html | truncate: 180 }}</p>
      {% if project.technologies %}
      <p class="project-card__tech">{{ project.technologies }}</p>
      {% endif %}
    </a>
    {% endfor %}
  </div>
  {% else %}
  <p>No projects are published yet.</p>
  {% endif %}
</section>

<section class="section section--split" id="about">
  <div class="section__intro">
    <p class="eyebrow">About This Setup</p>
    <h2>Markdown-driven portfolio</h2>
  </div>
  <div class="notes">
    <p>Create project pages in <code>_projects/your-project.md</code> with front matter like title, year, summary, and technologies.</p>
    <p>Store images and videos in <code>assets/resources/your-project/</code>, then embed them directly inside the Markdown page.</p>
    <p>This keeps GitHub Pages simple: content in Markdown, layout in Jekyll, and media in one predictable folder structure.</p>
  </div>
</section>
