---
layout: single
title: "Publications"
permalink: /publications/
---

{% assign pubs = site.data.publications %}
{% if pubs.size > 0 %}
{% for pub in pubs %}
<div class="publication">
<p>
{{ pub.authors }}.
<a href="{{ pub.pdf }}">{{ pub.title }}</a>.
<em>{{ pub.venue }}, {{ pub.year }}.</em>
</p>
<div class="pub-links">
{% if pub.pdf %}<a href="{{ pub.pdf }}">PDF</a>{% endif %}
{% if pub.cite %}<a href="{{ pub.cite }}">Cite</a>{% endif %}
{% if pub.code %}<a href="{{ pub.code }}">Code</a>{% endif %}
</div>
</div>
{% endfor %}
{% else %}
<p class="no-publications"><em>No publications listed yet. Check back soon!</em></p>
{% endif %}
