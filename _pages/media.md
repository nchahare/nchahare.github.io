---
layout: page
title:  media
nav: true
nav_order: 5
description: highlights of my projects in pictures
---

There is always more than meets the eye. I am not just an engineer. I have other interests, like cooking, learning new things, making origami. Here you can see pictures related to my work or random things I do on this part of the internet.

{% assign image_folder = "assets/gal/" %}

{% comment %} 
Get a list of all image files in the folder, sorted by filename
{% endcomment %}
{% assign image_files = site.static_files | where: "path", image_folder | where_exp: "file", "file.extname == '.jpg' or file.extname == '.jpeg' or file.extname == '.png' | sort: "name" %}

{% comment %} 
Group the image files into rows of three
{% endcomment %}
{% assign row_size = 3 %}
{% assign num_rows = image_files | size | divided_by: row_size %}

{% comment %} 
Loop through the rows and generate the columns for each row
{% endcomment %}
{% for i in (0..num_rows) %}
  <div class="row mt-3">
    {% for j in (0..row_size-1) %}
      {% assign index = i*row_size + j %}
      {% if index < image_files | size %}
        <div class="col-sm mt-3 mt-md-0">
          {% include figure.html path=image_files[index].path %}
        </div>
      {% endif %}
    {% endfor %}
  </div>
{% endfor %}
