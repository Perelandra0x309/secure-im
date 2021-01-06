---
layout: single
title: Messaging Protocols
which_category: 12
---
Some protocols are used by many applications, so all the applications that use these protocols will share the same features.<br>
<br>

<table class="w3-table w3-striped w3-bordered">
  <tr class="w3-dark-grey">
  <td><b>Protocol</b></td>
  <td><b>Communication types</b></td></tr>
{% assign applications = site.data.applications | where_exp: "item","item.category == page.which_category" | sort: 'name' | sort: 'recommendation' %}
{% for application in applications %}
<tr id="{{ application.name }}" >
  <td>
    {% if application.recommendation == 1 %}<img src="images/checkmarkplus.gif">
    {% elsif application.recommendation == 2 %}<img src="images/checkmark.gif">
    {% else %}<img src="images/x.gif">{% endif %}
    <a href="{{ application.url }}">{{ application.display_name }}</a>
  </td>
  <td>{{ application.communication_types }}</td>
</tr>
<tr><td colspan="4">
  
  Encryption protocol: {{ application.encryption_protocol }}<br>
  Shared Secret exchange: {{ application.shared_secret_exchange }}<br>
  Message Encryption Cipher: {{ application.message_encryption_cipher }}<br>
  Business model: {{ application.business_model }}<br>

{% if application.perfect_forward_secrecy == true %}
  {% if application.perfect_forward_secrecy_source %}
	Perfect forward secrecy: <span class="green"><a href="{{ application.perfect_forward_secrecy_source }}">Yes</a></span><br>
	{% else %}
	Perfect forward secrecy: <span class="green">Yes</span><br>
	{% endif %}
{% elsif application.perfect_forward_secrecy == false %}
  {% if application.perfect_forward_secrecy_source %}
	Perfect forward secrecy: <span class="red"><a href="{{ application.perfect_forward_secrecy_source }}">No</a></span><br>
	{% else %}
	Perfect forward secrecy: <span class="red">No</span><br>
	{% endif %}
{% else %}
	Perfect forward secrecy: {{ application.perfect_forward_secrecy }}<br>
{% endif %}

{% if application.message_stored_on_server == "Never" %}
  {% if application.message_stored_on_server_source %}
	Messages stored on server: <span class="green"><a href="{{ application.message_stored_on_server_source }}">Never</a></span><br>
	{% else %}
	Messages stored on server: <span class="green">Never</span><br>
	{% endif %}
{% elsif application.message_stored_on_server == true %}
  {% if application.message_stored_on_server_source %}
	Messages stored on server: <span class="red"><a href="{{ application.message_stored_on_server_source }}">Yes</a></span><br>
	{% else %}
	Messages stored on server: <span class="red">Yes</span><br>
	{% endif %}
{% elsif application.message_stored_on_server == "Temporarily" %}
  {% if application.message_stored_on_server_source %}
	Messages stored on server: <span class="yellow"><a href="{{ application.message_stored_on_server_source }}">Temporarily</a></span><br>
	{% else %}
	Messages stored on server: <span class="yellow">Temporarily</span><br>
	{% endif %}
{% else %}
	Messages stored on server: {{ application.message_stored_on_server }}<br>
{% endif %}


  Websites: {{ application.websites }}<br>
  Last tested: {{ application.last_update }}<br>
  <b>Notes:</b><br>
  <br>
  {% include_relative _data/{{ application.notes_file }} %}
</td></tr>
{% endfor %}

</table>
