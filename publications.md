---
layout: page
title: Publications
permalink: /publications/
nav: true
nav_order: 3
---

# Selected Publications

{% assign pubs = site.data.publications | sort: "year" | reverse %}

<ul class="publication-list">
  {% for pub in pubs %}
  <li>
    <p class="pub-title">
      <a href="{{ pub.url | default: '#' }}" target="_blank" rel="noopener noreferrer">
        {{ pub.title }}
      </a>
    </p>
    <p class="pub-authors">{{ pub.authors }}</p>
    <p class="pub-journal">
      <em>{{ pub.journal }}</em>
      {% if pub.volume %}, <strong>{{ pub.volume }}</strong>{% endif %}
      {% if pub.number %}({{ pub.number }}){% endif %}
      {% if pub.pages %}, pp. {{ pub.pages }}{% endif %}
      {% if pub.publisher %}, {{ pub.publisher }}{% endif %}
    </p>
    <p class="pub-year">{{ pub.year }}</p>
  </li>
  {% endfor %}
</ul>
