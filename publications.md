---
layout: single
title: "Publications"
permalink: /publications/
---

# Publications

<ul>
  {% for pub in site.data.publications %}
    <li>
      <strong>{{ pub.authors }}</strong> ({{ pub.year }}). 
      <em>{{ pub.title }}</em>{% if pub.journal %}, {{ pub.journal }}{% endif %}{% if pub.volume %}, {{ pub.volume }}{% endif %}{% if pub.number %}({{ pub.number }}){% endif %}{% if pub.pages %}, {{ pub.pages }}{% endif %}.
      {% if pub.publisher %} <small>({{ pub.publisher }})</small>{% endif %}
      {% if pub.booktitle %} In <em>{{ pub.booktitle }}</em>{% endif %}
      {% if pub.organization %} ({{ pub.organization }}){% endif %}
    </li>
  {% endfor %}
</ul>
