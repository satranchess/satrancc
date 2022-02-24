---
layout: page
title: Haberler
description: Balzac is a new, fluid & responsive theme for Jekyll.
menu: yes
image:
  feature: soft-trees.jpg
---

{% for tag in tags %}
	<ul>
	 {% for post in site.posts %}
		 {% if post.tags contains tag %}
		 <li>
		 <a href="{{ post.url }}">
		 {{ post.title }}
		 <small>{{ post.date | date_to_string }}</small>
		 </a>
		 </li>
		 {% endif %}
	 {% endfor %}
	</ul>
{% endfor %}