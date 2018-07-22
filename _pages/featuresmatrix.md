---
layout: featuresmatrix_layout
title: Features Matrix
permalink: /featuresmatrix.html
---
<br>
Country Key:
<table style="width:15%">
	<tr><td class="fiveeyes">5 Eyes Member</td></tr>
	<tr><td class="nineeyes">9 Eyes Member</td></tr>
	<tr><td class="fourteeneyes">14 Eyes Member</td></tr>
</table>
<br>
Features Matrix:
<br>
{% assign applications = site.data.applications | where_exp: "item","item.category < 7" | sort: 'name' %}
<table id="featurestable">
<thead><tr>
<th>Name</th>
<th>P2P or Other</th>
<th>Open or Closed Source</th>
<th width="15%">Platforms</th>
<th>Country of Origin</th>
<th>Requires Phone# or Email</th>
<th>ID contains personal info</th>
<th>Locally Encrypted Data</th>
<th>Uses Perfect Forward Secrecy</th>
<th>Ephemeral Messages</th>
<th>Foolproof (All Messages Encrypted)</th>
<th>Has Contact Verification</th>
<th>Android leaks files</th>
</tr></thead>
<tbody>

{% for application in applications %}
{% if application.recommendation == 1 %}{% capture htmlimage %}<img src="images/checkmark.gif"><img src="images/checkmark.gif">{% endcapture %}
{% elsif application.recommendation == 2 %}{% capture htmlimage %}<img src="images/checkmark.gif">{% endcapture %}
{% else %}{% capture htmlimage %}<img src="images/x.gif">{% endcapture %}
{% endif %}
<tr>
	<td>{{ htmlimage }}{% include generate_app_link.html app_name="application.name" %}</td>

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

{% capture classname %}{% endcapture %}
{% if application.country_origin == "Australia"
	or application.country_origin == "Canada"
	or application.country_origin == "New Zealand"
	or application.country_origin == "UK"
	or application.country_origin == "USA" %}
	{% capture classname %}fiveeyes{% endcapture %}
{% elsif application.country_origin == "Denmark"
	or application.country_origin == "France"
	or application.country_origin == "Netherlands"
	or application.country_origin == "Norway" %}
	{% capture classname %}nineeyes{% endcapture %}
{% elsif application.country_origin == "Belgium"
	or application.country_origin == "Germany"
	or application.country_origin == "Italy"
	or application.country_origin == "Spain" %}
	{% capture classname %}fourteeneyes{% endcapture %}
{% endif %}
{% if application.country_origin_source %}
  <td class="{{ classname }}"><a href="{{ application.country_origin_source }}">{{ application.country_origin }}</a></td>
{% else %}
	<td class="{{ classname }}">{{ application.country_origin }}</td>
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

{% if application.is_locally_encrypted == true %}
  {% if application.is_locally_encrypted_source %}
	<td bgcolor="green"><a href="{{ application.is_locally_encrypted_source }}">Yes</a></td>
	{% else %}
	<td bgcolor="green">Yes</td>
	{% endif %}
{% elsif application.is_locally_encrypted == false %}
  {% if application.is_locally_encrypted_source %}
	<td bgcolor="red"><a href="{{ application.is_locally_encrypted_source }}">No</a></td>
	{% else %}
	<td bgcolor="red">No</td>
	{% endif %}
{% else %}
	<td>{{ application.is_locally_encrypted }}</td>
{% endif %}

{% if application.perfect_forward_secrecy == true %}
  {% if application.perfect_forward_secrecy_source %}
	<td bgcolor="green"><a href="{{ application.perfect_forward_secrecy_source }}">Yes</a></td>
	{% else %}
	<td bgcolor="green">Yes</td>
	{% endif %}
{% elsif application.perfect_forward_secrecy == false %}
  {% if application.is_locally_encrypted_source %}
	<td bgcolor="red"><a href="{{ application.perfect_forward_secrecy_source }}">No</a></td>
	{% else %}
	<td bgcolor="red">No</td>
	{% endif %}
{% else %}
	<td>{{ application.perfect_forward_secrecy }}</td>
{% endif %}

{% if application.has_ephemeral_messages == true %}
	<td bgcolor="green">Yes</td>
{% elsif application.has_ephemeral_messages == false %}
	<td bgcolor="red">No</td>
{% else %}
	<td>{{ application.has_ephemeral_messages }}</td>
{% endif %}

{% if application.encypted_by_default == true %}
	<td bgcolor="green">Yes</td>
{% elsif application.encypted_by_default == false %}
	<td bgcolor="red">No</td>
{% else %}
	<td>{{ application.encypted_by_default }}</td>
{% endif %}

{% if application.has_contact_verification == true %}
	<td bgcolor="green">Yes</td>
{% elsif application.has_contact_verification == false %}
	<td bgcolor="red">No</td>
{% else %}
	<td>{{ application.has_contact_verification }}</td>
{% endif %}

{% if application.android_leaks_files == true %}
	<td bgcolor="red">Yes</td>
{% elsif application.android_leaks_files == false %}
	<td bgcolor="green">No</td>
{% else %}
	<td>{{ application.android_leaks_files }}</td>
{% endif %}

</tr>
{% endfor %}
</tbody>
</table>

<script language="javascript" type="text/javascript"> 
    // http://tablefilter.free.fr 
    var tableFilters = {
      status_bar: true,
      display_all_text: " [ Show all ] ",
      rows_counter: true,
      btn_reset: true,
      col_0: "none",
      col_1: "select",
      col_2: "select",
      col_3: "none",
      col_4: "select",
      col_5: "select",
      col_6: "select",
      col_7: "select",
      col_8: "select",
      col_9: "select",
      col_10: "select",
      col_11: "select",
      col_12: "select",
      help_instructions_html: "Use the filters above each column to filter and limit table data.<hr/>",
      
      /*** Extensions manager ***/
			btn_showHide_cols_text: 'Columns&#9660;',
			showHide_cols_text: 'Hide: ',
			extensions: {
				/*** Columns Visibility Manager extension load ***/
				name:['ColsVisibility'],
				src:['TableFilter/TFExt_ColsVisibility.js'],
				description:['Columns visibility manager'],
				initialize:[function(o){o.SetColsVisibility();}]
			}
    }  
    var tf01 = setFilterGrid("featurestable",1,tableFilters);  
</script>

<!--Page updated {{ page.date }}-->
<br>
