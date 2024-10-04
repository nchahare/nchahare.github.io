---
layout: default
title: Journal of experimental Nimesh
description: World's leading non-peer reviewed journal about Nimesh
permalink: /journal/
---

```
The newer content is withheld. 
Send me cash for them.
```

<table>
  {%- assign sorted_posts = site.posts | sort: 'date' | reverse -%}
  {%- for item in sorted_posts -%}
    <tr>
      <td class="date-column">
        {{ item.date | date: "%Y-%m-%d" }}
      </td>
      <td class="empty-column"></td>
      <td class="content-column">
        <a href="{{ item.url | relative_url }}">{{ item.title | escape }}</a>
      </td>
    </tr>
  {%- endfor -%}
</table>
