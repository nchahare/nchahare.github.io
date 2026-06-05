---
layout: default
title:  Nimesh's News
permalink: /news/
---

<style>
  table {
    vertical-align: top;
  }
  td {
    vertical-align: top;
  }
  /* Optional: Adds a tiny bit of space below the title */
  .news-title {
    margin-top: 0;
    margin-bottom: 0.5rem;
  }
</style>

<table>
  {%- assign sorted_news = site.news | sort: 'date' | reverse -%}
  {%- for item in sorted_news -%}
    <tr>
      <td class="date-column">
        {{ item.date | date: "%Y-%m-%d" }}
      </td>
      <td class="empty-column"></td>
      <td class="content-column">
        <h4 class="news-title">{{ item.title }}</h4>
        {{ item.content }}
      </td>
    </tr>
  {%- endfor -%}
</table>

<!-- The funny archive line -->
<p class="archive-note">
  Looking for older archives? 
  The past isn't free, folks. 
  Send some cash to unlock the premium history tier.
</p>