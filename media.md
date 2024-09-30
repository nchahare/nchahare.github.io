---
layout: default
title: media
description: There is always more than meets the eye. I am not just an engineer. I have other interests, like cooking, learning new things, making origami. Here you can see pictures related to my work or random things I do on this part of the internet.

images:
  - image_path: ../assets/img/meme.jpg
    title: Apple Pie
  - image_path: ../assets/img/mewithme.jpg
    title: Birthday Cake
---


<ul class="media">
  {% for image in page.images %}
    <img src="{{ image.image_path }}" alt="{{ image.title}}"/>
  {% endfor %}
</ul>