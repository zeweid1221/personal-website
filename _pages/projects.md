---
layout: page
title: Research
permalink: /projects/
description: Selected research on trustworthy generative AI, sequential modeling, and robust statistical inference.
nav: true
nav_order: 3
display_categories: [research]
horizontal: false
---

<style>
  .research-project-grid > .col {
    margin-bottom: 1.5rem;
  }

  .research-project-grid .card {
    min-height: 230px;
    overflow: hidden;
  }

  .research-project-grid .card:has(figure) {
    display: grid;
    grid-template-columns: minmax(250px, 40%) minmax(0, 60%);
  }

  .research-project-grid .card figure {
    grid-column: 2;
    grid-row: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    min-width: 0;
    min-height: 230px;
    margin: 0;
    padding: 1.25rem;
    background: #fff;
    border-left: 1px solid var(--global-divider-color);
  }

  .research-project-grid .card picture {
    display: flex;
    width: 100%;
    height: 190px;
    align-items: center;
    justify-content: center;
  }

  .research-project-grid .card .card-img-top {
    width: 100%;
    height: 100%;
    object-fit: contain;
  }

  .research-project-grid .card:has(figure) .card-body {
    grid-column: 1;
    grid-row: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .research-project-grid .card:not(:has(figure)) {
    min-height: auto;
  }

  @media (max-width: 767.98px) {
    .research-project-grid .card:has(figure) {
      display: flex;
      flex-direction: column;
    }

    .research-project-grid .card figure {
      width: 100%;
      min-height: 190px;
      padding: 1rem;
      border-bottom: 1px solid var(--global-divider-color);
      border-left: 0;
    }

    .research-project-grid .card picture {
      height: 160px;
    }
  }
</style>

<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 research-project-grid">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 research-project-grid">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
