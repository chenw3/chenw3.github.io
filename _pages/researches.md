---
layout: page
title: Research
permalink: /researches/
description: Dr. Wang's current research focuses on developing and implementing first-principles-based methods and machine-learning approaches to simulate the dynamics of phonons and electrons at the atomic level and their application to thermal management. Research topics include heat transport phenomena, anharmonic lattice dynamics, and structural phase transition for energy-converting materials, covering perovskites, thermoelectrics, and superionic conductors.
nav: true
nav_order: 5
# display_categories: []
horizontal: true
---

<!-- pages/research.md -->
<div class="projects">

<!-- Display projects without categories -->

{% assign sorted_projects = site.researches | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

 
<div class="cw-research-projects-wrap">
    {% for project in sorted_projects %}
      {% include researches_horizontal.liquid %}
    {% endfor %}
</div>
 
{% else %}
  <div class="grid">
    {% for project in sorted_projects %}
      {% include researches.liquid %}
    {% endfor %}
  </div>
{% endif %}

</div>
