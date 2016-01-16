---
layout: default
category: posts
title: News
---

<div class="news">
	<ul>
	  {% for post in site.categories.news %}
			<li>
				<a class="title" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
				<p class="meta">{{ post.date | date: "%b %-d, %Y" }}{% if post.author %} • {{ post.author }}{% endif %}</p>
				<div class="content">
					{{ post.excerpt }}
				</div>
			</li>
	  {% endfor %}
	</ul>
</div>
