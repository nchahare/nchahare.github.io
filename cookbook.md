---
layout: default
title: Fresh, Canned, and Frozen
description: Nimesh's cookbook
permalink: /cookbook/
---


{%- if site.recipes.size > 0 -%}
  <ul>
    {%- for recipe in site.recipes -%}
      <p>
        {%- assign date_format = "%Y-%m-%d" -%}
        {{ recipe.date | date: date_format }} <a href="{{ recipe.url | relative_url }}">{{ recipe.title | escape }}</a>
      </p>
    {%- endfor -%}
  </ul>
{%- endif -%}
