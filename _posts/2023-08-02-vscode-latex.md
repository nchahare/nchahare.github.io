---
title: "VS code: how to do LaTeX"
author: Nimesh Chahare
layout: post
date: 2023-08-02
description: How to run LaTeX in Visual Studio Code
tags: notes
---

Latex is a useful program for making nice documents. I use it to prepare my CV, letters, research statements, and most importantly, my PhD and Masters thesis. Yeah! Yeah! I know Word is better for sharing and collaborating; Now people are even using Google Docs. What a world! The other day, an undergrad remarked to me, "You use MS Word? That's for older people! Yes, you are old."

Anyways, It's true sometimes you will spend way too much time to on fixing figure caption alignment than in any other program, but I must say it is worth it. Documents look good! You can say its a small price you pay for beauty. 

**Choosing the editor**: Some people are using Overleaf for compiling documents online. It works for smaller documents. However, I always recommend people to run their code and programs locally. Don't need to send your data to random companies on internet. I found the best way of using Latex is by using it in VSCode.

**Procedure**: Just download and install the VSCode. Then install MiKTeX. MiKTeX, is a lighter installation of Latex. While installing, select the option of "Yes" to install packages on the fly. After the installation of MiKTeX, open the console and check for updates. If everything is up to date. You can move on to downloading and installing Strawbery Perl.  After all programs are installed, open VSCode go to the extensions tab, and then install the "LateX Workshop" extension. 

Then you are ready! Just write some document in tex or find some latex repository template on the internet. When you open the document in VSCode, you will see that the LateX workshop extension is able to detect the tex code, and on the left, there is an extra tab for tex. You can select the option to build the document. You can view the pdf. You can even select the option for clearing auxiliary files. 

All works well! You can see the status of your build on the bottom-left panel. If you want to go back and forth between pdf and code, use `ctrl` + `click`. 

I like VSCode because it is very well integrated in my workflow for git and version control. 

**References**: I just watched this [video](https://www.youtube.com/watch?v=4lyHIQl4VM8) by Fedrico. Also this [blog](https://mark-wang.com/blog/2022/latex/) gave good tips

