---
layout: default
title: media
description: The closest thing to my Instagram you'll ever encounter
images:
  - /assets/img/meme2024.jpg
  - /assets/img/organicorigami.jpg
  - /assets/img/phddefense.jpg
  - /assets/img/bcc1.jpg
  - /assets/img/mewithme.jpg
  - /assets/img/btechmachine.jpg

---

<div class="gallery">
  {% for image in page.images %}
    <div class="gallery-item">
      <img src="{{ site.baseurl }}{{ image }}" alt="Gallery Image" />
    </div>
  {% endfor %}
</div>

<style>
  .gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 10px;
  }
  
  .gallery-item {
    overflow: hidden;
  }
  
  .gallery-item img {
    width: 100%;
    height: auto;
    transition: transform 0.5s ease-in-out;
  }
  
  .gallery-item:hover img {
    transform: scale(1.1);
  }
</style>
