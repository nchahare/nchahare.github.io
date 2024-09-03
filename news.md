---
layout: default
title:  Nimesh's News
permalink: /news/
---

<table>
  {%- assign sorted_news = site.news | sort: 'date' | reverse -%}
  {%- for item in sorted_news -%}
    <tr>
      <td class="date-column">
        {{ item.date | date: "%Y-%m-%d" }}
      </td>
      <td class="empty-column"></td>
      <td class="content-column">
        {{ item.content }}
      </td>
    </tr>
  {%- endfor -%}
</table>