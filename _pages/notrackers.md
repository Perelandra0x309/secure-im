---
layout: default
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
{% if application.category == 1 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link p2popen.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 2 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link p2pclosed.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 3 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link otheropen.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 4 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link otherclosed.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 5 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link otherpartialopen.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 6 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link p2ppartialopen.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 10 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link index.html %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 11 %}{% capture htmllink %}<a href="{{ site.baseurl }}{% link index.html %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% endif %}
{% if application.recommendation == 1 %}{% capture htmlimage %}<img src="images/checkmark.gif"><img src="images/checkmark.gif">{% endcapture %}
{% elsif application.recommendation == 2 %}{% capture htmlimage %}<img src="images/checkmark.gif">{% endcapture %}
{% else %}{% capture htmlimage %}<img src="images/x.gif">{% endcapture %}
{% endif %}
<li>{{ htmllink }}{{ htmlimage }}</li>
{% endfor %}
</ul>
