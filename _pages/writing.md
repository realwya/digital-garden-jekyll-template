---
layout: page
title: 文章
permalink: /writing
---

我相信[[为什么要写作|写作能帮助我更好的思考]]。

关注我的公众号：**文遇安**，第一时间收到更新。

### 文章

<ul class="article-list">
  {% assign recent_notes = site.notes | sort: "date" | reverse %}
  {% for note in recent_notes %}
    <li>
      <span class="article-date">{{ note.date | date: "%Y-%m-%d" }}</span><a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>
