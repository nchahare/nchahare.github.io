---
title: shear device
description: Design and fabrication of shear device for cell mechanics
importance: 6
category: work
layout: page
img: assets/img/2022-09-03-13-22-54-image.png
---

# Design and fabrication of miniature shear device for cell mechanics

For my master’s thesis, I joined the biomechanics lab of Prof. Namrata Gundiah. One of the focuses of the lab is to understand cell mechanobiology. I designed and fabricated a bioreactor to study the mechanobiological effect of shear stress on cells by monitoring cytoskeletal reorganization and the response of focal adhesion kinase. This project was my first exposure to cell mechanobiology and applied mechanics methods like traction force microscopy and particle velocimetry. It acquainted me with basic cell biology practices and microscopy.

The idea was simple: to probe cells mechanically using shear force and observe their behavior. We chose to build a simple setup where the rotation of a conical plate in fluid would produce uniform shear flow over a large area. We also wanted this system to have the possibility of live imaging.

Cone plate rheometers are typically used to determine the properties of viscoelastic materials. However, we were the first to use them for mechanobiology of adherent cells.

<div class="row justify-content-sm-center">
{% include figure.html path="assets/img/2022-09-03-13-22-54-image.png" title="Cone plate rheometers" class="img-fluid rounded z-depth-1" %}
</div>
<br>

The calculation of the shear stress in the fluid can be approximated by using Newton’s law of viscosity

$$
\tau = \mu \frac{V}{h} = \mu \frac{\Omega r}{r tan(\beta) + c_o}
$$

By assuming very small gap and small angle:

$$
\tau = \mu \frac{\Omega}{\beta}
$$

For me, the challenge was to work with the practical aspects of the device. There were two sides to this

1. Mechanical fabrication
2. Electrical components

## Mechanical Fabrication

We designed the device with extensive use of SolidWorks. The device consists of a cone plate, the motor housing, a live cell chamber, a microscope stage, a microscope mount, and a stage for moving the cone.

<div class="row justify-content-sm-center">
{% include figure.html path="assets/img/2022-09-03-13-29-34-image.png" title="Cone plate rheometers" class="img-fluid rounded z-depth-1" %}
</div>
<br>

The interesting part of the setup was the cone. First, the fabrication has to be smooth and accurate enough to produce a constant angle. The mechanical workshop of the Raman Research Institute did the fantastic work. We had a cone with a roughness of $0.8 \mu m$.

Second, the cell substrate has to be exactly parallel to the cone plate. We had to go to extra lengths to match the tilt. We would focus on different parts of the cone and use the alignment stage.

<div class="row justify-content-sm-center">
{% include figure.html path="assets/img/2022-09-03-13-33-34-image.png" title="Cone plate rheometers" class="img-fluid rounded z-depth-1" %}
</div>
<br>


## Electrical components

We needed a motor that could spin fast and not wobble. Consider noisy fans; the faster you spin, the more you vibrate. On the suggestion of Prof. Pramod Pullarkat, we decided to go with the BLDC motor from the old hard drives. It is compact , light, and doesn't wobble.

These hard drives are designed to run at a certain fixed speed and voltage. Thus, we used an electronic speed controller (ESC) with a pulse width modulation signal to control the speed. Here, a function generator could produce a wave between 0 and 5V, making the motor spin at different speeds.

<div class="row justify-content-sm-center">
{% include figure.html path="assets/img/2022-09-03-13-48-18-image.png" title="Cone plate rheometers" class="img-fluid rounded z-depth-1" %}
</div>
<br>

To measure the speed, we used an infrared sensor next to the motor. For this, I had to learn Arduino UNO. I designed a GUI program in MATLAB to have live data analysis. We could use the MATLAB interface to program different speed protocols and monitor the results.

## Results

At the end of my masters thesis, I had the device ready and working. Unfortunately, I could not perform any experiments on this myself. We registered for the Indian patent.

<div class="row justify-content-sm-center">
{% include figure.html path="assets/img/2022-09-03-13-50-33-image.png" title="Cone plate rheometers" class="img-fluid rounded z-depth-1" %}
</div>
<br>

Pullarkat, P., Vishwakarma, R., Gundiah, N., and **Chahare, N. R.**, [A microscope mountable fluid shear device](http://ipindia.gov.in/writereaddata/Portal/IPOJournal/1_2591_1/Part-1.pdf). Indian patent, IN201641029893A, pg 275/677 Published 2018-03-09.

I was very pleased to see interesting results using my share device. My colleague Neha Paddillaya used the device to understand cell adhesion strength and cellular invasiveness. In this study, she would step by step increase the pressure and count the cells attached to a region. She found that cell invasiveness is correlated to cell adhesion strength, which could be useful in cancer diagnostics.

Paddillaya, N., Ingale, K., Gaikwad, C., Saini, D. K., Pullarkat, P., Kondaiah, P., ... & Gundiah, N. (2022). [Cell adhesion strength and tractions are mechano-diagnostic features of cellular invasiveness](https://pubs.rsc.org/en/content/articlelanding/2022/SM/D2SM00015F). *Soft Matter*, *18*(23), 4378-4388.

<div class="row justify-content-sm-center">
{% include figure.html path="assets/img/2022-09-03-13-56-46-image.png" title="Cone plate rheometers" class="img-fluid rounded z-depth-1" %}
</div>
<br>
