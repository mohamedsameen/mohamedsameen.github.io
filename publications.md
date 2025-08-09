---
layout: page
title: Publications
permalink: /publications/
nav: true
nav_order: 3
---

# Publications

{% assign pubs = site.data.publications | sort: "year" | reverse %}

{% assign current_year = nil %}

{% for pub in pubs %}
  {% if pub.year != current_year %}
    {% if current_year != nil %}
      </ul>
    {% endif %}
    <h2 class="pub-year">{{ pub.year }}</h2>
    <ul class="pub-list">
    {% assign current_year = pub.year %}
  {% endif %}

  <li>
    <p class="pub-title">
      <a href="{{ pub.url | default: '#' }}" target="_blank" rel="noopener noreferrer">{{ pub.title }}</a>
    </p>
    <p class="pub-authors">{{ pub.authors }}</p>
    <p class="pub-journal"><em>{{ pub.journal }}</em></p>
  </li>

  {% if forloop.last %}
    </ul>
  {% endif %}
{% endfor %}
