---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: post
---
<main class="page-content" aria-label="Content">
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
