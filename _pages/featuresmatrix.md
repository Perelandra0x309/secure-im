---
layout: single
title: App Features Matrix
permalink: /featuresmatrix.html
---
<em>Note: this page is best viewed on a desktop computer with a large screen!</em><br>
<br>
This matrix shows many of the features of each app I have reviewed in detail.  There is a lot of data to display so I have tried to make it possible for you to hide columns in the table and show only the columns you wish to compare.  Javascript is required for this feature.<br>
<br>
In the top right corner of the features table is a menu titled "Columns".  Click on this to show a menu where you can hide the columns you do not wish to see.  If the table is still too large to view all at once after removing some columns you can also use your web browser's zoom setting to shrink the entire page.  A zoom setting of 80% may be enough to view the entire table.<br>
<br>
To prevent some level of infomation overload, I have not included applications in this matrix that are not recommended for obvious reasons (cost, not E2EE, enterprise only) as listed on my <a href="{% link rejectedapps.md %}">Rejected Apps page</a>.<br>
<br>
Country Key:<br>
<table border="1" cellpadding="5" style="border-collapse: collapse;">
	<tr><td class="fiveeyes">5 Eyes Member</td></tr>
	<tr><td class="nineeyes">9 Eyes Member</td></tr>
	<tr><td class="fourteeneyes">14 Eyes Member</td></tr>
</table>

<br>
Encryption Methods:
<table border="1" cellpadding="3" style="border-collapse: collapse;">
<tr><th></th><th>Shared Secret Exchange</th><th>Message Encryption Cipher</th></tr>
<tr>
<td style="width:15%">Best:</td>
<td style="width:50%">
<a href="https://www.signal.org/docs/specifications/x3dh/">X3DH Curve25519, X3DH Curve448</a><br>
ECDH25519, ECDHC brainpoolp256r1, ECDH P256, ECDH P521 (Diffie-Hellman Elliptical Curves)<br>
RSA 4096 PKI and higher
</td>
<td style="width:35%">
<a href="https://download.libsodium.org/doc/advanced/stream_ciphers/xsalsa20">XSalsa20</a>, <a href="https://download.libsodium.org/doc/advanced/stream_ciphers/xchacha20">XChaCha20</a><br>
AES-192, AES-256
</td>
</tr>

<tr>
<td>Good:</td>
<td>
DH MODP1536 through MODP8192 (Diffie-Hellman Modular Exponential)<br>
RSA 2048 PKI
</td>
<td>
<a href="https://download.libsodium.org/doc/advanced/stream_ciphers/salsa20">Salsa20</a>, <a href="https://download.libsodium.org/doc/advanced/stream_ciphers/chacha20">ChaCha20</a><br>
AES-128
</td>
</tr>

<tr>
<td>Not Recommended:</td>
<td>
RSA 1024 PKI
</td>
<td>RC4+</td>
</tr>
</table>

<br>
Features Matrix:
<br>
{% assign applications = site.data.applications | where_exp: "item","item.category < 7" | sort: 'name' %}
<table id="featurestable" style="border-collapse: collapse;">
<thead><tr>
<th>&nbsp;&nbsp;&nbsp;</th>
<th>Name</th>
<th>Infrastructure</th>
<th>Source Code</th>
<th width="15%">Platforms</th>
<th>Encryption Protocol</th>
<th>Shared Secret Exchange</th>
<th>Message Encryption Cipher</th>
<th>Country of Origin</th>
<th>Requires Phone# or Email</th>
<th>ID contains personal info</th>
<th>Locally Encrypted Data</th>
<th>Uses Perfect Forward Secrecy</th>
<th>Ephemeral Messages</th>
<th>Foolproof (All Messages Encrypted)</th>
<th>Has Contact Verification</th>
<th>Leaks Files</th>
<th>Android Trackers</th>
<th>Business Model</th>
</tr></thead>
<tbody>

{% assign final_platforms = 'Android' %}

{% for application in applications %}
{% if application.recommendation == 1 %}
  {% capture htmlimage %}<img  src="images/checkmarkplus.gif">{% endcapture %}
  {% capture recdiv %}<div style="display:none;">recommended</div>{% endcapture %}
{% elsif application.recommendation == 2 %}
  {% capture htmlimage %}<img src="images/checkmark.gif">{% endcapture %}
  {% capture recdiv %}<div style="display:none;">recommended</div>{% endcapture %}
{% else %}
  {% capture htmlimage %}<img src="images/x.gif">{% endcapture %}
  {% capture recdiv %}{% endcapture %}
{% endif %}
<tr>
	<td>{{ htmlimage }}</td>
	<td>{{ recdiv }}{% include generate_app_link.html app_name=application.name %}</td>

{% if application.category == 1 %}
	<td>P2P</td>
{% elsif application.category == 2 %}
	<td>Centralized</td>
{% elsif application.category == 3 %}
	<td>Decentralized</td>
{% else %}
	<td>?</td>
{% endif %}

<td>{{ application.source_type }}</td>

<td>{{ application.platforms }}</td>
{% assign platforms_scrubbing = application.platforms | strip_html | split: '(' %}
{% for element in platforms_scrubbing %}
  {% assign clean = element | append: ' ' | split: ')' | last | strip | replace: ' ,',',' | replace: ', ',',' %}
  {% assign final_platforms = final_platforms | append: ',' | append: clean %}
{% endfor %}
{% assign final_platforms = final_platforms | replace: ',,',',' | split:',' | uniq | join: ',' %}

<td>{{ application.encryption_protocol }}</td>

