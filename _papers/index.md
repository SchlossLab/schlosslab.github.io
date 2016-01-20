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

<ol>

	{%	for pub in site.papers reversed	%}
		{% if pub.layout != "index_page"%}
		<li>
			<b>{{ pub.authors }}.</b>
			{{ pub.year }}.
			{{ pub.title }}.
			<i>{{ pub.journal }}</i>.

			{% if pub.volume %}
			<b>{{ pub.volume }}:</b>
			{% endif %}

			{{ pub.pages }}.

			{% if pub.doi %}
			DOI: <a href="http://doi.org/{{pub.doi}}">{{pub.doi}}</a>.
			{% endif %}


			<div class="supp">
				<a href="{{ pub.url | replace:'yml','pdf' | replace:'papers','assets/pdf'}}">
					<i class="fa fa-file-pdf-o fa-lg"></i>
				</a>
				{% if pub.github	%}
					<a href="https://github.com/SchlossLab/{{ pub.github }}">
						<i class="fa fa-github fa-lg" ></i>
					</a>
				{% endif			%}

				{% if pub.data		%}
					<a href="{{pub.data}}">
						<i class="fa fa-table fa-lg" ></i>
					</a>
				{% endif			%}

				{% if pub.google_scholar	%}
				<a href="{{pub.google_scholar}}">
					<i class="ai ai-google-scholar ai-lg"></i>
				</a>
				{% endif			%}

			</div>

		</li>
		{% endif %}
	{%	endfor %}
</ol>
</div>
