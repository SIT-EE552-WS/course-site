---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
---
<main class="page-content" aria-label="Content">
<div class="wrapper">
{% for assignment in site.assignments %}
  <article class="post h-entry">
  <h2>Week {{assignment.week}} - HW {{assignment.homework}} - {{ assignment.name }}</h2>
  <p>{{ assignment.content | markdownify }}</p>
  </article>
{% endfor %}
</div>
</main>
<link rel="stylesheet" href="/assets/main.css">
<link type="application/atom+xml" rel="alternate" href="http://localhost:4000/feed.xml" title="EE552 - Introduction to Programming in Java" />
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
