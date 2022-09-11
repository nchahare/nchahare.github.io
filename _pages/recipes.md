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
  <div class="container">
    <div class="row row-cols-3">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- endfor %}
</div>
