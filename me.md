---
layout: default
title: Nimesh Chahare, Ph.D.
description: This is how I look
permalink: /me/
images:
  - /assets/img/meme2024.jpg

---

{% if page.images %}
  <div class="image-container">
    {% for image in page.images %}
      <img src="{{ site.baseurl }}{{ image }}">
    {% endfor %}
  </div>
{% endif %}
