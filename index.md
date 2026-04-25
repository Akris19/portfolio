---
layout: default
title: Portfolio
---

<section class="section" id="projects">
  <div class="section__intro">
    <h2>Projects</h2>
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
