---
layout: index_page
title: Organization of schloss-data folder
---

## Preamble
This page outlines the organizational standards of the `schloss-data` shared directory on our mapped drive. The actual path is `/mnt/EXT/schloss-data`. The goals of this outline are to:

1. Articulate guidlines for preserving organization of shared data.
2. Maximize disk space by minimizing data redundancies and out-of-date files
3. Prevent confusion while differentiating current and legacy versions.
4. Promote a high standard of version control.

## File Structure

### Summary


	schloss-data
	├── archive #Archived data from previous lab members and old projects
	├── bin #Shared scripts that other labbies can use
	├── dbs #Reference databases and datasets
	│   ├── symlinks #Create symlinks to the most up-to-date reference
	│   └── directories_for_references #File storage including fasta, fastq, blastdb
	├── git #Cloned git repositories for each project
	└── users* #Top level directories for eash active lab user


### Example

	schloss-data
	├── archive
	│   ├── users
	│   │   ├── alyx.tar.gz
	│   │   └── zackular.tar.gz
	│   ├── projects
	│   │   ├── schloss_PacBio16S_PeerJ_2016.tar.gz
	│   │   └── Ding_HMP_Nature_2014.tar.gz
	│   └── README.txt
	├── bin
	├── dbs
	│   ├── kegg -> kegg2015
	│   ├── nt -> NcbiNt2016
	│   ├── KeggDatabases
	│   │   ├── kegg2015
	│   │   └── kegg2013
	│   ├── NcbiNt
	│   │   ├── NcbiNt2016
	│   │   ├── NcbiNt2015
	│   │   └── NcbiNt2013
	│   └── README.txt
	├── git
	│   ├── Project_Example_001
	│   ├── HumanMicrobiomeExampleDir
	│   └── README.txt
	├── pdschloss
	├── ghannig
	└── kiverson


## Server Regulations
* Create a new project by [cloning the git repository](https://help.github.com/articles/cloning-a-repository/) from GitHub.
* Projects must be **version controlled** and formatted using the [new project template](https://github.com/schlossLab/new_project).
* The owner of a project not documented in its parent directory README will be notified before file removal.
* Questions, comments, concerns, and high fives can be directed to [Geof Hannigan](ghannig@umich.edu).
