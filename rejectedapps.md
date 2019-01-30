---

title: Rejected Apps
---
These apps are strongly not recommended for various reasons, including not being end-to-end encrypted (E2EE), abondoned projects, geared towards enterprise environments, cost too much or have serious security problems.<br>
<br>
<p id="note2ee">Apps that are not E2EE:</p>
<ul>
  {% assign applications = site.data.applications | where_exp: "item","item.category == 10" | sort: 'name' %}
  {% for application in applications %}
  <li id="{{ application.name }}">{{ application.display_name }}</li>
  {% endfor %}
</ul>
<br>
<p>Apps not recommended for other reasons:</p>
<ul>
  {% assign applications = site.data.applications | where_exp: "item","item.category == 11" | sort: 'name' %}
  {% for application in applications %}
  <li id="{{ application.name }}">{{ application.display_name }}- {{ application.notes_text }}
    {% endfor %}
</ul>
