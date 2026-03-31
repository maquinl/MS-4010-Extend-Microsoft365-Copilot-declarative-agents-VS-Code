---
title: Online Hosted Instructions
permalink: index.html
layout: home
---

# MS-4010: Extend Microsoft 365 Copilot with declarative agents by using Visual Studio Code

These are the lab exercises associated with Microsoft skilling content on [Microsoft Learn](https://learn.microsoft.com/training/paths/build-plugins-connectors-microsoft-copilot-microsoft-365/).

<hr>

## Labs

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions/Labs'" | where_exp:"page", "page.lab.title" | where:"lab.islab", true | sort: "url" %}
| Module | Lab | Duration |
| --- | --- | --- |
{% for activity in labs %}| {{ activity.lab.module }} | [{{ activity.lab.title }}]({{ site.github.url }}{{ activity.url }}) | {{ activity.lab.duration }} |
{% endfor %}

<hr>

## Demos

{% assign demos = site.pages | where_exp:"page", "page.url contains '/Instructions/Demos'" | where_exp:"page", "page.demo.title" %}
{% for activity in demos %}
{% if activity.demo.title %}

### [{{ activity.demo.title }}]({{ site.github.url }}{{ activity.url }})

{% if activity.demo.module %}**Module**: {{ activity.demo.module }}{% endif %}
<hr>
{% endif %}
{% endfor %}
