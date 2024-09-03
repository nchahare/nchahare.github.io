---
layout: default
title: Journal of experimental Nimesh
description: Worlds second best non-peer review journal full of random things
---


{%- if site.posts.size > 0 -%}
  <ul>
    {%- for post in site.posts -%}
      <p>
        {%- assign date_format = "%Y-%m-%d" -%}
        {{ post.date | date: date_format }} <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
      </p>
    {%- endfor -%}
  </ul>
{%- endif -%}
