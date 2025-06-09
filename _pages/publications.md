---
layout: default
permalink: /publications/
title: "Publications"
---

{% for publication in site.data.publications %}
  ## {{ publication.title }}
  **Authors:** {{ publication.authors }}
  {% if publication.journal %}
  **Journal:** {{ publication.journal }}
  {% endif %}
  {% if publication.conference %}
  **Conference:** {{ publication.conference }}
  {% endif %}
  **Year:** {{ publication.year }}
  {% if publication.url %}
  [Link to Publication]({{ publication.url }})
  {% endif %}
{% endfor %}
