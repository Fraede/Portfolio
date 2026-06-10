---
layout: default
title: Fareed Dubiure - Portfolio
permalink: /projects/
---


<div class="gallery-container">

&#x20; <div class="project-gallery">

&#x20;   {% for project in site.projects %}

&#x20;     <div class="gallery-item">

&#x20;       <a href="{{ project.url | relative\_url }}">

&#x20;         <img src="{{ project.image | relative\_url }}" alt="{{ project.title }}" />

&#x20;         <p>{{ project.title }}</p>

&#x20;       </a>

&#x20;     </div>

&#x20;   {% endfor %}

&#x20; </div>

</div>

