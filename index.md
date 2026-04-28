---
layout: default
title: Portfolio
---

<section class="section" id="projects">
  <div class="section__intro">
    <h2>Projects</h2>
  </div>

  {% assign all_projects = site.projects | sort: "order" %}
  {% assign upcoming_projects = "" | split: "" %}
  {% assign published_projects = "" | split: "" %}
  {% for project in all_projects %}
    {% if project.status == "Upcoming" or project.upcoming == true %}
      {% assign upcoming_projects = upcoming_projects | push: project %}
    {% else %}
      {% assign published_projects = published_projects | push: project %}
    {% endif %}
  {% endfor %}
  {% if all_projects.size > 0 %}
  <div class="project-grid">
    {% for project in published_projects %}
    {% assign modal_id = 'project-modal-published-' | append: forloop.index %}
    <button class="project-card" type="button" data-modal-target="{{ modal_id }}" aria-haspopup="dialog" aria-controls="{{ modal_id }}">
      {% if project.cover %}
      <figure class="project-card__cover">
        <img src="{{ project.cover | relative_url }}" alt="{{ project.title }} cover image">
      </figure>
      {% endif %}

      <div class="project-card__meta">
        <span>{{ project.year | default: "Project" }}</span>
        {% if project.status %}
        <span>{{ project.status }}</span>
        {% endif %}
      </div>
      <h3>{{ project.title }}</h3>
      <p>{{ project.summary | default: project.excerpt | strip_html | truncate: 180 }}</p>
      <span class="project-card__cta">Open project</span>
    </button>
    {% endfor %}
  </div>
  {% else %}
  <p>No projects are published yet.</p>
  {% endif %}
</section>

{% if upcoming_projects.size > 0 %}
<section class="section" id="upcoming-projects">
  <div class="section__intro">
    <h2>Upcoming Projects</h2>
    <p>Work in progress, early concepts, and projects that are still under development.</p>
  </div>

  <div class="project-grid">
    {% for project in upcoming_projects %}
    {% assign modal_id = 'project-modal-upcoming-' | append: forloop.index %}
    <button class="project-card project-card--upcoming" type="button" data-modal-target="{{ modal_id }}" aria-haspopup="dialog" aria-controls="{{ modal_id }}">
      {% if project.cover %}
      <figure class="project-card__cover">
        <img src="{{ project.cover | relative_url }}" alt="{{ project.title }} cover image">
      </figure>
      {% endif %}

      <div class="project-card__meta">
        <span>{{ project.year | default: "Upcoming" }}</span>
        <span>{{ project.status | default: "Upcoming" }}</span>
      </div>
      <h3>{{ project.title }}</h3>
      <p>{{ project.summary | default: project.excerpt | strip_html | truncate: 180 }}</p>
      <span class="project-card__cta">Open project</span>
    </button>
    {% endfor %}
  </div>
</section>
{% endif %}

{% for project in published_projects %}
{% assign modal_id = 'project-modal-published-' | append: forloop.index %}
<div class="project-modal" id="{{ modal_id }}" hidden>
  <div class="project-modal__backdrop" data-modal-close></div>
  <div class="project-modal__dialog" role="dialog" aria-modal="true" aria-labelledby="{{ modal_id }}-title">
    <button class="project-modal__close" type="button" aria-label="Close project" data-modal-close>&times;</button>

    <div class="project-modal__inner">
      <header class="project-modal__header">
        {% if project.technologies %}
        <p class="project-tech-line"><strong>Technologies:</strong> {{ project.technologies }}</p>
        {% endif %}

        {% if project.status %}
        <p class="eyebrow">{{ project.status }}</p>
        {% endif %}

        {% if project.year %}
        <p class="eyebrow">{{ project.year }}</p>
        {% endif %}

        <h3 id="{{ modal_id }}-title">{{ project.title }}</h3>

        {% if project.summary %}
        <p class="project-modal__summary">{{ project.summary }}</p>
        {% endif %}
      </header>

      <div class="project-modal__content">
        {{ project.content }}
      </div>
    </div>
  </div>
</div>
{% endfor %}

{% for project in upcoming_projects %}
{% assign modal_id = 'project-modal-upcoming-' | append: forloop.index %}
<div class="project-modal" id="{{ modal_id }}" hidden>
  <div class="project-modal__backdrop" data-modal-close></div>
  <div class="project-modal__dialog" role="dialog" aria-modal="true" aria-labelledby="{{ modal_id }}-title">
    <button class="project-modal__close" type="button" aria-label="Close project" data-modal-close>&times;</button>

    <div class="project-modal__inner">
      <header class="project-modal__header">
        {% if project.technologies %}
        <p class="project-tech-line"><strong>Technologies:</strong> {{ project.technologies }}</p>
        {% endif %}

        {% if project.status %}
        <p class="eyebrow">{{ project.status }}</p>
        {% endif %}

        {% if project.year %}
        <p class="eyebrow">{{ project.year }}</p>
        {% endif %}

        <h3 id="{{ modal_id }}-title">{{ project.title }}</h3>

        {% if project.summary %}
        <p class="project-modal__summary">{{ project.summary }}</p>
        {% endif %}
      </header>

      <div class="project-modal__content">
        {{ project.content }}
      </div>
    </div>
  </div>
</div>
{% endfor %}
