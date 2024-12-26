---
layout: page
title: 写作
permalink: /writing
---

[[为什么要写作|写作能帮助我更好的思考]]。

关注我的公众号：文遇安。

## 文章

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} —— <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>
