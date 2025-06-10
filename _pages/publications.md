---
layout: single
title: "Publications"
permalink: /publications/
author_profile: true
---

<div class="small">
{% assign pubs = site.data.publications | sort: 'year' | reverse %}

<ol reversed>
{% for pub in pubs %}
  <li>
    {{ pub.authors }}. <strong>{{ pub.title }}</strong>. <em>{{ pub.journal }}</em>, <strong>{{ pub.year }}</strong>.
    {% if pub.doi %} <a href="{{ pub.doi }}" target="_blank">DOI</a>{% endif %}
    {% if pub.pdf %} | <a href="{{ pub.pdf }}" target="_blank">PDF</a>{% endif %}
  </li>
{% endfor %}
</ol>
</div>
