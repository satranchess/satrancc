---
layout: page
title: Haberler
description: Balzac is a new, fluid & responsive theme for Jekyll (and AnchorCMS). It's gloriously beautiful and suited to long form. Built on a SCSS foundation, it's organized and awesome.
menu: yes
image:
  feature: soft-trees.jpg
---

{% for tag in tags %}
	<h2 id="{{ tag | slugify }}">{{ tag }}</h2>
	<ul>
	 {% for post in site.posts %}
		 {% if post.tags contains tag %}
		 <li>
		 <h3>
		 <a href="{{ post.url }}">
		 {{ post.title }}
		 <small>{{ post.date | date_to_string }}</small>
		 </a>
		 {% for tag in post.tags %}
			 <a class="tag" href="/blog/tag/#{{ tag | slugify }}">{{ tag }}</a>
		 {% endfor %}
		 </h3>
		 </li>
		 {% endif %}
	 {% endfor %}
	</ul>
{% endfor %}