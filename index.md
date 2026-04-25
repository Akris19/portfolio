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
    <p>Each project card opens inline, so visitors can browse the work without leaving the portfolio overview.</p>
  </div>

  {% assign projects = site.projects | sort: "order" %}
  {% if projects.size > 0 %}
  <div class="project-grid">
    {% for project in projects %}
    {% assign modal_id = 'project-modal-' | append: forloop.index %}
    <button class="project-card" type="button" data-modal-target="{{ modal_id }}" aria-haspopup="dialog" aria-controls="{{ modal_id }}">
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
      <span class="project-card__cta">Open project</span>
    </button>
    {% endfor %}
  </div>

  {% for project in projects %}
  {% assign modal_id = 'project-modal-' | append: forloop.index %}
  <div class="project-modal" id="{{ modal_id }}" hidden>
    <div class="project-modal__backdrop" data-modal-close></div>
    <div class="project-modal__dialog" role="dialog" aria-modal="true" aria-labelledby="{{ modal_id }}-title">
      <button class="project-modal__close" type="button" aria-label="Close project" data-modal-close>&times;</button>

      <div class="project-modal__inner">
        <header class="project-modal__header">
          {% if project.year %}
          <p class="eyebrow">{{ project.year }}</p>
          {% endif %}

          <h3 id="{{ modal_id }}-title">{{ project.title }}</h3>

          {% if project.summary %}
          <p class="project-modal__summary">{{ project.summary }}</p>
          {% endif %}

          <div class="project-modal__facts">
            {% if project.role %}
            <p><strong>Role</strong> {{ project.role }}</p>
            {% endif %}
            {% if project.status %}
            <p><strong>Status</strong> {{ project.status }}</p>
            {% endif %}
            {% if project.technologies %}
            <p><strong>Tools</strong> {{ project.technologies }}</p>
            {% endif %}
          </div>
        </header>

        {% if project.cover %}
        <figure class="project-modal__cover">
          <img src="{{ project.cover | relative_url }}" alt="{{ project.title }} cover image">
        </figure>
        {% endif %}

        <div class="project-modal__content">
          {{ project.content }}
        </div>
      </div>
    </div>
  </div>
  {% endfor %}
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
    <p><a class="button button--secondary" href="{{ '/about/' | relative_url }}">Open full About page</a></p>
  </div>
</section>
