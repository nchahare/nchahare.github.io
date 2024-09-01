---
layout: post
title: "Python: How to setup VS code"
description: Just list of extensions needed for python to work well.
date: 2023-10-20
tags: resources
toc: true

authors:
  - name: Nimesh R. Chahare
    url: "https://nchahare.github.io"
    affiliations:
      name: Institute for Bioengineering of Catalonia, Barcelona
toc:
  - name: Introduction
  - name: Extensions
  - name: Install packages
  - name: References
---


## Introduction

I want to standardize things a little bit with vscode. So I am writing this post.

### Microsoft vscode

It's Free, little bit open source, but owned by Bill Gates. So don't get use it. So far I like it a lot because of plugins and most importantly it has in built git support. 


### Get started

1. Install vscode
2. Open a folder for your code
3. Save the folder as workspace (`File` --> `save as workspace`)
	   Workspace stores all your folders and settings in the file. So next time you can just open the workspace file.
4. Download extensions, icon is on the left 

## Extensions

1. Python extension pack
	
	This extension pack packages some of the most popular Python extensions.	
	- [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python "https://marketplace.visualstudio.com/items?itemName=ms-python.python") - Linting, Debugging (multi-threaded, remote), Intellisense, code formatting, refactoring, unit tests, snippets, Data Science (with Jupyter), PySpark and more.
	- [Jinja](https://marketplace.visualstudio.com/items?itemName=wholroyd.jinja "https://marketplace.visualstudio.com/items?itemName=wholroyd.jinja") - Jinja template language support for Visual Studio Code.
	- [Django](https://marketplace.visualstudio.com/items?itemName=batisteo.vscode-django "https://marketplace.visualstudio.com/items?itemName=batisteo.vscode-django") - Beautiful syntax and scoped snippets for perfectionists with deadlines.
	- [Visual Studio IntelliCode](https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode "https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode") - Provides AI-assisted productivity features for Python developers in Visual Studio Code with insights based on understanding your code combined with machine learning..
	- [Python Environment Manager](https://marketplace.visualstudio.com/items?itemName=donjayamanne.python-environment-manager "https://marketplace.visualstudio.com/items?itemName=donjayamanne.python-environment-manager") - Provides the ability to view and manage all of your Python environments & packages from a single place.
	- [Python Docstring Generator](https://marketplace.visualstudio.com/items?itemName=njpwerner.autodocstring "https://marketplace.visualstudio.com/items?itemName=njpwerner.autodocstring") - Quickly insert Python comment blocks with contextually inferred parameters for classes and methods based on multiple, selectable template patterns.
	- [Python Indent](https://marketplace.visualstudio.com/items?itemName=KevinRose.vsc-python-indent "https://marketplace.visualstudio.com/items?itemName=KevinRose.vsc-python-indent") - Correct python indentation in Visual Studio Code.
	- [Jupyter](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter "https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter") - Provides Jupyter notebook support for Python language, used for data science, scientific computing and machine learning.

2. Pylance: Fast, feature-rich language support for Python (*update: they have added this part in the extension pack since this post was written.*)
3. Jupyter: Notebook for python
4. CodeSnap: Lets you take screenshots of code
5. Path Intellisense: Visual Studio Code plugin that autocompletes filenames.


### To enable Jupyter style in python vscode (optional)

Enable this option `settings` > `jupyter: send selection to interactive window` 

So Idea is that in vscode you can open the jupyter notebook and run like normal notebook, but what is even better that you get to run the python files like jupyter notebook

By turning on the option, you can open the python file, select the like of code and press `shift + enter` . This opens another window which is like jupyter notebook.

## Install packages

Easy just use pip, it works and it is simple
`pip install blah`

## References

This guy did a video about it in context of data science, but I found his advice quite nice.
[https://www.youtube.com/watch?v=zulGMYg0v6U](https://www.youtube.com/watch?v=zulGMYg0v6U)
