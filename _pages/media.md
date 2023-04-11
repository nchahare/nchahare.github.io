---
layout: page
title:  media
nav: true
nav_order: 5
description: highlights of my projects in pictures
---

There is always more than meets the eye. I am not just an engineer. I have other interests, like cooking, learning new things, making origami. Here you can see pictures related to my work or random things I do on this part of the internet.

{% assign image_folder = 'assets/gal' %}
{% assign row_size = 3 %}

<style>
  .gallery-image {
    width: 100%;
    height: auto;
    object-fit: cover;
  }
</style>

<div class="container">
  {% assign images_in_folder = site.static_files | where_exp: "file", "file.path contains image_folder" %}
  {% for file in images_in_folder %}
    {% assign column = forloop.index0 | modulo: row_size %}
    {% if column == 0 %}
      <div class="row mt-3">
    {% endif %}
        <div class="col-md-4 mt-3 mt-md-0">
          {% include figure.html src="{{ file.path }}" alt="" class="img-fluid rounded z-depth-1 gallery-image" zoomable=true }
        </div>
    {% if column == row_size | minus: 1 or forloop.last %}
      </div>
    {% endif %}
  {% endfor %}
</div>