---
layout: page
title: cv
permalink: /cv/
nav: true
nav_order: 3
---

## {{ site.first_name }} {{ site.last_name }}

Machine learning · Python / PyTorch

{% if site.data.profile.resume_pdf != '' %}
[Download CV (PDF)]({{ site.data.profile.resume_pdf | relative_url }})
{% endif %}

## Education

**[{{ site.data.profile.university }}](https://zh.bit.edu.cn/)** — {{ site.data.profile.major }}
Undergraduate background · {{ site.data.profile.education_dates }}

Areas of study: machine learning, deep learning, and reinforcement learning.

## Research & Projects

{% assign ordered_projects = site.projects | sort: 'importance' %}
{% for project in ordered_projects %}
- **[{{ project.title }}]({{ project.url | relative_url }})** — {{ project.description }}
{% endfor %}

## Technical Skills

| Area | Tools and methods |
| --- | --- |
| Programming & frameworks | Python, PyTorch |
| Machine learning | ML, DL, RL; image diffusion; KNN |
| Language models | ChatGLM2-6B, LoRA, Prefix tuning, p-tuning |
| Computer vision | Custom VGG, CIFAR-10 |
| Systems & data | Linux, Hadoop, Spark, SQL, MySQL |

[Contact information]({{ '/contact/' | relative_url }})

