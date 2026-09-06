---
layout: page
title: github / contact
permalink: /contact/
nav: true
nav_order: 4
---

I welcome conversations about machine learning, generative modeling, and technical projects.

{% if site.data.profile.github_username != '' %}
## GitHub

[{{ site.data.profile.github_username }}](https://github.com/{{ site.data.profile.github_username }})
{% else %}
GitHub profile: to be added.
{% endif %}

{% if site.data.profile.email != '' %}
## Email

[{{ site.data.profile.email }}](mailto:{{ site.data.profile.email }})
{% else %}
Email: to be added.
{% endif %}

