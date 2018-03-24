---
layout: default
title: Features Matrix
permalink: /featuresmatrix.html
---

<br>
Country Key:
<table style="width:15%">
	<tr><td bgcolor="red">5 Eyes Member</td></tr>
	<tr><td bgcolor="orange" style="color: black">9 Eyes Member</td></tr>
	<tr><td bgcolor="yellow" style="color: black">14 Eyes Member</td></tr>
</table>
<br>
Features Matrix:
<br>
{% assign applications = site.data.applications | where_exp: "item","item.category < 5" | sort: 'name' %}
<table>
<th>Name</th>
<th>P2P or Other</th>
<th>Open or Closed Source</th>
<th>Platforms</th>
<th>Country of Origin</th>
<th>Requires Phone# or Email</th>
<th>ID contains personal info</th>
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

{% if application.category == 1 or application.category == 2 or application.category == 6 %}
	<td>P2P</td>
{% elsif application.category == 3 or application.category == 4 or application.category == 5 %}
	<td>Other</td>
{% else %}
	<td>?</td>
{% endif %}
	
{% if application.category == 1 or application.category == 3 %}
	<td>Open</td>
{% elsif application.category == 5 or application.category == 6 %}
        <td>Partially Open</td>
{% elsif application.category == 2 or application.category == 4 %}
	<td>Closed</td>
{% else %}
	<td>?</td>
{% endif %}

	<td>{{ application.platforms }}</td>

{% if application.country_origin == "Australia"
	or application.country_origin == "Canada"
	or application.country_origin == "New Zealand"
	or application.country_origin == "UK"
	or application.country_origin == "USA" %}
	<td bgcolor="red">{{ application.country_origin }}</td>
{% elsif application.country_origin == "Denmark"
	or application.country_origin == "France"
	or application.country_origin == "Netherlands"
	or application.country_origin == "Norway" %}
	<td bgcolor="orange" style="color: black">{{ application.country_origin }}</td>
{% elsif application.country_origin == "Belgium"
	or application.country_origin == "Germany"
	or application.country_origin == "Italy"
	or application.country_origin == "Spain" %}
	<td bgcolor="yellow" style="color: black">{{ application.country_origin }}</td>
{% else %}
	<td>{{ application.country_origin }}</td>
{% endif %}

{% if application.requires_phone_number == "Either" %}
	<td bgcolor="red">Phone or Email</td>
{% elsif application.requires_phone_number == true and application.requires_email == true %}
	<td bgcolor="red">Phone and Email</td>
{% elsif application.requires_phone_number == false and application.requires_email == false %}
	<td bgcolor="green">No</td>
{% elsif application.requires_phone_number == true %}
	<td bgcolor="red">Phone</td>
{% elsif application.requires_email == true %}
	<td bgcolor="red">Email</td>
{% else %}
	<td>{{ application.requires_phone_number }}</td>
{% endif %}

{% if application.id_contains_contact_info == false %}
	<td bgcolor="green">No</td>
{% elsif application.id_contains_contact_info == "Email" %}
	<td bgcolor="red">Email</td>
{% elsif application.id_contains_contact_info == "Phone" %}
	<td bgcolor="red">Phone</td>
{% else %}
	<td>{{ application.id_contains_contact_info }}</td>
{% endif %}

{% if application.android_requires_google_play == true %}
	<td bgcolor="red">Yes</td>
{% elsif application.android_requires_google_play == false %}
	<td bgcolor="green">No</td>
{% else %}
	<td>{{ application.android_requires_google_play }}</td>
{% endif %}

{% if application.is_locally_encrypted == true %}
	<td bgcolor="green">Yes</td>
{% elsif application.is_locally_encrypted == false %}
	<td bgcolor="red">No</td>
{% else %}
	<td>{{ application.is_locally_encrypted }}</td>
{% endif %}

{% if application.perfect_forward_secrecy == true %}
	<td bgcolor="green">Yes</td>
{% elsif application.perfect_forward_secrecy == false %}
	<td bgcolor="red">No</td>
{% else %}
	<td>{{ application.perfect_forward_secrecy }}</td>
{% endif %}
</tr>
{% endfor %}

</table>
Page updated {{ page.date }}<br>
