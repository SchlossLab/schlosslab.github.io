---
layout: default
category: posts
---

<div class="news">

	<ul>
	  {% for post in site.categories.diary %}
			<li>
				<a class="diary-title" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
				<p class="post-meta">{{ post.date | date: "%b %-d, %Y" }}{% if post.author %} • {{ post.author }}{% endif %}</p>
				{{ post.excerpt }}
			</li>
	  {% endfor %}
	</ul>
</div>
</div>
