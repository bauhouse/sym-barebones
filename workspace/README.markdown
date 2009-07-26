# BareBones Workspace

The BareBones workspace is a modified workspace for Symphony 2.0.4. The main difference between this install and the official version is that this version has been rebuilt from a clean install with exactly the same structure as the default Spectrum theme. The only files that are different are:

- install.sql
- data-sources/data.archive.php
- data-sources/data.article_images.php
- data-sources/data.article.php
- data-sources/data.comments.php
- data-sources/data.drafts.php
- data-sources/data.homepage_articles.php
- data-sources/data.navigation.php
- data-sources/data.notes.php
- data-sources/data.rss_articles.php
- data-sources/data.website_owner.php

All the data sources point to the same sections, but these now have different IDs, since everything was rebuilt from the ground up. (I know, it's pretty lame, but I like ID numbers starting from 1 for everything.) 

- CSS and images are not included
- No entries have been created
- The order of the sections has been modified

## Install

The BareBones Ensemble repository brings together the [Symphony 2.0.4](http://github.com/symphony/symphony-2/tree/master) core application, the required extensions and the [BareBones workspace](http://github.com/bauhouse/workspace/tree/barebones) to simplify the install process.

### Install from BareBones Ensemble ZIP Archive

Go to the [Downloads](http://github.com/bauhouse/workspace/downloads) page to download the ZIP file. This is the simplest, if you want to avoid using Git altogether.

### Install BareBones Ensemble via Git

This repository has been created to make the installation as simple as possible. A single Git command will provide all that you need:

	git clone git://github.com/bauhouse/sym-barebones.git

That should be all. Install Symphony as usual. (Find the instructions at the [official Symphony 2 repository](http://github.com/symphony/symphony-2).) For convenience, they have been included below:

### Install Symphony and BareBones Workspace via Git

If you'd rather put everything together yourself, the process looks something like this:

Clone my fork of the Symphony 2 repository

	git clone git://github.com/bauhouse/symphony-2.git

Rename the directory from `symphony-2` to `test`

	mv symphony-2 test

Change the current working directory to `test`

	cd test

Create a new branch called `barebones`

	git checkout -b barebones

Pull the changes from the GitHub repository for the barebones branch

	git pull origin barebones

Initialize the submodules

	git submodule init

Update the submodules

	git submodule update
	
At this point, all the files required for a bare bones install are ready. The second branch that has been included as a submodule is the workspace, which is referring to a specific commit of the [barebones branch](http://github.com/bauhouse/symphony-2/tree/barebones) of my fork of the Symphony workspace repository. To clone this fork separately, use the following commands:

	git clone git://github.com/bauhouse/workspace.git
	cd workspace
	git checkout -b barebones
	git pull origin barebones


