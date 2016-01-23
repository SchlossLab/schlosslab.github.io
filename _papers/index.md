---
layout: index_page
category: papers
title: Papers
---

<div class="bibliography">

<div class="legend">
	<h4>Legend</h4>
	<ul>
		<li><i class="fa fa-file-pdf-o fa-lg"></i> PDF version of paper</li>
		<li><i class="fa fa-github fa-lg" ></i> GitHub repository of paper with reproducible version of manuscript</li>
		<li><i class="fa fa-table fa-lg" ></i> Raw data used in manuscript</li>
		<li><i class="ai ai-google-scholar ai-lg"></i> Google Scholar page</li>
	</ul>
</div>

<ol reversed>
	{% assign this_year = (site.time | date: '%Y') %}

	{% for year in (2000..this_year) reversed %}
		{% assign year_array = site.papers | where:"year", year		%}

		{% for pub in year_array 	%}
			{% if pub.layout != "index_page"%}
				<li>
					{% include reference.html ref=pub%}
				</li>
			{% endif %}
		{% endfor %}
	{% endfor %}
</ol>
</div>
