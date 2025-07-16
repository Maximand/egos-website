---
layout: single
title: "News"
permalink: /news/
---

<ul class="news-list">
{% assign sorted_news = site.news | sort: "date" | reverse %}
{% for post in sorted_news %}
  <li class="news-item">
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p><small>{{ post.date | date: "%B %-d, %Y" }}</small></p>
    <p>{{ post.summary }}</p>
  </li>
{% endfor %}
</ul>
