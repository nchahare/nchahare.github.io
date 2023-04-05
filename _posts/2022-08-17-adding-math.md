---
title: Adding Math to my jekyll webpage
date: 2022-08-17
author: Nimesh Chahare
excerpt:
tags: notes
mathjax: true
layout: post

---



By default it was not possible to use math equations in the markdown Jekyll blogs. I was using github readme markdown earlier and there it supports the typical Latex math text.

So to solve any problem in my life, I google and found the solution right away. Thanks to this person's comment [here](https://github.com/mmistakes/minimal-mistakes/issues/735#issuecomment-269500816) and this blog [here](https://www.katarinahoeger.com/2017/12/08/jekyll-supports-math). Both essentially say the same thing.

Add a directory called

```cmd
"_includes\scripts.html"
```

Edit the html with

```html
{% if page.mathjax %}
<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>
{% endif %}
```

This would allow you to use mathjax library to write equations. You just have to had the following in the YAML

```md
---
mathjax: true
---
```

Fun fact:

> YAML stands for **yet another markup language** or YAML ain't markup language (a recursive acronym)
>
> YAML stuff is on the top of every markdown files adding data



My first attempt to write equations

```math
$$ a = 1 $$
$$ b = 2 $$
$$ a + b = 3 $$
```

$$ a = 1 $$
$$ b = 2 $$
$$ a + b = 3 $$



It works great. I will use the following webpage as Mathjax reference:

- [MathJax basic tutorial and quick reference - Mathematics Meta Stack Exchange](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/5024#5024)

- [MathJax Cheat Sheet for Mathematical Notation @ https://jojozhuang.github.io](https://jojozhuang.github.io/tutorial/mathjax-cheat-sheet-for-mathematical-notation/)



It was little  scary for me as a new user to jekyll to add an extra directory like include and scripts.html. Because in past, every time I add something like this the whole site stops functioning properly. I am glad that it worked properly and in the future I might be able to add more scripts like this.
