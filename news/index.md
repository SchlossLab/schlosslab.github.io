---
layout: index_page
category: posts
title: News
---

<div class="news">
	<ul>
	  {% for post in site.categories.news %}
			<li>
				<div class="title">{{ post.title }}</div>
				<p class="meta">{{ post.date | date: "%b %-d, %Y" }}{% if post.author %} • {{ post.author }}{% endif %}</p>
				<div class="content">

					{%	assign excerpt_count = post.excerpt | number_of_words	%}
					{%	assign content_count = post.content | number_of_words	%}
					{%	if excerpt_count != content_count						%}

						{{ post.excerpt | remove: '</p>' }}
						<a class="read-more" href="{{ post.url | prepend: site.baseurl }}">Read more...</a></p>
					{% else													%}
						{{ post.excerpt }}
					{% endif													%}

				</div>
			</li>
	  {% endfor %}
	</ul>
</div>
