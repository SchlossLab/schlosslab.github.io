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

*Clostridium difficile* infection (CDI) following therapeutic antibiotic treatment represents a considerable threat to human health, each year causing as many as half a million infections, 29,000 deaths, and a healthcare burden of $4.8 million. CDI can cause severe abdominal pain and diarrhea, and can develop the life-threatening conditions, which it accomplishes through secretion of protein toxins. Infections in healthy individuals are uncommon, as the combination of the innate immune system and gut microbiome prevent colonization under ordinary circumstances. However, disruption of the native gut bacterial communities during antibiotic therapy, often for unrelated illness, provides opportunity for *C. difficile* to establish infection. Subsequent treatment of CDI with antibiotics is typically effective, but recurrence of disease is common and may be increasing in prevalence. This, in combination with increased prevalence of infection, the emergence of more virulent forms of the pathogen, and the ever-present threat of antibiotic resistance highlight the need to better understand the mechanisms by which the gut immune system and the resident microbiota prevent initial colonization and subsequent recurrence by *C. difficile*. We use a combination of 16S rRNA gene sequencing, metagenomics, metatranscriptomics, and metabolomics in a mouse model for CDI and in infected patients to identify microbial functions that are important for colonization resistance and clearance of *C. difficile*.

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
