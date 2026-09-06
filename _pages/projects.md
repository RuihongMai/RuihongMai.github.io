---
layout: page
title: projects
permalink: /projects/
nav: true
nav_order: 2
---

A selection of my undergraduate research and technical work.

{% assign ordered_projects = site.projects | sort: 'importance' %}
{% for project in ordered_projects %}
### [{{ project.title }}]({{ project.url | relative_url }})

{{ project.description }}

*{{ project.category }}*

{% endfor %}

