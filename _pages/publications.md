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
  <li style="margin-bottom: 20px; padding-bottom: 20px; border-bottom: 1px solid #ccc; overflow: hidden;">
    {% if pub.image %}
      <img src="{{ pub.image | relative_url }}" width="150px" alt="Image for {{ pub.title }}" style="float: left; margin-right: 15px; border-radius: 6px;" />
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
