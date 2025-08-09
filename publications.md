---
layout: page
title: Publications
permalink: /publications/
nav: true            # Show in main navigation
nav_order: 3         # Adjust position as needed
---

# Selected Publications

Below is a curated list of my selected publications with clickable titles linking to the original papers.

{% assign pubs = site.data.publications %}

<ul class="publication-list">
  {% for pub in pubs %}
  <li>
    <p class="pub-title">
      <a href="{{ pub.url | default: '#' }}" target="_blank" rel="noopener noreferrer">
        <strong>{{ pub.title }}</strong>
      </a>
    </p>
    <p class="pub-authors">{{ pub.authors }}</p>
    <p class="pub-journal">
      <em>{{ pub.journal }}</em>
      {% if pub.volume %}, <strong>{{ pub.volume }}</strong>{% endif %}
      {% if pub.number %}({{ pub.number }}){% endif %}
      {% if pub.pages %}, pp. {{ pub.pages }}{% endif %}
      {% if pub.year %} ({{ pub.year }}){% endif %}
      {% if pub.publisher %}, {{ pub.publisher }}{% endif %}
    </p>
  </li>
  {% endfor %}
</ul>

