---
layout: default
title: Fresh, Canned, and Frozen
description: Nimesh's cookbook
permalink: /cookbook/
---


<table>
  {%- assign sorted_recipes = site.recipes | sort: 'date' | reverse -%}
  {%- for item in sorted_recipes -%}
    <tr>
      <td class="date-column">
        <a href="{{ item.url | relative_url }}">{{ item.title | escape }}</a>
      </td>
      <td class="empty-column"></td>
      <td class="content-column">
        {{ item.description | escape }}
      </td>
    </tr>
  {%- endfor -%}
</table>
