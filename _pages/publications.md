---
layout: single
title: "Publications"
permalink: /publications/
author_profile: true
---

{% assign pubs = site.data.publications | sort: 'year' | reverse %}
{% assign count = 0 %}

<ol reversed>
{% for pub in pubs %}
  {% assign count = count | plus: 1 %}
  <li>
    {{ pub.authors }}. <strong>{{ pub.title }}</strong>. <em>{{ pub.journal }}</em>, <strong>{{ pub.year }}</strong>.
    {% if pub.doi %} <a href="{{ pub.doi }}" target="_blank">DOI</a>{% endif %}
    {% if pub.pdf %} | <a href="{{ pub.pdf }}" target="_blank">PDF</a>{% endif %}
  </li>
{% endfor %}
</ol>
