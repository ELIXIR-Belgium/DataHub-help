---
title: installing for production
layout: page
redirect_from: "/install-production.html"
---

# Installing SEEK in a production environment

This page contains some extra notes about setting up SEEK for production (i.e.
for real use rather than for development).

By reading and following these extra notes, you will more performance out of
SEEK, and reduce the ongoing maintenance.

If you wish to run under a sub URI, e.g. example.com/seek, then please read and
follow [Installing under a sub URI](install-on-suburi.html) at the end
of the installation.

## Before you install SEEK

This will make sure some of the rake tasks affect the appropriate database.

To save time later there are also some additional packages to install:

    sudo apt-get install libapr1-dev libaprutil1-dev

You will need to install SEEK as the www-data user. First, to make the
installation simpler, give this user a dedicated home directory:

    sudo /etc/init.d/apache2 stop
    sudo usermod -d /home/www-data www-data
    sudo usermod -s /bin/bash www-data
    sudo mkdir /home/www-data
    sudo chown www-data /home/www-data
    sudo /etc/init.d/apache2 start

We recommend installing SEEK in /srv/rails/seek - first you need to create
this and grant permissions to www-data

    sudo mkdir -p /srv/rails
    sudo chown www-data /srv/rails

Now switch to the www-data user

    sudo su - www-data
    cd /srv/rails

Before following the standard INSTALL guide you need to set an environment
variable to indicate that you intend to setup and run SEEK as production.

    export RAILS_ENV=production

you will need to reset this variable if you close your shell and start a new
session


You can now follow the overall [Installation Guide](install.html), and
then return to this page for some additional steps to get SEEK running
together with Apache, and also automating the required services.

If you have problems with requiring a sudo password during the RVM steps -
first setup RVM and ruby-1.9.3 as a user with sudo access, and repeat the
steps as the www-data user. This means the required packages should then be
installed. At the time of writing this guide this shouldn't be necessary.

## After you have installed SEEK

## Compiling Assets

Assets - such as images, javascript and stylesheets, need to be precompiled -
which means minifying them, grouping some together into a single file, and
compressing. These then get placed into *public/assets*. To compile them run
the following command. This can take some time, so be patient

    bundle exec rake assets:precompile

### Serving SEEK through Apache

First you need to setup [Passenger Phusion](https://www.phusionpassenger.com/)
.Still as the www-data user, run the command:

    bundle exec passenger-install-apache2-module

This will compile a module for Apache, and at the end present you with some
lines that need adding to /etc/apache2/apache2.conf. These will look something
like the following, but the paths will most likely be different:

    LoadModule passenger_module /home/www-data/.rvm/gems/ruby-2.2.7/gems/passenger-5.1.2/buildout/apache2/mod_passenger.so
    <IfModule mod_passenger.c>
      PassengerRoot /home/www-data/.rvm/gems/ruby-2.2.7/gems/passenger-5.1.2
      PassengerDefaultRuby /home/www-data/.rvm/gems/ruby-2.2.7/wrappers/ruby
    </IfModule>

You will need to be a user that has sudo permissions, and edit this file:

    sudo nano /etc/apache2/apache2.conf

Now create a virtual host definition for SEEK:

    sudo nano /etc/apache2/sites-available/seek.conf

which looks like (if you have registered a DNS for your site, then set
ServerName appropriately):

    <VirtualHost *:80>
      ServerName www.yourhost.com
      DocumentRoot /srv/rails/seek/public
       <Directory /srv/rails/seek/public>
          # This relaxes Apache security settings.
          Allow from all
          # MultiViews must be turned off.
          Options -MultiViews
          Require all granted
       </Directory>
       <LocationMatch "^/assets/.*$">
          Header unset ETag
          FileETag None
          # RFC says only cache for 1 year
          ExpiresActive On
          ExpiresDefault "access plus 1 year"
       </LocationMatch>
    </VirtualHost>

The LocationMatch block tells Apache to serve up the assets (images, CSS,
Javascript) with a long expiry time, leading to better performance since these
items will be cached. You may need to enable the *headers* and *expires*
modules for Apache, so run:

    sudo a2enmod headers
    sudo a2enmod expires

Now enable the SEEK site, and disable the default that is installed with
Apache, and restart:

    sudo a2ensite seek
    sudo a2dissite 000-default
    sudo service apache2 restart

If you now visit http://localhost (note there is no 3000 port) - you should
see SEEK.

If you wish to restart SEEK, maybe after an upgrade, without restarting Apache
you can do so by running (as www-data)

    touch /srv/rails/seek/tmp/restart.txt
    
### Configuring for HTTPS

We would strongly recommend using [Lets Encrypt](https://letsencrypt.org/) for free SSL certificates.     

### Setting up the services

The following steps show how to setup delayed_job and
soffice to run as a service, and automatically start and shutdown when you
restart the server. Apache Solr should already be setup from following the [Setting up Solr](setting-up-solr) instructions.


#### Delayed Job Background Service

Create the file /etc/init.d/delayed_job-seek and copy the contents of
[scripts/delayed_job-seek](scripts/delayed_job-seek) into it.

The run:

    sudo chmod +x /etc/init.d/delayed_job-seek
    sudo update-rc.d delayed_job-seek defaults

start it up with:

    sudo /etc/init.d/delayed_job-seek start

