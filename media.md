---
layout: default
title: media
description: The closest thing to my Instagram you'll ever encounter
permalink: /media/
images:
  - /assets/img/meme2024.jpg
  - /assets/img/organicorigami.jpg
  - /assets/img/bcc1.jpg
  - /assets/img/phddefense.jpg
  - /assets/img/thesiscover.png
  - /assets/img/1702570033758.jpg
  - /assets/img/GBFPAUbX0AAyBXM.jpg
  - /assets/img/pfm1.png
  - /assets/img/pfm2.png
  - /assets/img/image1117_dresden.png
  - /assets/img/misti.png
  - /assets/img/firenze.jpg
  - /assets/img/v1h64o.jpg
  - /assets/img/catcat.jpg
  - /assets/img/mewithme.jpg
  - /assets/img/IMG_20230110_202613.jpg
  - /assets/img/IMG_20230221_185347.jpg
  - /assets/img/birdsandboats.jpg
  - /assets/img/epimechfc.png
  - /assets/img/meatmuseum.jpg
  - /assets/img/roseinapot.jpg
  - /assets/img/pear.jpg
  - /assets/img/rosalind.jpg
  - /assets/img/ricardo.jpg
  - /assets/img/lizard.jpg
  - /assets/img/smallelephant.jpg
  - /assets/img/lions.jpg
  - /assets/img/btechmachine.jpg
---
<div class="gallery">
  {% for image in page.images %}
    <div class="gallery-item">
      <a href="{{ site.baseurl }}{{ image }}">
        <img src="{{ site.baseurl }}{{ image }}" alt="Nimesh Chahare" />
      </a>
    </div>
  {% endfor %}
</div>

<style>
  /* Existing styles */
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
    aspect-ratio: 1/1;
    object-fit: cover;
    transition: transform 0.5s ease-in-out;
  }
  
  .gallery-item:hover img {
    transform: scale(1.1);
  }

</style>