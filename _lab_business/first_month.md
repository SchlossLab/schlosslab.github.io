---
layout: index_page
title: It's your first month in the lab, now what?
---

Very few people join the lab with the foundation to do reproducible microbial ecology analysis or an appreciation for how to analyze microbiome data. Over time, we've found a set of tools are pretty critical to success in the lab. We think of this as our [full stack](https://en.wikipedia.org/wiki/Solution_stack) for doing the analytical end as a microbial ecologist who is concerned about the reproducibility of their analysis. Don't feel like you need to master this stack in your first week or month of being in the lab. By going through these tutorials and actually using the tools in your daily work you'll eventually get it. Also, we pride ourselves on being an inclusive community that wants to help each other to grow in these skills. Trust us, before long, you will be helping us with something you assumed we all knew.

The Schloss Lab Full Stack includes: mothur, R, knitr, git, bash, and make. In your first month of being in the lab, you should do the following tutorials and do them all on Great Lakes, the high performance computer cluster that the lab uses. If you run into any problems ask Pat, it's very likely that you have run into a common problem or that the problem isn't your fault:


### The Curriculum
* Getting a Great Lakes account
  * Email <a href="mailto:hpc-support@umich.edu">Great Lakes Help</a> and tell them to add your uniqname to the Schloss Lab Great Lakes allocation and our Turbo storage allocatio. cc Pat on your email to the Great Lakes Help people (technically they're part of ARC-TS) since Pat will have to approve your request
  * Complete and submit the [Great Lakes account form](https://arc-ts.umich.edu/login-request/)
* Become familiar with Great Lakes (be sure to check out the [life hacks](lab_life_hacks.html) page)
  * `ssh greatlakes.arc-ts.umich.edu`
  * `cd /nfs/turbo/schloss-lab`
  * `mkdir [your uniqname]`
  * `cd [your uniqname]`
  * Next time you log in you can do `cd /nfs/turbo/schloss-lab/[your uniqname]` to get back to this point.
* The tools we use
	- bash: [Software Carpentry bash tutorial](http://swcarpentry.github.io/shell-novice/)
	- mothur: [MiSeq SOP](http://www.mothur.org/wiki/MiSeq_SOP) and the [Kozich et al. (2013) paper](/assetts/pdfs/2013_kozich.pdf)
	- R: [minimalR](http://www.riffomonas.org/minimalR)
	- git, knitr, bash, make: [Reproducible research tutorial](http://www.riffomonas.org/reproducible_research)
	- Fork [lab website source code](https://www.github.com/SchlossLab/schlosslab.github.io) and submit a pull request to add a file with your information and a picture
* [Read the papers](/papers) where Pat is first or last author from last 2 yrs and then dig into the rest of the literature


You can supplement those materials with these tutorials and cheat sheets:

* bash
  * [Codecademy materials](https://www.codecademy.com/learn/learn-the-command-line)
* R and knitr
	* [R Cheatsheets](https://www.rstudio.com/resources/cheatsheets/)
  * [Rmarkdown materials](http://rmarkdown.rstudio.com)
  * [Software Carpentry Workshop tutorial 1](http://swcarpentry.github.io/r-novice-inflammation/)
  * [Software Carpentry Workshop tutorial 2](http://swcarpentry.github.io/r-novice-gapminder/)
* git
  * [Software Carpentry Workshop tutorial](http://swcarpentry.github.io/git-novice/)
  * [Codecademy materials](https://www.codecademy.com/learn/learn-git)
* make
  * [Software Carpentry Workshop tutorial](http://swcarpentry.github.io/make-novice/)


### Useful software
We are primarily a Mac/Linux lab and we make use of a Linux-based computer cluster. Thankfully the tool set that we use can be ported to any operating system.

* For Windows users one of
  * [git bash](https://git-for-windows.github.io) and [PuTTY](http://www.putty.org)
  * [enable Bash on Windows 10](http://stackoverflow.com/questions/36352627/how-to-enable-bash-in-windows-10-developer-preview)
* [mothur](https://github.com/mothur/mothur/releases)
* [R](https://www.r-project.org)
	* [Desktop RStudio](https://www.rstudio.com) to make interacting with R easier
	* [RStudio via ARC-Connect](greatlakes.arc-ts.umich.edu) to connect to RStudio on Great Lakes [ On the top of the page when it loads you should see a dropdown menu for "Interactive Apps". You can select Rstudio from there; off campus access requires using the VPN ]
* Text editor (what you use is a personal preference):
	* [Atom](https://atom.io)
	*	[Sublime Text](https://www.sublimetext.com)
	* [TextWrangler](https://itunes.apple.com/us/app/textwrangler/id404010395?mt=12)
	* [vim](http://www.vim.org)
	* [emacs](https://www.gnu.org/software/emacs/)
* Paper management software (this is a personal preference):
	* [Papers](http://www.papersapp.com)
	* [Zotero](https://www.zotero.org)
