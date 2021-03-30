---
title: Projects
---

<main class="page-content" aria-label="Content">
<h2>Table of Contents</h2>
<table>
<thead>
<tr>
<th>Title</th>
</tr>
</thead>
<tbody>
{% for project in site.projects %}
{% if project.title != 'Projects' %}
<tr>
<td><a href="{{project.url}}">{{project.title}}</a></td>
</tr>
{% endif %}
{% endfor %}
</tbody>
</table>
</main>
