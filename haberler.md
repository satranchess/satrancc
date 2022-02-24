---
layout: page
title: Haberler
description: Balzac is a new, fluid & responsive theme for Jekyll (and AnchorCMS). It's gloriously beautiful and suited to long form. Built on a SCSS foundation, it's organized and awesome.
menu: yes
image:
  feature: soft-trees.jpg
---

{% for tag in site.tags %}
  {% assign t = tag | first %}
  {% assign posts = tag | last %}

{{ t | downcase }}
<ul>
{% for post in posts %}
  {% if post.tags contains t %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <span class="date">{{ post.date | date: "%B %-d, %Y"  }}</span>
  </li>
  {% endif %}
{% endfor %}
</ul>
{% endfor %}