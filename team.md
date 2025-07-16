---
layout: single
permalink: /team/
---

<h1 style="text-align:center;">Meet the Team</h1>
<h2 style="text-align:center;">Researchers</h2>

<div class="team-grid">
{% for member in site.data.team %}
  <div class="team-member">
    <img src="{{ member.photo }}" alt="{{ member.name }}">
    <h3><a href="/team/{{ member.id }}/">{{ member.name }}</a></h3>
    <p>{{ member.role }}</p>
    <div class="team-links">
      {% if member.website %}
        <a href="{{ member.website }}">🔗</a>
      {% endif %}
      {% if member.email %}
        <a href="mailto:{{ member.email }}">✉️</a>
      {% endif %}
      {% if member.scholar %}
        <a href="{{ member.scholar }}">🎓</a>
      {% endif %}
    </div>
  </div>
{% endfor %}
</div>
