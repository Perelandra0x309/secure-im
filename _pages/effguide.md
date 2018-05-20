---
layout: default
title: EFF Messenger choosing Guide
permalink: /effguide.html
---

<script>
function setFilters() {
  // Declare variables 
  var input, filterRec, filterEph, filterID, filterFoolproof, filterPuddle, filterHammer, filterVer, table, tr, td, i;
  input = document.getElementById("onlyRec");
  filterRec = input.checked;
  input = document.getElementById("ephemCB");
  filterEph = input.checked;
  input = document.getElementById("idCB");
  filterID = input.checked;
  input = document.getElementById("foolproofCB");
  filterFoolproof = input.checked;
  input = document.getElementById("puddleCB");
  filterPuddle = input.checked;
  input = document.getElementById("hammerCB");
  filterHammer = input.checked;
  input = document.getElementById("verifyCB");
  filterVer = input.checked;
  table = document.getElementById("myTable");
  tr = table.getElementsByTagName("tr");

  // Loop through all table rows, and hide those who don't match the search query
  for (i = 0; i < tr.length; i++) {
    td = tr[i].getElementsByTagName("td")[9];
    if (td) {
      if (filterRec && td.innerHTML > 2) {
        tr[i].style.display = "none";
      } else if (filterEph && tr[i].getElementsByTagName("td")[3].innerHTML != "Yes"){
        tr[i].style.display = "none";
      } else if (filterID && tr[i].getElementsByTagName("td")[4].innerHTML != "No"){
        tr[i].style.display = "none";
      } else if (filterFoolproof && tr[i].getElementsByTagName("td")[5].innerHTML != "Yes"){
        tr[i].style.display = "none";
      } else if (filterPuddle && tr[i].getElementsByTagName("td")[6].innerHTML != "Yes"){
        tr[i].style.display = "none";
      } else if (filterHammer && tr[i].getElementsByTagName("td")[7].innerHTML != "Yes"){
        tr[i].style.display = "none";
      } else if (filterVer && tr[i].getElementsByTagName("td")[8].innerHTML != "Yes"){
        tr[i].style.display = "none";
      } else {
        tr[i].style.display = "";
      }
    }
  }
}
</script>

<br>
Read EFF's <a href="https://www.eff.org/deeplinks/2018/03/thinking-about-what-you-need-secure-messenger">Thinking About What You Need In A Secure Messenger</a>.
<br>
<ul>
  <li>Are you worried about your messages being intercepted by governments or service providers?<br>
    Solution: End-to-end encryption<br>
    All messengers listed on this page will have full end to end encryption as an option.<br>
  </li>
  <li>Are you worried about people in your physical environment reading your messages?<br>
  Solution: ephemeral or “disappearing” messages<br>
  </li>
  <li>Do you want to avoid giving out your phone number (or email)?<br>
  Solution: Messengers that allow aliases (and do not expose your personal information as part of your ID)<br>
  </li>
  <li>How risky would a mistake be? Do you need a “foolproof” encrypted messenger?<br>
  Solution: Only encrypted communication is possible<br>
  </li>
  <li>Are you more concerned about the the “Puddle Test” or the “Hammer Test”?<br>
  “Puddle Test”: If you accidentally dropped your phone in a Puddle and ruined it, would your messages be lost forever? Would you be able to recover them? Note that the No marked in yellow means that not passing the puddle test may be something you DO want.  Not passing this test could be desirable or not depending on your use case.<br>
  “Hammer Test”: If you and a contact intentionally took a Hammer to your phones or otherwise tried to delete all your messages, would they really be deleted? Would someone else be able to recover them?<br>
  </li>
  <li>Do you need features to help you verify the identity of the person you’re talking to?<br>
  Solution: contact verification<br>
  </li>
</ul>
<br>
<input type="checkbox" id="onlyRec" onchange="setFilters()" name="onlyRec" value="false"> <label for="onlyRec">Show only recommended apps</label><br>
<br>
Show apps that have:<br>
<input type="checkbox" id="ephemCB" onchange="setFilters()" name="ephemCB" value="false"> <label for="ephemCB">Ephemeral Messages</label><br>
<input type="checkbox" id="idCB" onchange="setFilters()" name="idCB" value="false"> <label for="idCB">ID contains no personal info</label><br>
<input type="checkbox" id="foolproofCB" onchange="setFilters()" name="foolproofCB" value="false"> <label for="foolproofCB">Foolproof encryption</label><br>
<input type="checkbox" id="puddleCB" onchange="setFilters()" name="puddleCB" value="false"> <label for="puddleCB">Passes Puddle test</label><br>
<input type="checkbox" id="hammerCB" onchange="setFilters()" name="hammerCB" value="false"> <label for="hammerCB">Passes Hammer test</label><br>
<input type="checkbox" id="verifyCB" onchange="setFilters()" name="verifyCB" value="false"> <label for="verifyCB">Has contact verification</label><br>

{% assign applications = site.data.applications | where_exp: "item","item.category < 7" | sort: 'name' %}
<table id="myTable">
<th>Name</th>
<th>Platforms</th>
<th width="11%">Country of Origin</th>
<th width="11%">Ephemeral Messages</th>
<th width="11%">ID contains personal info</th>
<th width="11%">Foolproof (All Messages Encrypted)</th>
<th width="11%">Passes Puddle Test</th>
<th width="11%">Passes Hammer Test</th>
<th width="11%">Has Contact Verification</th>
<th style="display:none">Recomendation</th>

{% for application in applications %}
<tr>
	<td>{% include generate_app_link.html app_name="application.name" %}</td>
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

{% if application.has_ephemeral_messages == true %}
	<td bgcolor="green">Yes</td>
{% elsif application.has_ephemeral_messages == false %}
	<td bgcolor="red">No</td>
{% else %}
	<td>{{ application.has_ephemeral_messages }}</td>
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

{% if application.encypted_by_default == true %}
	<td bgcolor="green">Yes</td>
{% elsif application.encypted_by_default == false %}
	<td bgcolor="red">No</td>
{% else %}
	<td>{{ application.encypted_by_default }}</td>
{% endif %}

{% if application.passes_puddle_test == true %}
	<td bgcolor="green">Yes</td>
{% elsif application.passes_puddle_test == false %}
	<td class="yellow">No</td>
{% else %}
	<td>{{ application.passes_puddle_test }}</td>
{% endif %}

{% if application.passes_hammer_test == true %}
	<td bgcolor="green">Yes</td>
{% elsif application.passes_hammer_test == false %}
	<td bgcolor="red">No</td>
{% else %}
	<td>{{ application.passes_hammer_test }}</td>
{% endif %}

{% if application.has_contact_verification == true %}
	<td bgcolor="green">Yes</td>
{% elsif application.has_contact_verification == false %}
	<td bgcolor="red">No</td>
{% else %}
	<td>{{ application.has_contact_verification }}</td>
{% endif %}

	<td style="display:none">{{ application.recommendation }}</td>
</tr>
{% endfor %}

</table>
<!-- Page updated {{ page.date }}<br> -->
