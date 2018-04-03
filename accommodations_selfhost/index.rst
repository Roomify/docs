.. _accommodations_selfhost: Selfhosted installation instructions,

Roomify for Accommodations - Self-Hosted
======================================================================

Installation
-----------------

Installing a self-hosted Roomify for Accommodations site is very simple.

Keep in mind that Roomify for Accommodations is a pre-configured Drupal site. You may download a packaged zip file from `the releases page <https://github.com/Roomify/RfA/releases>`__.

Within that file you will find a MySQL database dump and the *entire* Drupal site including all source code, Javascript libraries and PHP libraries that are used.

Here is what you need to do.

1. Unzip the file provided.

2. Place that file in the appropriate location in either your local development environment or your webserver.

3. Configure your web server to point to that location.

4. Import the included .sql file to your MySQL or MariaDB installation.

5. Edit the *existing* sites/default/settings.php file and adjust database settings to point to the database you imported in Step 4.

.. tip:: Subdirectory Installations
   If your RfA installation will be placed in a subfolder of your server, (i.e. http://your.server/folder/RfA/) you must set the `$base_url <https://api.drupal.org/api/drupal/developer!globals.php/global/base_url/7.x>`__ variable to your site's URL (without a trailing "/") in settings.php.

6. Set the appropriate permissions for the files directory (`Here <https://www.drupal.org/node/244924/>`__ is an excellent guide.)

7. Ensure that the PHP memory limit (the memory_limit setting in your web server's php.ini file) is at least 160M.

8. Ensure you are using at least PHP5.4 although PHP7.0 is preferred.

In order to login to the Drupal site you can reset the password using Drush or login with:

user: admin
pass: admin

*Please change your password immediately!*

Keep in mind this is just like setting up any Drupal site. The only difference that you don't need to go through the installation process of Drupal itself. The database we provide is preconfigured. Our packaging tool makes a clean installation of Roomify for Accommodations and adds the exported database to the package.

Updating
----------

We provide updates to Roomify for Accommodations on a regular basis - just go to `the releases page <https://github.com/Roomify/RfA/releases>`__ to download the latest release.

Instructions given here are generalized, and *must* be adapted to your particular situation and deployment process.

*Always make a full backup of your entire codebase, files and database before installing updated code!!!*

If you have not customized any code or functionality (e.g. modifying views or other functionality exported to the roomify features) and your files directory and settings.php file are in the default location (sites/default), the process is simple:

1. Move your entire codebase to a backup location outside the web server's document root.

2. Do *not* import the included .sql file.

3. Unzip the new file you have updated into your web server's document root.

4. Remove the new sites/default directory and copy the sites/default directory from the older installation.

5. Run `database updates <https://www.drupal.org/upgrade/running-update-php>`__.

6. Revert all features - the quickest way to do this is to use `drush <http://drush.ws>`__ and use the command features-revert-all. You may find more information on reverting features `here <https://www.drupal.org/node/582680>`_.

7. `Clear all caches <https://www.drupal.org/documentation/clearing-rebuilding-cache>`__ - it's possible that all features may not fully revert until you have cleared caches and reverted features twice or three times. This is known behavior with Drupal and not particular to Roomify for Accommodations.

8. If any settings that you have modified are reverted by following this process, you should restore your database backup and manually revert features, only reverting functionality that you have not modified. Please see the section on customization for more information.

NB: It is best not to skip versions of Roomify for Accommodations; for example, by updating directly from version 1.0.6 to 1.0.9. It may work, but we only test updating one version at a time and therefore recommend that you follow this practice.

Customizing Roomify for Accommodations
----------------------------------------------

When making customizations, your goal should be to avoid directly modifying source code and settings/configurations provided by Roomify for Accommodations. This will make the process of installing updates far easier and avoid having to manually re-integrate any changes you make. Here are a few specific recommendations:

1. Place any custom modules you create or download under sites/default/modules - This will allow you to follow the update process provided above without any additions or modifications.

2. Use `hooks <https://www.drupal.org/node/292>`__ in a custom module wherever possible to modify functionality.

3. The `Features Override <https://www.drupal.org/project/features_override>`__ module may be useful to customize functionality provided by Roomify features.

4. If you wish to customize the Roomify-provided permissions for roles on the site, you will need to disable the Roomify Rights module. This module enforces correct permissions for Roomify functionality, so as a result, you will need to track permission changes manually. The simplest way to do this is to keep your site in version control and look for changes to invocations of hook_roomify_rights after installing an update.

.. toctree::
   :maxdepth: 3

