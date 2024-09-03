---
layout: default
title: Journal of experimental Nimesh
description: Worlds second best non-peer review journal full of random things
---

{% for post in site.posts %}
  <div class="blog-item">
    <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
    <p class="meta"><i>{{ post.description }}</i></p>
    <p class="meta">{{ post.date | date_to_string }}</p>
  </div>
{% endfor %}