---
layout: default
title: Fareed Dubiure - Portfolio
permalink: /projects/
---

<div class="project-gallery">
  {% for project in site.projects %}
    <div class="gallery-item">
      <a href="{{ project.url | relative_url }}">
        <img src="{{ project.image | relative_url }}" alt="{{ project.title }}">
        <p>{{ project.title }}</p>
      </a>
      {% if project.excerpt %}
      <p class="gallery-excerpt">{{ project.excerpt }}</p>
      {% endif %}
    </div>
  {% endfor %}
</div>
