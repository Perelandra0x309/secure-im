---
layout: default
title: Peer to Peer Open Source
---
<table>
  <tr><td colspan="4" style="text-align:center"><H2>P2P Open Source</H2></td></tr>
  <tr><td><b>Application</b></td>
  <td><b>Platforms</b></td>
  <td><b>Communication types</b></td></tr>
{% for application in site.data.applications %}
<tr>
  <td><a name="{{ application.name }}" href="{{ application.url }}">{{ application.name }}</a></td>
  <td><a href="https://ricochet.im/releases/latest/">Windows, Mac, Linux</a></td>
  <td>Text</td>
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
   
</td></tr>
{% endfor %}

</table>
