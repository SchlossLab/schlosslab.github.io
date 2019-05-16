---
layout: index_page
category: science
title: Science
---

### Colorectal cancer

There are 1.4 million people in the US with a history of colorectal cancer (CRC). Although the mortality rate has declined in recent decades, incidence rates are expected to rise due to the aging population and increasing occurrence of CRC in younger individuals. Cancerous or precancerous cells in the colon form lesions which are typically detected via colonoscopy, but the technique is invasive, expensive, and only 39% of patients return for subsequent screening. There is a need for improved non-invasive screening methods. We are using an innovative source to detect CRC: the human microbiome. Human microbiome can directly contribute to the development of CRC. We try to identify microbial biomarkers associated with CRC and to develop computational models that improve the non-invasive detection of CRC.


{% assign section_papers = site.array %}
{% for paper in site.papers reversed %}
	{% if paper.section contains "cancer" %}
		{% assign section_papers = section_papers | push: paper %}
	{% endif %}
{% endfor %}

{% assign paper_count = section_papers | size %}
{% if paper_count > 0 %}
	{% assign sorted_papers = section_papers | sort: 'year' | reverse %}

<div class="papers">
	<ol>
		{% for paper in sorted_papers %}
			{% if paper.layout == "chapter" %}
				<li>{% include reference_chapter.html ref=paper %}</li>
			{% else %}
				<li>{% include reference_paper.html ref=paper %}</li>
			{% endif %}
		{% endfor %}
	</ol>
</div>

{% endif %}




### *Clostridium difficile* Infection

{% assign section_papers = site.array %}
{% for paper in site.papers reversed %}
	{% if paper.section contains "cdiff" %}
		{% assign section_papers = section_papers | push: paper %}
	{% endif %}
{% endfor %}

{% assign paper_count = section_papers | size %}
{% if paper_count > 0 %}
	{% assign sorted_papers = section_papers | sort: 'year' | reverse %}

<div class="papers">
	<ol>
		{% for paper in sorted_papers %}
			{% if paper.layout == "chapter" %}
				<li>{% include reference_chapter.html ref=paper %}</li>
			{% else %}
				<li>{% include reference_paper.html ref=paper %}</li>
			{% endif %}
		{% endfor %}
	</ol>
</div>

{% endif %}




### Bioinformatic tool development


{% assign section_papers = site.array %}
{% for paper in site.papers reversed %}
	{% if paper.section contains "tools" %}
		{% assign section_papers = section_papers | push: paper %}
	{% endif %}
{% endfor %}

{% assign paper_count = section_papers | size %}
{% if paper_count > 0 %}
	{% assign sorted_papers = section_papers | sort: 'year' | reverse %}

<div class="papers">
	<ol>
		{% for paper in sorted_papers %}
			{% if paper.layout == "chapter" %}
				<li>{% include reference_chapter.html ref=paper %}</li>
			{% else %}
				<li>{% include reference_paper.html ref=paper %}</li>
			{% endif %}
		{% endfor %}
	</ol>
</div>

{% endif %}


### Scientific culture

{% assign section_papers = site.array %}
{% for paper in site.papers reversed %}
	{% if paper.section contains "culture" %}
		{% assign section_papers = section_papers | push: paper %}
	{% endif %}
{% endfor %}

{% assign paper_count = section_papers | size %}
{% if paper_count > 0 %}
	{% assign sorted_papers = section_papers | sort: 'year' | reverse %}

<div class="papers">
	<ol>
		{% for paper in sorted_papers %}
			{% if paper.layout == "chapter" %}
				<li>{% include reference_chapter.html ref=paper %}</li>
			{% else %}
				<li>{% include reference_paper.html ref=paper %}</li>
			{% endif %}
		{% endfor %}
	</ol>
</div>

{% endif %}
