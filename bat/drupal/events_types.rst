.. _bat_drupal_event_types:


Connect Types to Events
************************

In BAT we try to have the least amount of things hard-coded. This allows us to create truly flexible booking systems. However, it also means that we need to *explain* to the framework all connections.

In :doc:`type_bundles` we created a Meeting Room Type and in :doc:`events` we created two types of events for availability and pricing. We now have to connected the two. In other words, we need to let BAT know that our meeting rooms will have events of the type Meeting Room Available and Pricing *happen* to them.

Default event value fields
===========================
To connect a Type Bundle to an Event you first have to add a default event value field. 

In ``bat/config/type-bundles`` click on the manage fields tab of the event type you are interested in and add fields to hold default event values.

Fixed State Events
-------------------
For fixed state events the type of field is always going to be BAT Event State Reference field. 

.. image:: images/add_default_event_value_field.png

In the field settings you need to select the Event Type that this field will point to (it will only show event types that have fixed states).

.. image:: images/select_event_type.png

Now, with the field in place you can visit ``bat/config/type-bundles`` and click on the "edit" operation of the type bundle you are interested in. For every type of Event you will see a drop-down that allows you to connect a field of this Type Budle to an Event Type.

.. image:: images/connect.png

This may seem like an extra step but you should keep in mind that BAT makes no assumptions. You may have multiple fixed state event fields pointing to multiple event types. As a result, there is a bit of extra setup to define everything.

Arbitrary state events
-----------------------
For arbitrary state events you can create a field out of the set of fields that BAT supports. Currently those are:

* Integer
* Commerce Price
* Text