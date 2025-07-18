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
  <li style="margin-bottom: 20px; overflow: hidden;">
    {% if pub.image %}
      <img src="{{ pub.image | relative_url }}" width="100px" alt="Image for {{ pub.title }}" style="float: left; margin-right: 10px; border-radius: 4px;" />
    {% endif %}
    <div>
      {{ pub.authors }}. <strong>{{ pub.title }}</strong>. <em>{{ pub.journal }}</em>, <strong>{{ pub.year }}</strong>.
      {% if pub.doi %} <a href="{{ pub.doi }}" target="_blank">DOI</a>{% endif %}
      {% if pub.pdf %} | <a href="{{ pub.pdf }}" target="_blank">PDF</a>{% endif %}
    </div>
    <div style="clear: both;"></div>
  </li>
{% endfor %}
</ol>
</div>
