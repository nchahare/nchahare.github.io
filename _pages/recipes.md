---
layout: page
title: Cook book
permalink: /recipes/
description: A collection of my recipes
nav: false
nav_order: 4
display_categories: [work]
horizontal: false
---

<!-- pages/projects.md -->
<div class="recipes">
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  {%- assign categorized_projects = site.recipes %}
  {%- assign sorted_projects = categorized_projects %}
  <!-- Generate cards for each project -->

  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endfor %}
</div>
