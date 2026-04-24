---
layout: default
title: Portfolio
---

# Portfolio

{% for project in site.projects %}
## [{{ project.title }}]({{ site.baseurl }}{{ project.url }})

**Technologies:** {{ project.technologies }}

{{ project.excerpt }}
{% endfor %}