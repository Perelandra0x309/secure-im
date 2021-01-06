---
layout: single
title: App Index
permalink: /applist.html
---
{% assign last_letter = "" %}
{% assign index_string = "" %}
{% assign total_count = 0 %}
{% assign namelist = site.data.applications | map: "display_name" | sort_natural %}
{% for name in namelist %}
  {% assign total_count = total_count | plus: 1 %}
  {% assign current_letter = name | slice: 0 | capitalize %}

  {% if current_letter != last_letter %}
    {% capture text %}<a href="#{{ current_letter }}1">{{ current_letter }}</a>&nbsp;{% endcapture %}
    {% assign index_string = index_string | append: text %}
  {% endif %}
  {% assign last_letter = current_letter %}

{% endfor %}

This is an alphabetical index of all the {{ total_count }} apps reviewed on this site.<br>
<br>
Recommendation key:<br>
<ul>
  <li><img src="images/checkmarkplus.gif">- Highly recommended</li>
  <li><img src="images/checkmark.gif">- Worth a try</li>
  <li><img src="images/x.gif">- Stay away!</li>
</ul>
<br>
<ul>
{{ index_string }}<br>
<br>

{% assign applications = site.data.applications | sort: 'name' %}
{% assign last_letter = "" %}
{% for application in applications %}
{% assign current_letter = application.name | slice: 0 | capitalize %}
{% if current_letter != last_letter %}
  {% assign letterindex = 1 %}
{% else %}
  {% assign letterindex = letterindex | plus: 1 %}
{% endif %}
{% assign last_letter = current_letter %}

{% if application.category == 1 %}{% capture htmllink %}<a id="{{ current_letter }}{{ letterindex }}" href="{{ site.baseurl }}{% link p2papps.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 2 %}{% capture htmllink %}<a id="{{ current_letter }}{{ letterindex }}" href="{{ site.baseurl }}{% link centralizedapps.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 3 %}{% capture htmllink %}<a id="{{ current_letter }}{{ letterindex }}" href="{{ site.baseurl }}{% link decentralizedapps.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 10 %}{% capture htmllink %}<a id="{{ current_letter }}{{ letterindex }}" href="{{ site.baseurl }}{% link rejectedapps.md %}#note2ee">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 11 %}{% capture htmllink %}<a id="{{ current_letter }}{{ letterindex }}" href="{{ site.baseurl }}{% link rejectedapps.md %}#{{ application.name }}">{{ application.display_name }}</a>{% endcapture %}
{% elsif application.category == 12 %}{% capture htmllink %}<a id="{{ current_letter }}{{ letterindex }}" href="{{ site.baseurl }}{% link protocols.md %}#{{ application.name }}">{{ application.display_name }}</a> (Messaging Protocol){% endcapture %}
{% else %}{% capture htmllink %}{{ application.display_name }}{% endcapture %}
{% endif %}
{% if application.recommendation == 1 %}{% capture htmlimage %}<img src="images/checkmarkplus.gif">{% endcapture %}
{% elsif application.recommendation == 2 %}{% capture htmlimage %}<img src="images/checkmark.gif">{% endcapture %}
{% else %}{% capture htmlimage %}<img src="images/x.gif">{% endcapture %}
{% endif %}
<li>{{ htmllink }}{{ htmlimage }}</li>
{% endfor %}
</ul>
