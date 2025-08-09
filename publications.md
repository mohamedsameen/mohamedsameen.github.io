---
layout: page
title: Publications
permalink: /publications/
nav: true
nav_order: 3
---


# Publications

{% assign pubs_by_year = site.data.publications | group_by: "year" | sort: "name" | reverse %}

{% for year_group in pubs_by_year %}
  <h2 class="pub-year">{{ year_group.name }}</h2>
  <ul class="pub-list">
    {% for pub in year_group.items %}
      <li>
        <p class="pub-title">
          <a href="{{ pub.url }}" target="_blank" rel="noopener noreferrer">{{ pub.title }}</a>
        </p>
        <p class="pub-authors">{{ pub.authors }}</p>
        <p class="pub-journal"><em>{{ pub.journal }}</em></p>
      </li>
    {% endfor %}
  </ul>
{% endfor %}
