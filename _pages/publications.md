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
    {% if pub.image %}
    <img src="{{ pub.image | relative_url }}" alt="Thumbnail for {{ pub.title }}" style="width: 120px; float: left; margin-right: 15px; border-radius: 6px;" />
    {% endif %}
  <p>
    <strong>{{ pub.title }}</strong><br>
    {{ pub.authors }}<br>
    <em>{{ pub.journal }}</em>, {{ pub.year }}<br>
    {% if pub.link %}
      <a href="{{ pub.link }}">[PDF]</a>
    {% endif %}
  </p>
  
  <li>
    {{ pub.authors }}. <strong>{{ pub.title }}</strong>. <em>{{ pub.journal }}</em>, <strong>{{ pub.year }}</strong>.
    {% if pub.doi %} <a href="{{ pub.doi }}" target="_blank">DOI</a>{% endif %}
    {% if pub.pdf %} | <a href="{{ pub.pdf }}" target="_blank">PDF</a>{% endif %}
  </li>
  
  
{% endfor %}
</ol>
</div>

