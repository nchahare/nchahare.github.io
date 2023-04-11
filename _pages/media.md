---
layout: page
title:  media
nav: true
nav_order: 5
description: highlights of my projects in pictures
---

There is always more than meets the eye. I am not just an engineer. I have other interests, like cooking, learning new things, making origami. Here you can see pictures related to my work or random things I do on this part of the internet.

{% assign image_folder = 'assets/img' %}
{% assign row_size = 3 %}

<div class="row mt-3">
{% for file in site.static_files %}
  {% if file.path contains image_folder %}
    {% if forloop.index0 % row_size == 0 and forloop.index0 != 0 %}
    </div><div class="row mt-3">
    {% endif %}
    <div class="col-sm mt-3 mt-md-0">
      {% include figure.html path=file.path class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
  {% endif %}
{% endfor %}
</div>
