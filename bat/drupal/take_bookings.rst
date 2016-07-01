.. _bat_drupal_bookings:

Taking Bookings
****************

Now that we can search for availability (:doc:`search_availability`) the next logical step is to provide support for taking bookings.

The simplest way to create a booking is to change the state of an event to the appropriate state as described in :doc:`manage_units`. This can either be achieved through the Event Management interface or programmatically. 

However, more sophisticated applications may require different interaction modes. For example we may need to connect a Booking to an order / payment, collect additional user information and place it in the context of a checkout flow. While we could collect all that information within an Event we would be overcomplicating the Event entity and not separating concerns appropriately. Instead, we can opt to create a Booking entity that connects an Event to, for example, an Order or Customer Data.

This is the method we are using for our own BAT-based products and it is described here to help others consider the possibilities when using BAT Drupal. 

The code for this is specific to an application (it depends on your Event Types, Event States and general application logic) so it is not included in the BAT Drupal module. Please `get in touch <https://roomify.us/get-started>`_ if you are interested in commercial services in this direction. 

Booking Entity
---------------
The first step is to create a Booking Entity. The purpose of this entity is to connect an Event to a Booking and any information that may be associated with that Booking (customer profile, order, etc).

As with everything else in BAT we can have different booking types for different scenarios, etc.

.. image:: images/bat-booking.png

The Booking Entity has an entity reference field to an Event. It is the state change at the Event that will actually modify the availability of a Unit. The Booking simply joins an Event to other information our application needs.

Add Booking Link
----------------
On our Meeting Room View we will add a Book Now link. The Book Now link will only appear following a search and takes into account the values entered in the facet filter. The link passes those on to a basic booking form.

.. image:: images/book-now.png

Booking Form
-------------
The booking form can have any fields our use case requires - in this case we just add a "Confirm Booking" button that will:

#. Re-check availability 

#. Create an event that sets the availability of a meeting room to booking

#. Create a booking entity

.. image:: images/booking-form.png

Depending on the use case one could delay the creation of the Event to after a checkout process.

Bookings
---------
We now have a Booking that is connected with the relevant event. We can use this entity to add any other type of information that is required with the booking and we need to take care to update the relevant event when the booking is changed.

.. image:: images/example-booking.png

NB: We have not as yet dealt with calculating the price of the booking. Costs would be determined by referring to pricing events for the period of the Booking and using the Valuator class of the BAT PHP library to determine the cost over that period.







