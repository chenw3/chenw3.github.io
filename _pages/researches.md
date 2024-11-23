---
layout: page
title: Research
permalink: /researches/
description: With the rapid development of micro-nano processing technology centered on photolithography, the gate length of transistors in integrated circuits has gradually decreased to the same order of magnitude as the average mean free path of energy carriers (such as phonons and electrons), invalidating the macroscopic description of thermal conduction phenomena based on Fourier's law. Meanwhile, recent advances in simulation tools (first-principles calculations, machine learning potentials, Boltzmann transport equation, molecular dynamics, etc.) have led to new insights into phonon transport and scattering mechanisms. In this context, we aim to conduct in-depth theoretical research on anharmonic phonon behavior at finite temperatures to address the challenges encountered by the traditional theoretical framework based on the lowest-order perturbation method plus linear Boltzmann transport equation in dealing with complex systems such as non-periodic lattices, inter-band quantum tunneling effects and higher-order strong anharmonicity, to better understand and manipulate the microscopic flow of energy.
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
