---
layout: page
title: Nimesh's Cookbook
permalink: /recipes/
description: A collection of my recipes
nav: false
snav_order: 4
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
    <div class="row row-cols-3">
    {%- for project in sorted_projects -%}
      {% include recipes_horizontal.html %}
    {%- endfor %}
    </div>
  </div>

  <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSfxl9Xn2-x-xiScF0fY5EtmX2STObeRe8U_jl5MliHTToftLQ/viewform?embedded=true" width="360" height="407" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>

  {%- endfor %}
</div>
