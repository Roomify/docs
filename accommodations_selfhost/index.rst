.. _accommodations_selfhost: Selfhosted installation instructions,

Installation instructions for Roomify for Accommodations - Self-Hosted
======================================================================

Installing a self-hosted Roomify for Accommodations site is very simple.

Keep in mind that Roomify for Accommodations is a pre-configured Drupal site. Once you `purchase the solution <https://store.roomify.us/roomify-accommodations-self-hosted>`_ you will receive a ZIP file.

Within that file you will find a MySQL database dump and the *entire* Drupal site including all source code, Javascript libraries and PHP libraries that are used.

Here is what you need to do.

1. Unzip the file provided.

2. Place that file in the appropriate location in either your local development environemnt or your webserver.

3. Configure your web server to point to that location. 

4. Import the included .sql file to your MySQL or MariaDB installation.

5. Edit the *existing* sites/default/settings.php file and adjust database settings to point to the database you imported in Step 4. 

6. Set appropriate permissions for the files directory (`Here <https://www.drupal.org/node/244924/>`_ is an excellent guide.)

7. Ensure PHP memory limit (memory_limit) is at least 160M.

8. Esnure you are using at least PHP5.4 although PHP5.6 is preferred.

In order to loging to the Drupal site you can reset the password using Drush or login with:
user: admin
pass: admin

*Please change your password immediately!*

Keep in mind this is just like setting up any Drupal site with the only difference that you don't need to go through the installation process of Drupal itself. The database we provide is preconfigured. Our packaging tool does a clean installation of Roomify for Accommodations and adds the exported database to the package.


.. toctree::
   :maxdepth: 3