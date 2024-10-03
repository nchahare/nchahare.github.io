---
layout: default
title: Nimesh Chahare, Ph.D.
description: Nimesh Chahare is a postdoctoral scientist at Columbia University in New York. His research focuses on the intersection of mechanical engineering and developmental biology, specifically exploring the morphogenesis of early embryonic brain.
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
