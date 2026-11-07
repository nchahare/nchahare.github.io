---
layout: default
title: Nimesh's Publications
description: Papers, patents and code. The full record lives on Google Scholar and ORCID.
permalink: /publications/
sections:
  - type: article
    heading: Research articles
  - type: patent
    heading: Patents
  - type: software
    heading: Research software
  - type: thesis
    heading: Thesis
---

<p class="small">
  Also on
  <a href="https://scholar.google.com/citations?user={{ site.scholar_userid }}">Google Scholar</a> /
  <a href="https://orcid.org/0000-0003-3210-6777">ORCID</a>.
  Equal contribution is marked with <strong>+</strong>.
</p>

{% for section in page.sections %}
  {%- assign entries = site.data.publications | where: "type", section.type -%}
  {%- if entries.size > 0 -%}
<h2 id="{{ section.type }}">{{ section.heading }}</h2>

<ul class="pub-list">
  {%- for item in entries %}
  <li class="pub">
    <span class="pub-year">{{ item.year }}</span>
    <span class="pub-body">
      <span class="pub-title">
        {%- if item.link -%}
          <a href="{{ item.link }}">{{ item.title }}</a>
        {%- else -%}
          {{ item.title }}
        {%- endif -%}
      </span>
      {%- if item.authors %}
      <span class="pub-authors">{{ item.authors }}</span>
      {%- endif %}
      <span class="pub-venue">
        {{ item.venue }}
        {%- if item.code %} &middot; <a href="{{ item.code }}">code</a>{% endif -%}
      </span>
    </span>
  </li>
  {%- endfor %}
</ul>
  {%- endif -%}
{% endfor %}

<style>
  .pub-list {
    list-style: none;
    padding-left: 0;
    margin: 0 0 2.5rem 0;
  }

  .pub {
    display: flex;
    gap: 1rem;
    padding: 0.9rem 0;
    border-bottom: 1px solid var(--border);
  }

  .pub:last-child {
    border-bottom: none;
  }

  .pub-year {
    flex: 0 0 3.5rem;
    color: var(--text-light);
    font-variant-numeric: tabular-nums;
  }

  .pub-body {
    display: block;
  }

  .pub-title {
    display: block;
    font-weight: bold;
  }

  .pub-authors,
  .pub-venue {
    display: block;
    font-size: 0.95rem;
    color: var(--text-light);
  }

  @media (max-width: 600px) {
    .pub {
      flex-direction: column;
      gap: 0.2rem;
    }

    .pub-year {
      flex: none;
      font-size: 0.9rem;
    }
  }
</style>
