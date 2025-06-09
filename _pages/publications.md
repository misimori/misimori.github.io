---
layout: single
title: "Publications"
permalink: /publications/
author_profile: true
---

{% for pub in site.data.publications %}
### {{ pub.title }}
**Authors:** {{ pub.authors }}  
**Journal:** {{ pub.journal }}, {{ pub.year }}  
{% if pub.doi %}[DOI]( {{ pub.doi }} ){% endif %} {% if pub.pdf %}| [PDF]( {{ pub.pdf }} ){% endif %}
<hr>
{% endfor %}
