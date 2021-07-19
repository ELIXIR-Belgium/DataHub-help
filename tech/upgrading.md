---
title: upgrading seek
layout: page
redirect_from: "/upgrading.html"
---

# Upgrading SEEK

If you have an existing SEEK installation, and you haven't done so already,
please take a moment to fill out our very short,optional [SEEK Registration
Form](http://www.seek4science.org/seek-registration). Doing so will be very useful
to us in the future when we try and raise further funding to develop and
support SEEK and the associated tools.

**Always backup your SEEK data before starting to upgrade!!** - see the
[Backup Guide](backups.html).

This guide assumes that SEEK has been installed following the [Installation
Guide](install.html). It assumes it is a production server that is
being updated, and that commands are run from the root directory of the SEEK
application.


## Identifying your version

The version of SEEK you are running is shown at the bottom left, within the
footer, when viewing pages in SEEK.

You can also tell which version you have installed by looking at the
*config/version.yml* file, so for example version 0.13.2 looks something like:

    major: 0
    minor: 13
    patch: 2


## Upgrading between patch versions (e.g. between 1.4.0 and 1.4.1) 

When upgrading between patch versions, it should only be necessary to run 
    
    bundle install
    bundle exec rake seek:upgrade 

## Steps to upgrade from 1.10.x to 1.11.x

### Upgrading Ruby

You will need to upgrade Ruby to Ruby 2.6.6. If you are using [RVM](https://rvm.io/) (according to the [Installation Guide](install.html) )you should be prompted to install during the standard installation steps that follow.
If you are not prompted you can install with the command:

    rvm install ruby-2.6.6

### Set RAILS_ENV
              

**If upgrading a production instance of SEEK, remember to set the RAILS_ENV first**

    export RAILS_ENV=production

### Stopping services before upgrading

    bundle exec rake seek:workers:stop
    bundle exec rake sunspot:solr:stop

### Updating from GitHub

If you have an existing installation linked to our GitHub, you can fetch the
files with:

    git pull
    git checkout v1.11.1

### Updating using the tarball

You can download the file from
<https://github.com/seek4science/seek/archive/v1.11.1.tar.gz> You can
unpack this file using:

    tar zxvf seek-1.11.1.tar.gz
    mv seek seek-previous
    mv seek-1.11.1 seek
    cd seek/

and then copy across your existing filestore and database configuration file
from your previous installation and continue with the upgrade steps. The
database configuration file you would need to copy is _config/database.yml_,
and the filestore is simply _filestore/_

If you have a modified _config/sunspot.yml_ you will also need to copy that across.

### Doing the upgrade

After updating the files, the following steps will update the database, gems,
and other necessary changes. Note that seek:upgrade may take longer than usual if you have data stored that points to remote
content.

**Please note** - during the upgrade the step _Updating session store_ can take a long time and appear that it has frozen, so please be patient. 

    cd . #this is to allow RVM to pick up the ruby and gemset changes
    gem install bundler
    bundle install --deployment
    bundle exec rake seek:upgrade
    bundle exec rake assets:precompile # this task will take a while       

### Setup Cron Services

This version includes an update to ActiveJob and requires some cron jobs for periodic background jobs to run. To set these up run:

    bundle exec whenever --update-crontab

### Restarting services

    bundle exec rake sunspot:solr:start
    bundle exec rake seek:workers:start                
    
    bundle exec rake tmp:clear  

           
---
    
## Earlier upgrade notes

For details of how to upgrade between earlier versions please visit
[Upgrades between earlier versions](earlier-upgrades.html)
