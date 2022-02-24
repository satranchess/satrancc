---
layout: page
title: "Dersler"
menu: yes
image:
  feature: soft-trees.jpg
---

{% for post in site.tags.ders %}
 <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}