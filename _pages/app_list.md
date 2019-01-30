---
layout: single
title: Apps Index
permalink: /applist.html
---

Recommendation key:<br>
<ul>
  <li><img src="images/checkmark.gif"><img src="images/checkmark.gif">- Highly recommended</li>
  <li><img src="images/checkmark.gif">- Worth a try</li>
  <li><img src="images/x.gif">- Stay away!</li>
</ul>
<br>
Index of applications:
<ul>
{% assign applications = site.data.applications | sort: 'name' %}

{% for application in applications %}
{% if application.category == 1 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link p2papps.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 2 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link centralizedapps.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 3 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link decentralizedapps.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 10 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link rejectedapps.md %}#note2ee">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 11 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link rejectedapps.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 12 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link protocols.md %}#{{ application.name }}">{{ application.display_name }}</a> (Messaging Protocol){% endcapture %}
{% else %}{% capture htmllink %}{{ application.display_name }}{% endcapture %}
{% endif %}
{% if application.recommendation == 1 %}{% capture htmlimage %}<img src="images/checkmark.gif"><img src="images/checkmark.gif">{% endcapture %}
{% elsif application.recommendation == 2 %}{% capture htmlimage %}<img src="images/checkmark.gif">{% endcapture %}
{% else %}{% capture htmlimage %}<img src="images/x.gif">{% endcapture %}
{% endif %}
<li>{{ htmllink }}{{ htmlimage }}</li>
{% endfor %}
</ul>
