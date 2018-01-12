---
layout: default
title: Applications list
permalink: /applist.html
---
{% assign applications = site.data.applications | sort: 'name' %}
{% for application in applications %}
{% if application.category == 1 %}<a href="/p2popen.html#{{ application.name }}">{{ application.display_name }}</a>
{% elsif application.category == 2 %}<a href="/p2pclosed.html#{{ application.name }}">{{ application.display_name }}</a>
{% elsif application.category == 3 %}<a href="/otheropen.html#{{ application.name }}">{{ application.display_name }}</a>
{% elsif application.category == 4 %}<a href="/otherclosed.html#{{ application.name }}">{{ application.display_name }}</a>
{% endif %}
{% if application.recommendation == 1 %}<img src="images/checkmark.gif"><img src="images/checkmark.gif">
{% elsif application.recommendation == 2 %}<img src="images/checkmark.gif">
{% else %}<img src="images/x.gif">
{% endif %}
<br>
{% endfor %}
