.. _installation:

Installation
************

Install Drupal
===============

Follow the `instructions <http://drupal.org/documentation/install>`_ to install Drupal.

Download Modules
================

Then download Rooms and all its dependencies as described in :ref:`rooms_requirements` and place them in the sites/all/modules directory of Drupal.

*Ensure that you are using BAT API 1.0 - Rooms will not work with BAT API 2.x*

Download necessary JS libraries
===============================
To display administrative calendars, Rooms depends on the FullCalendar (http://fullcalendar.io) library. Within the Rooms module there is a rooms.make file which will download the library if using Drush or you can visit `here <https://github.com/arshaw/fullcalendar/releases/download/v2.6.1/fullcalendar-2.6.1.zip>`_ to download it.

The FullCalendar library should be placed in sites/all/libraries so that you end up with the file located here: sites/all/libraries/fullcalendar/fullcalendar.js

*You do not need the Drupal FullCalendar Module - just the library mentioned above.* 

Enable Rooms modules
====================
Visit the /admin/modules page of your Drupal installation and activate all the Rooms modules. Drupal will pickup all the dependencies and activate a number of other modules as well and inform you if something is missing.

Check if everything went well
==============================
Visit the /admin/reports/status page of your Drupal Installation and check that there are no errors related to Rooms. You should see the message "The FullCalendar Library is installed" if everything went well.

Start your Roomified site!
===========================
At the end of the activation process you should see a new tab across the black bar at the top of Drupal called Rooms or you should be able to navigate to admin/rooms with three options available Bookable Units, Bookings and Configuration.
