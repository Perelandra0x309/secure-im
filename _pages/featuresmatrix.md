---
layout: default
title: Features Matrix
permalink: /featuresmatrix.html
---

<br>
Features Matrix:

{% assign applications = site.data.applications | where_exp: "item","item.category < 5" | sort: 'name' %}

<table>
<th>Name</th>
<th>Type</th>
<th>Platforms</th>
<th>Country of Origin</th>
<th>Requires Phone#</th>
<th>Requires email</th>
<th>Requires Google Play</th>
<th>Locally Encrypted Data</th>
<th>Uses Perfect Forward Secrecy</th>

{% for application in applications %}
{% if application.recommendation == 1 %}{% capture htmlimage %}<img src="images/checkmark.gif"><img src="images/checkmark.gif">{% endcapture %}
{% elsif application.recommendation == 2 %}{% capture htmlimage %}<img src="images/checkmark.gif">{% endcapture %}
{% else %}{% capture htmlimage %}<img src="images/x.gif">{% endcapture %}
{% endif %}
<tr>
	<td>{% include generate_app_link.html app_name="application.name" %}</td>
	<td>{{ application.category }}</td>
	<td>{{ application.platforms }}</td>
	<td>{{ application.country_origin }}</td>
{% if application.requires_phone_number == "Yes" %}{% capture tdclass %} background-color="red"{% endcapture %}
{% if application.requires_phone_number == "No" %}{% capture tdclass %} background-color="green"{% endcapture %}
{% endif %}
	<td{{ tdclass }}>{{ application.requires_phone_number }}</td>

	<td>{{ application.requires_email }}</td>
	<td>{{ application.android_requires_google_play }}</td>
	<td>{{ application.is_locally_encrypted }}</td>
	<td>{{ application.perfect_forward_secrecy }}</td>
</tr>
{% endfor %}

</table>
Page updated {{ page.date }}<br>
