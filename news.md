---
layout: single
title: "News"
permalink: /news/
---

{% assign sorted_news = site.news | sort: "date" | reverse %}

{% if sorted_news.size > 0 %}
<ul class="news-list">
  {% for post in sorted_news %}
    <li class="news-item">
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <p><small>{{ post.date | date: "%B %-d, %Y" }}</small></p>
      <p>{{ post.summary }}</p>
    </li>
  {% endfor %}
</ul>
{% else %}
<p class="no-news"><em>No news yet, please check back soon!</em></p>
{% endif %}
