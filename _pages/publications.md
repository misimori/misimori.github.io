---
layout: single
title: "Publications"
permalink: /publications/
author_profile: true
---

<div class="small">
<ol reversed>
{% assign pubs = site.data.publications | sort: 'year' | reverse %}
{% for pub in pubs %}
  <li>
    {{ pub.authors }}.
    {% if pub.doi %}
      <strong><a href="{{ pub.doi }}" target="_blank">{{ pub.title }}</a></strong>.
    {% elsif pub.pdf %}
      <strong><a href="{{ pub.pdf }}" target="_blank">{{ pub.title }}</a></strong>.
    {% else %}
      <strong>{{ pub.title }}</strong>.
    {% endif %}
    <em>{{ pub.journal }}</em>, <strong>{{ pub.year }}</strong>.
    {% if pub.doi %} <a href="{{ pub.doi }}" target="_blank">DOI</a>{% endif %}
    {% if pub.pdf %} | <a href="{{ pub.pdf }}" target="_blank">PDF</a>{% endif %}
  </li>
{% endfor %}
</ol>
</div>
