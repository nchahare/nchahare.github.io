---
title: Computational tool for analysing nuclear to cytoplasmic transport
author: Nimesh Chahare
excerpt: Description of my collaboration with Ion Andreu
date: 2021-09-10
tags: memories
layout: post
---
**Incomplete**

One day my friend Ion Andreu asked me to collaborate on a new project involving FLIP. I immediately said yes. To be honest, that time was not the best time for me with my main project. I was glad to help. At the time, Ion was working with Ignasi Granero-Moya at Prof. Pere Roca-Cusachs' lab.

Their lab also does mechanobiology but at much more molecular scale than I work in. As we know, cells sense their environment to perform physiological functions. Ion was working on understanding how the sensing happens. Mechanical force is one of the most important elements that make up the cell environment. So Ignasi and Ion were focusing their efforts on exploring the process of cell sensing the external forces.

They already had seen that the forces lead nuclear translocation of proteins, where some proteins would go from cytoplasm to nucleus or other way around. However, it was not clear if force controls the nucleocytoplasmic transport. There were many questions to answer, like

- Is the transport active or passive?  
- Why is there transport?  
- What happens to the permeability of the nucleus?  
- What is up with the nuclear pore complexes

Ion and Ignasi thought that this transport has to be mechanosensitive, independently of any specific signaling pathway. This would enable a general mechanism by which nuclear force could control the nuclear localization of proteins, and thereby transcription.

This is all cool, but where do I come in? Ignasi and Ion decided to look at transport of artificial molecules. They decided to look methods to quantify the transport. Bleaching techniques are an amazing way to quantify movement of molecules. Photobleaching burns the fluorescence of molecule at one particular location. If right after the bleaching, there are other molecules are moving in that location the fluorescence will be recovered. If it doesn't recover totally, it means that the molecules are bound and not mobile. This technique is called fluorescence recovery after photobleaching (FRAP). This is more standard technique, information you get is how fast the molecules diffuse and how much is the mobile fraction. For me the computation was simple. One script could do all the job: from analysing the images from microscope to the mobile fraction.

Using my code, they were able to show that the artificial constructs are totally mobile and do not bind to anything the cells.

My proper work came for working with fluorescence loss in photobleaching (FLIP). Here, on contrary to FRAP, you continue to bleach all the time in a small location. If there are mobile molecules, they will get bleached when they come to that location. And the whole cell will be bleached. If all the molecules are immobile then only the bleaching part gets bleached. This method is little complicated to analyse. There is no one single method which people use. There are people who do intense computational models to get the results. There are people who do not so much, which honestly feels wrong.

This is where my work started. Luckily I could refer to this paper:

Ege, N. et al. Quantitative analysis reveals that actin and src-family kinases regulate nuclear YAP1 and its export. Cell Syst. 6, 692–708.e13 (2018)

These people did too much. For me and Ion, it was very clear that we don't want to do that much.

I took it as inspiration and tried to simplify this transport problem. I thought of nucleus and cytoplasm as tanks connected to each other via tubes. But cytoplasm has a leak, implying constant bleaching. Intuitively, it is very clear that the cytoplasm tank is draining and as it is connected to the nucleus tank. Nucleus tank is also draining. The transport across the nucleus can be easily written in the form of simple ordinary differential equations.

There was some trouble with this kind of thinking that we forget what fluorescence means. Is it concentration of molecules or number of the molecules. Because of this we had to correct for the volumes of nucleus and cytoplasm.

However, in the end it worked great. We could understand the complex behaviour of the nucleus and mechanical forces.
