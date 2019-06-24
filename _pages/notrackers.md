---
layout: single
title: No Trackers Hall of Fame
permalink: /notrackers.html
---
Recommendation key:<br>
<ul>
  <li><img src="images/checkmark.gif"><img src="images/checkmark.gif">- Highly recommended</li>
  <li><img src="images/checkmark.gif">- Worth a try</li>
</ul>
<br>
Recommended Android apps that have no trackers (according to <a href="https://exodus-privacy.eu.org/page/what/">exodus-privacy.eu.org</a>)
<br>
{% assign applications = site.data.applications | where:"exodus_privacy_trackers_count","0" |  where_exp:"item","item.recommendation < 3" | sort: 'name' %}
<ul>
{% for application in applications %}
{% if application.category == 1 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link p2papps.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 2 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link centralizedapps.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 3 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link decentralizedapps.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 10 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link rejectedapps.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 11 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link rejectedapps.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 12 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link protocols.md %}#{{ application.name }}">{{ application.display_name }}</a> (Messaging Protocol){% endcapture %}
{% endif %}
{% if application.recommendation == 1 %}{% capture htmlimage %}<img src="images/checkmark.gif"><img src="images/checkmark.gif">{% endcapture %}
{% elsif application.recommendation == 2 %}{% capture htmlimage %}<img src="images/checkmark.gif">{% endcapture %}
{% else %}{% capture htmlimage %}<img src="images/x.gif">{% endcapture %}
{% endif %}
<li>{{ htmllink }}{{ htmlimage }}</li>
{% endfor %}
</ul>
