---
layout: default
title: Applications list
permalink: /applist.html
---
{% assign applications = site.data.applications | sort: 'name' %}

{% for application in applications %}
{% if application.category == 1 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link p2popen.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 2 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link p2pclosed.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 3 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link otheropen.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 4 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link otherclosed.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% endif %}
{% if application.recommendation == 1 %}{% capture htmlimage %}<img src="images/checkmark.gif"><img src="images/checkmark.gif">{% endcapture %}
{% elsif application.recommendation == 2 %}{% capture htmlimage %}<img src="images/checkmark.gif">{% endcapture %}
{% else %}{% capture htmlimage %}<img src="images/x.gif">{% endcapture %}
{% endif %}
{{ htmllink }}{{ htmlimage }}
<br>
{% endfor %}
