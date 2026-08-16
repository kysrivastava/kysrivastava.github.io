---
layout: page
title: "Projects"
permalink: /projects/
nav: true
nav_order: 3
description: A small set of engineering projects in retrieval, agent workflows, and research-adjacent tooling.
---

{% assign sorted_projects = site.projects | sort: "importance" %}

<div class="row row-cols-1 row-cols-md-3">
  {% for project in sorted_projects %}
    <div class="col mb-4">
      <a href="{% if project.redirect %}{{ project.redirect }}{% else %}{{ project.url | relative_url }}{% endif %}">
        <div class="card h-100 hoverable">
          <div class="card-body">
            <h3 class="card-title">{{ project.title }}</h3>
            <p class="card-text">{{ project.description }}</p>
            {% if project.github %}
              <p class="card-text"><small>{{ project.github }}</small></p>
            {% endif %}
          </div>
        </div>
      </a>
    </div>
  {% endfor %}
</div>
