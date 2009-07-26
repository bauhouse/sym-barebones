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
- events/event.publish_article.php
- events/event.save_comment.php
- events/event.save_message.php

All the data sources and events point to the same sections, but these now have different IDs, since everything was rebuilt from the ground up. (I know, it's pretty lame, but I like ID numbers starting from 1 for everything.) 

- CSS and images are not included
- No entries have been created
- The order of the sections has been modified

## Install from BareBones Ensemble ZIP Archive

There are a few ways to install this workspace. Depending on what you prefer, you might like to simply download a complete ZIP file. Go to the downloads area to download the ZIP file, which contains the Symphony 2.0.4 core application, all required extensions, and the BareBones workspace. This is the simplest, if you want to avoid using Git altogether.

## Install BareBones Ensemble via Git

Refer to the [bauhouse/sym-barebones](http://github.com/bauhouse/sym-barebones) or the [official Symphony 2 repository](http://github.com/symphony/symphony-2) for the complete install instructions for Symphony 2. This install may be slightly different than the official symphony-2 repository, as I have updated extensions to the latest releases as of 25 July 2009.

	git clone git://github.com/bauhouse/sym-barebones.git
	git submodule init
	git submodule update

That should be all. Install Symphony as usual. (Find the instructions at the [official Symphony 2 repository](http://github.com/symphony/symphony-2).)

## Install Symphony and BareBones Workspace via Git

The BareBones Ensemble repository brings together the Symphony 2.0.4 core application, the required extensions and the BareBones workspace to simplify the install process. If you'd rather put everything together yourself, the process looks something like this:

	git clone git://github.com/symphony/symphony-2.git

Initialize the submodules

	git submodule init

Update the submodules

	git submodule update
	
At this point, all the files required for a clean install are ready. The second branch that has been included as a submodule is the workspace, which is referring to a specific commit of the barebones branch of my fork of the Symphony workspace repository. To clone this fork separately, use the following commands:

	git clone git://github.com/bauhouse/workspace.git
	cd workspace
	git checkout -b barebones
	git pull origin barebones

