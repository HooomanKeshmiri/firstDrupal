
# firstDrupalSite: Test Drupal website on with Drupal8 recipe 
This is a basic Drupal website that was developed through Lando with a Drupal8 recipe. The goal of this project was to get familiar with both making content directly with Drupal as well as using Lando to initialize the website.
#
## Description:
This application is a website that can be navigated by anyone and was made in Drupal. It can be used by anyone to get familiar with both using Drupal. It is recommended that if you are to download the files and launch the website that you use Lando to both initialize and launch the site. The Lando installation guide will be posted further below. To develop the web page Drupal was used as this is a predecessor to a project that I will be on using Drupal and I needed to learn how to use Drupal effectively.

#

## Installation:

Downloading Lando: https://docs.lando.dev/basics/installation.html

To use this web page first download the code base from github. Following that install Lando on your device and in the repository that you cloned.  

Type `lando start` to have lando build the app in the container. Once this is completed you can use `lando info` to have lando display the database information you need to install drupal such as database name, password, and the host. After this you can either paste the url given by lando into your web browser, or use `open yourURL.lndo.site` into the terminal. The webpage will open and follow the instructions for installing Drupal. 

Note: When it asks about the database, that is where you will input the information you got from `lando info`.

#

## Usage:
The usage of this web page is extremely simple and like every other webpage. If you would like to edit the page you can visit the developmental tools in the Drupal GUI.

#### Module / Theme Editing 
In drupal there are some default themes that you can install for the website but you can also download external ones. Using `lando composer require drupal/a_theme:(version)`. This also applies to modules that you would like to install.

To export your modules and themes to your remote Repo so that others can work on it type `lando drush cex module_name*` after you enabled a module. To enable a module you can use `lando drush en module_name`.

## Troubleshooting
Some issues may occur while using/editing this site.  Somethings to try:

`lando drush cr all` clears the cache of current site and you can use `lando restart` to restart the wbesite. You can also use `lando rebuild -y` to rebuild the website in your Docker.

Finally if the above don't work you can destroy the site as a last measure. `lando destroy` to destroy the site for a rebuild.
#
Credits:
Hooman Keshmiri
Farnoosh Johnson