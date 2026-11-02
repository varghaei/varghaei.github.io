---
layout: page
title: research
permalink: /research/
description: Research areas in computer vision, biometrics, and generative AI.
nav: true
nav_order: 2
---

<!-- pages/projects.md -->
<div class="projects">
{% assign sorted_projects = site.projects | sort: "importance" %}
  <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
</div>
