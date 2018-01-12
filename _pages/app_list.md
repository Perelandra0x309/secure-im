---
layout: default
title: Applications list
permalink: /applist.html
---
{% assign applications = site.data.applications | sort: 'name' %}
{% for application in applications %}
<a href="{{ application.url }}">{{ application.display_name }}</a><br>
{% endfor %}
