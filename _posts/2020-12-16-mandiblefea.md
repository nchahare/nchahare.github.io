---
layout: post
title: Cutting mechanics of wood by beetle larval mandibles
description:  The study examined CWSB larval mandibles' biomechanics, providing insights for developing cutting tools and pest control strategies.
date: 2020-12-16
tags: notes
authors:
  - name: Nimesh R. Chahare
    url: "https://nchahare.github.io"
    affiliations:
      name: Indian Institute of Science, Bengaluru

toc:
  - name: Introduction
  - name: Methods
  - name: Results
  - name: Conclusion
---

*Adapted from the published manuscirpt: [Kundanati, L., Chahare, N. R., Jaddivada, S., Karkisaval, A. G., Sridhar, R., Pugno, N. M., & Gundiah, N. (2020). Cutting mechanics of wood by beetle larval mandibles. Journal of the Mechanical Behavior of Biomedical Materials, 112, 104027](https://www.sciencedirect.com/science/article/abs/pii/S1751616120305786?via%3Dihub).*

## Introduction

Wood boring beetles cause significant damage to forests, crops, and timber. The larvae's ability to tunnel inside wood allows them to evade their natural enemies and access a nutritional source with reduced competition. The coffee white stem borer (CWSB), Xylotrechus quadripes, is a major pest that devastates coffee plantations. This study aims to analyze the structure-property relationships of the CWSB larval mandibles and their response to mechanical stresses during wood cutting.

<div class="row justify-content-sm-center">
{% include figure.html path="assets/img/fea11.jpg" alt="fre introduction" caption="A: Scanning electron micrograph of the top of the CWSB mandible sample brings into focus the curved cutting parts of the tip region of the mandible. B: Side view highlights the surface of the mandible and the cutting cuspal edge. C: Zoomed view of the edge region of the mandible demonstrates the tip sharpness measured to be 0.5 micron." %}
</div>

## Methods

In this study, we employed finite element simulations as a crucial method to investigate the biomechanical properties of the CWSB larval mandibles during wood cutting. We first characterized the mandible morphology, composition, and mechanical properties using scanning electron microscopy with X-ray microanalysis, microtomography, and nanoindentation experiments. We also analyzed the wood substrate properties and compared them with the larval mandibles.

To further our understanding, we developed a finite element model of the larval mandible using the information obtained from the previous steps. We applied three different boundary conditions to represent various scenarios during wood cutting: fully pinned, semi pinned, and pivot. These cases allowed us to investigate the load-bearing capability of the mandible, the effects of muscle attachments, and the displacement of the mandible about the hinge axis.

We then analyzed the stress contours on the mandible under these boundary conditions to identify stress distribution patterns and the role of the hollow region in the mandible during wood cutting. Finally, using a scaling model of two indenters cutting through a quasi-brittle wood material, we characterized the relationship between the mandible shape and the chip sizes generated during cutting, which helped us understand the efficiency of the cutting mechanism employed by the larvae.

<div class="row justify-content-sm-center">
{% include figure.html path="assets/img/fea1.jpg" alt="fre introduction" caption="A: Splines were constructed using the microCT results at different heights from the base to the tip of the mandible that were used for constructing a 3D geometrical model B: The model after reconstruction is shown with cross-sectional planes in the tip region corresponding to plane 1 (solid) and a hollow region (plane 2). C: The structure was meshed and divided into the tip (blue), intermediate (red), and base (green) regions of the mandible. D: Surface S1, located at the base of the mandible, corresponded to the attachment of the adductor muscle. This, along with the axis of rotation (M-M′), and the rigid links represented with yellow crosses, were used to impose the pivot boundary condition to compare stress distributions on the mandible. T-T′ refers to the sagittal plane through the mandible. E: A semi pinned boundary condition shows fixed nodes at adductor (S1 surface) and abductor muscle (S2 surface) attachments at the base region of the mandible. F: All nodes at the mandible base (in brown) had zero translational displacements for the fully pinned boundary condition." %}
</div>

## Results

In this study, I conducted finite element simulations to gain insights into the stress distribution and behavior of the CWSB larval mandibles during wood cutting. The X-ray microtomographic three-dimensional reconstruction of the mandible revealed a highly curved and sharp cutting edge with an internally localized conical hollow region. The volume of this hollow region was approximately half the total mandible volume, making it a relatively lightweight structure.

I then developed a finite element model of the mandible, incorporating the material properties obtained from nanoindentation experiments. I applied three different boundary conditions to represent various scenarios during wood cutting: fully pinned, semi pinned, and pivot. These cases allowed me to investigate the load-bearing capability of the mandible, the effects of muscle attachments, and the displacement of the mandible about the hinge axis.

The stress contours on the mandible for these three boundary conditions showed few differences in the stress distributions at the tip of the mandible (region 3), which is primarily involved in cutting. The maximum stress of approximately 155 MPa was present on the back surface. However, stress differences among the boundary conditions were apparent towards the muscle attachment points (region 1) and at the base surface of the mandible.

I further investigated the spatial variations in the von Mises stresses along the front and back outer bounding surfaces of the mandible along its length. The results showed that stresses had similar profiles for the fully pinned and semi pinned cases on the front and back surfaces of the mandible. For the pivot case, stresses on the front surface were about five times higher in region 1 located towards the base of the mandible compared to the other two cases.

The hollow structure in the mandible extended from approximately 165 μm at the tip to the base of the mandible, coinciding with regions on the back and front surfaces having less stress (<90 MPa). The presence of the hollow region and its relationship with stress distributions suggest that these biomechanical adaptations aid in the cutting of wood by the mandibles.

<div class="row justify-content-sm-center">
{% include figure.html path="assets/img/fea2.jpg" alt="fre introduction" caption="von Mises stress distributions corresponding to A) fully pinned, B) Semi pinned, and C) Pivot boundary conditions are shown on the back, midsection, front, and base surfaces of the mandible." %}
</div>

## Conclusion

In conclusion, this study aimed to characterize the structure-property relationships of the CWSB larval mandibles and analyze their response to mechanical stresses encountered during wood cutting. Through a combination of experimental techniques and finite element simulations, I was able to explore the biomechanical properties and stress distribution patterns in the mandible, shedding light on the efficiency of the cutting mechanism employed by the larvae.

The highly curved and sharp cutting edge, as well as the internally localized conical hollow region, play critical roles in the mandible's performance during wood cutting. The hollow region not only reduces the weight of the mandible but also aids in stress distribution and load absorption during impact. Furthermore, the incorporation of zinc in the cutting edges increases material hardness and facilitates cutting through wood.

The finite element simulations conducted provided valuable insights into the stress distributions on the front and back surfaces of the mandible under different boundary conditions, revealing how biomechanical adaptations contribute to the cutting of wood. Additionally, the scaling model of two indenters cutting through a quasi-brittle wood material demonstrated how the larvae can produce small chip sizes suitable for ingestion through the modulation of the distance between the two mandible cutting edges.

These findings not only deepen our understanding of the biomechanical design principles in insect mandibles but also offer potential applications in the development of novel boring and cutting tools. Furthermore, the study highlights the possibility of leveraging biomechanical insights for pest control strategies, such as identifying zinc chelators as herbicides to control infestations. Overall, this research underscores the importance of studying mechanical principles in nature to design bioinspired tools and devise effective pest management solutions.
