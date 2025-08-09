---
layout: single
title: "Publications"
permalink: /publications/
---

# Publications

<ul class="publications-list">
  {% for pub in site.data.publications %}
    <li>
      <p>
        <span class="pub-authors">{{ pub.authors }}</span> ({{ pub.year }}). 
        <em>
          {% if pub.url %}
            <a href="{{ pub.url }}" target="_blank" rel="noopener noreferrer">{{ pub.title }}</a>
          {% else %}
            {{ pub.title }}
          {% endif %}
        </em>.
        <span class="pub-journal">
          {% if pub.journal %} {{ pub.journal }}{% endif %}
          {% if pub.volume %}, <strong>{{ pub.volume }}</strong>{% endif %}
          {% if pub.number %}({{ pub.number }}){% endif %}
          {% if pub.pages %}, pp. {{ pub.pages }}{% endif %}.
        </span>
        {% if pub.publisher %} <small>({{ pub.publisher }})</small>{% endif %}
        {% if pub.booktitle %} In <em>{{ pub.booktitle }}</em>{% endif %}
        {% if pub.organization %} ({{ pub.organization }}){% endif %}
      </p>
    </li>
  {% endfor %}
</ul>

<style>
  .publications-list {
    list-style-type: none;
    padding-left: 0;
  }
  .publications-list li {
    margin-bottom: 1.3em;
    line-height: 1.4;
  }
  .publications-list a {
    color: #0066cc;
    text-decoration: none;
  }
  .publications-list a:hover {
    text-decoration: underline;
  }
  /* Smaller font for authors */
  .pub
