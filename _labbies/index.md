---
layout: index_page
category: labbies
title: Labbies
---

The members of the Schloss Lab represent a diverse array of backgrounds, interests, and goals.

{% assign page_array = site.labbies | where:"status", "current"		%}
{% include picture_grid.html pages=page_array columns=4	%}



<h3>Alumni</h3>
<p>While we hate to say goodbye, our goal is to train people and then send them on to greener pastures. It is not an exaggeration to say that the present state of the lab is due in large part to the many contributions of those that have worked with us over the years.</p>

{% assign page_array = site.labbies | where:"status","alumni"		%}
{% include picture_grid.html pages=page_array columns=4				%}
