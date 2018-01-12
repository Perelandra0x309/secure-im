---
layout: default
title: Applications list
permalink: /applist.html
---
{% for application in site.data.applications | sort: 'name' %}
<a href="{{ application.url }}">{{ application.display_name }}</a><br>
{% endfor %}
