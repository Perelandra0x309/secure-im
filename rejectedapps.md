---

title: Rejected Applications
---

<p>Apps that are not E2EE:</p>
<ul>
  {% assign applications = site.data.applications | where_exp: "item","item.category == 10" | sort: 'name' %}
  {% for application in applications %}
  <li><a name="{{ application.name }}"></a>{{ application.display_name }}</li>
  {% endfor %}
</ul>
<br>
<p>Apps not recommended for other reasons:</p>
<ul>
  {% assign applications = site.data.applications | where_exp: "item","item.category == 11" | sort: 'name' %}
  {% for application in applications %}
  <li><a name="{{ application.name }}"></a>{{ application.display_name }}- {{ application.notes_text }}
    {% endfor %}
</ul>
