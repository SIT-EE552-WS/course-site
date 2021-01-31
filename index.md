---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: post
---
<main class="page-content" aria-label="Content">
<h2>Table of Contents</h2>
<table>
<thead>
<tr>
<th>Week</th>
<th>Assigment</th>
<th>Title</th>
</tr>
</thead>
<tbody>
{% for assignment in site.assignments %}
<tr>
<td>{{assignment.week}}</td>
<td>{{assignment.homework}}</td>
<td><a href="{{assignment.url}}">{{assignment.title}}</a></td>
</tr>
{% endfor %}
</tbody>
</table>
<div class="wrapper">
{% for assignment in site.assignments %}
  <article class="post h-entry">
  <h2><a href="{{ assignment.url }}"> Homework {{assignment.week}}.{{assignment.homework}} - {{ assignment.title }}</a></h2>
  <p>{{ assignment.content | markdownify }}</p>
  </article>
{% endfor %}
</div>
</main>

<link rel="stylesheet" href="/assets/main.css">
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
