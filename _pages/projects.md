---
layout: page
title: 项目
permalink: /projects
---
This is my projects page. 

<ul class="article-list">
  {% assign recent_notes = site.notes | where: "is_project", true | sort: "date" | reverse %}
  {% for note in recent_notes %}
    <li>
      <span class="article-date">{{ note.date | date: "%Y-%m-%d" }}</span><a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>