<td>{{ application.shared_secret_exchange }}</td>

<td>{{ application.message_encryption_cipher }}</td>

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
	<td class="red">Phone or Email</td>
{% elsif application.requires_phone_number == true and application.requires_email == true %}
	<td class="red">Phone and Email</td>
{% elsif application.requires_phone_number == false and application.requires_email == false %}
	<td class="green">No</td>
{% elsif application.requires_phone_number == true %}
	<td class="red">Phone</td>
{% elsif application.requires_email == true %}
	<td class="red">Email</td>
{% else %}
	<td>{{ application.requires_phone_number }}</td>
{% endif %}

{% if application.id_contains_contact_info == false %}
	<td class="green">No</td>
{% elsif application.id_contains_contact_info == "Email" %}
	<td class="red">Email</td>
{% elsif application.id_contains_contact_info == "Phone" %}
	<td class="red">Phone</td>
{% else %}
	<td>{{ application.id_contains_contact_info }}</td>
{% endif %}

{% if application.is_locally_encrypted == true %}
  {% if application.is_locally_encrypted_source %}
	<td class="green"><a href="{{ application.is_locally_encrypted_source }}">Yes</a></td>
	{% else %}
	<td class="green">Yes</td>
	{% endif %}
{% elsif application.is_locally_encrypted == false %}
  {% if application.is_locally_encrypted_source %}
	<td class="red"><a href="{{ application.is_locally_encrypted_source }}">No</a></td>
	{% else %}
	<td class="red">No</td>
	{% endif %}
{% else %}
	<td>{{ application.is_locally_encrypted }}</td>
{% endif %}

{% if application.perfect_forward_secrecy == true %}
  {% if application.perfect_forward_secrecy_source %}
	<td class="green"><a href="{{ application.perfect_forward_secrecy_source }}">Yes</a></td>
	{% else %}
	<td class="green">Yes</td>
	{% endif %}
{% elsif application.perfect_forward_secrecy == false %}
  {% if application.is_locally_encrypted_source %}
	<td class="red"><a href="{{ application.perfect_forward_secrecy_source }}">No</a></td>
	{% else %}
	<td class="red">No</td>
	{% endif %}
{% else %}
	<td>{{ application.perfect_forward_secrecy }}</td>
{% endif %}

{% if application.has_ephemeral_messages == true %}
	<td class="green">Yes</td>
{% elsif application.has_ephemeral_messages == false %}
	<td class="red">No</td>
{% else %}
	<td>{{ application.has_ephemeral_messages }}</td>
{% endif %}

{% if application.encypted_by_default == true %}
  {% if application.encypted_by_default_source %}
	<td class="green"><a href="{{ application.encypted_by_default_source }}">Yes</a></td>
	{% else %}
	<td class="green">Yes</td>
	{% endif %}
{% elsif application.encypted_by_default == false %}
  {% if application.encypted_by_default_source %}
	<td class="red"><a href="{{ application.encypted_by_default_source }}">No</a></td>
	{% else %}
	<td class="red">No</td>
	{% endif %}
{% else %}
	<td>{{ application.encypted_by_default }}</td>
{% endif %}

{% if application.has_contact_verification == true %}
	<td class="green">Yes</td>
{% elsif application.has_contact_verification == false %}
	<td class="red">No</td>
{% else %}
	<td>{{ application.has_contact_verification }}</td>
{% endif %}

{% if application.leaks_files == false %}
	<td class="green">No</td>
{% elsif application.leaks_files contains "?" %}
	<td>{{ application.leaks_files }}</td>
{% else %}
	<td class="red">{{ application.leaks_files }}</td>
{% endif %}


	<td>{{ application.exodus_privacy_trackers_description }}</td>

  <td>{{ application.business_model }}</td>
</tr>
{% endfor %}
</tbody>
</table>

{% assign protocols = site.data.applications | map: "encryption_protocol" | join: ',' | strip_html | replace: ' ,',',' | replace: ', ',',' | split:',' | uniq | sort %}

{% assign trackers = site.data.applications | map: "exodus_privacy_trackers_description" | join: ',' | replace: ' ,',',' | replace: ', ',',' | split:',' | uniq | sort %}

{% capture texts_values %}[['Only recommended'],['{{ final_platforms | split: ',' | sort | join: "','" }}'],['{{ protocols | join: "','"}}'],['{{ trackers | join: "','"}}']]{% endcapture %}
{% capture values_values %}[['*recommended'],['*{{ final_platforms | split: ',' | sort | join: "','*" }}'],['*{{ protocols | join: "','*"}}'],['*{{ trackers | join: "','*"}}']]{% endcapture %}

<script language="javascript" type="text/javascript"> 
    // http://tablefilter.free.fr 
    var tableFilters = {
      remember_grid_values: true,
      status_bar: true,
      display_all_text: "Show all",
      rows_counter: true,
      mark_active_columns: true,
      btn_reset: true,
      col_0: "none",
      col_1: "select",
      col_2: "checklist",
      col_3: "checklist",
      col_4: "select",
      col_5: "select",
      col_6: "checklist",
      col_7: "checklist",
      col_8: "checklist",
      col_9: "checklist",
      col_10: "checklist",
      col_11: "checklist",
      col_12: "checklist",
      col_13: "checklist",
      col_14: "checklist",
      col_15: "checklist",
      col_16: "checklist",
      col_17: "select",
      custom_slc_options: {
        cols:[1,4,5,17],
        texts: {{ texts_values }},
        values: {{ values_values }},
        sorts: [false,false,false,false]
      },
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


