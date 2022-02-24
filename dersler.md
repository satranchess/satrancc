---
layout: page
title: "Dersler"
menu: yes
tag: ders
image:
  feature: soft-trees.jpg
---

<ul class="tags">
{% for tag in site.tags %}
  {% assign t = tag | first %}
  {% assign posts = tag | last %}
  <li>{{t | downcase | replace:" ","-" }} has {{ posts | size }} posts</li>
{% endfor %}
</ul>