.. _bat_drupal_requirements:

Requirements
************

Introduction
============
BAT for Drupal uses four components that are all required to get the full range of funcitonality.

#.  The `BAT PHP Library <https://github.com/roomify/bat>`_  - this provides the core booking functionality and the best way to manage it on your Drupal site is through `Composer and Composer Manager for Drupal <https://www.drupal.org/project/composer_manager>`_
#.  The `BAT <https://drupal.org/project/bat>`_ module is a wrapper around the library providing Entity, Views, Rules and Event Management via calendars.
#.  The `BAT API 2.x <https://drupal.org/project/bat_api>`_ provides REST access to event data and event manipulation. It powers things such as the dragging and dropiing of events on the calendar UI.
#.  The `FullCalendar jQuery library <http://fullcalendar.io>`_ as a UI to events.


Dependencies
=============

Drupal Modules
---------------

* `BAT API <http://drupal.org/project/bat_api>`_ > version 2.x
* `X Autoload <https://drupal.org/project/xautoload>`_ - provides support for PSR-4 style name spaces
* `Composer Manager <https://www.drupal.org/project/composer_manager>`_ - to get the BAT PHP library
* `Date <http://drupal.org/project/date>`_
* `Entity <http://drupal.org/project/entity>`_
* `Entity Reference <http://drupal.org/project/entityreference>`_
* `Ctools <http://drupal.org/project/ctools>`_
* `JQuery Update <http://drupal.org/project/jquery_update>`_
* `Libraries <http://drupal.org/project/libraries>`_
* `Views <http://drupal.org/project/views>`_
* `Views Megarow <https://www.drupal.org/project/views_megarow>`_
* `Views Bulk Operations <https://www.drupal.org/project/views_bulk_operations>`_
* `Search API <https://www.drupal.org/project/search_api>`_
* `Facet API <https://www.drupal.org/project/facetapi>`_
* `Services <http://drupal.org/project/services>`_ (a dependency of BAT API)

jQuery Libraries
----------------
#. `FullCalendar library <https://github.com/arshaw/fullcalendar/releases/download/v2.6.0/fullcalendar-2.6.0.zip>`_ 
#. `FullCalendar Scheduler extension <https://github.com/fullcalendar/fullcalendar-scheduler/releases/download/v1.2.0/fullcalendar-scheduler-1.2.0.zip>`_.
#. `Timepicker <https://fgelinas.com/code/timepicker/releases/jquery-ui-timepicker-0.3.3.zip>`_ - This not a strict requirements - simply makes the creation of hour-based events easier. 


Drush-based Setup
------------------
If you are familiar with Drush and Drush make then you can use the bat.make file in the BAT module repository to get all the modules requireed (in versions we have tested BAT with) and the FullCalendar Library. From your Drupal root run

``drush make --no-core sites/all/modules/bat/bat.make``


Composer
---------
You will need to install Composer if you don't have that already (a great idea since it will be needed for Drupal 8).

Follow the instructions from the `Composer Manager module <https://www.drupal.org/project/composer_manager>`_ to get setup. 