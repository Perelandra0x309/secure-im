---
layout: default
title: Peer to Peer Open Source
---
<table>
  <tr><td colspan="4" style="text-align:center"><H2>P2P Open Source</H2></td></tr>
  <tr><td><b>Application</b></td>
  <td><b>Platforms</b></td>
  <td><b>Communication types</b></td></tr>
{% assign applications = site.data.applications | where:"category","1" | sort: 'name' | sort: 'recommendation' %}
{% for application in applications %}
<tr>
  <td>
    {% if application.recommendation == 1 %}<img src="images/checkmark.gif"><img src="images/checkmark.gif">
    {% elseif application.recommendation == 2 %}<img src="images/checkmark.gif">
    {% else %}<img src="images/checkmark.gif"><img src="images/x.gif">{% endif %}
    <a name="{{ application.name }}" href="{{ application.url }}">{{ application.display_name }}</a>
  </td>
  <td>{{ application.platforms }}</td>
  <td>{{ application.communication_types }}</td>
</tr>
<tr><td colspan="4">
  Country of origin: {{ application.country_origin }}<br>
  Requires a phone number: {{ application.requires_phone_number }}<br>
  Requires an email address: {{ application.requires_email }}<br>
  Android app requires Google Play Services: {{ application.android_requires_google_play }}<br>
  Data is locally encrypted: {{ application.is_locally_encrypted }}<br>
  Perfect forward secrecy: {{ application.perfect_forward_secrecy }}<br>
  Websites: {{ application.websites }}<br>
  <hr>
  <b>Notes:</b><br>
  {% include_relative _data/{{ application.notes_file }} %}
</td></tr>
{% endfor %}

</table>
