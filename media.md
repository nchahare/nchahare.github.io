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
      <a href="#" onclick="openLightbox('{{ site.baseurl }}{{ image }}')">
        <img src="{{ site.baseurl }}{{ image }}" alt="Nimesh Chahare" />
      </a>
    </div>
  {% endfor %}
</div>

<!-- Lightbox container -->
<div id="lightbox" style="display:none;">
  <span class="close">&times;</span>
  <img class="lightbox-content" id="lightbox-image">
  <div id="caption"></div>
</div>

<script>
function openLightbox(imageSrc) {
  document.getElementById('lightbox').style.display = 'block';
  document.getElementById('lightbox-image').src = imageSrc;
}

document.getElementById('lightbox').addEventListener('click', (e) => {
  if (e.target === document.getElementById('lightbox')) {
    closeLightbox();
  }
});

document.querySelector('.close').addEventListener('click', closeLightbox);

function closeLightbox() {
  document.getElementById('lightbox').style.display = 'none';
}
</script>

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

  /* New styles for lightbox */
  #lightbox {
    position: fixed;
    z-index: 9999;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0,0,0,0.8);
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  #lightbox img {
    max-width: 90%;
    max-height: 80%;
    margin-top: calc(50vh - 40vh); /* Calculate vertical center */
  }

  .close {
    color: white;
    font-size: 35px;
    font-weight: bold;
    position: absolute;
    top: 15px;
    right: 35px;
    cursor: pointer;
  }

  #caption {
    margin-top: 15px;
    color: white;
  }
</style>