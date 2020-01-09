.. _roomify_accommodations_global_booking:

Global Booking Settings
***********************

Working on the Quickstart?  Get back to Step 3 here: :ref:`roomify_accommodations_setup_bookings`.

Your Roomify for Accommodations site offers several ways to customize how you take bookings.  The Global Booking Settings, accessed via the Manage Configuration tab of your dashboard, will apply to all properties, site-wide.

#. `Booking Settings`_
#. `Booking Page settings`_

Booking Settings
================

These settings control how a booking can be made on the site, as well as some configuration around how taxes are calculated, and whether or not a deposit is taken as payment for the booking.

	How soon a booking may start - This will determine how close to the start date a booking can be made.  The options are **Same day** up through **7 days** in advance.  This means that if the site is configured to allow bookings starting 2 days in advance, a user will only see availability that is 2+ days from the current date.

	Advance Bookings - This will limit how far in the future bookings can be made.  The options for this are not limited, you can allow bookings 50 years from now, if you like (although we don't recommend it!).  The default setting is one year.

	Allow instant bookings - Enabling instant bookings means that users will be able to book and pay immediately. Make sure to setup a suitable payment method!  If this is disabled, users will only be able to book via a conversation. (For more information, see - :ref:`roomify_accommodations_properties_enquiries`) Instant bookings can still be turned off for individual room types/houses of a property, but an owner cannot make a property available for instant bookings if the site manager has turned them off Globally.

	Apply property taxes to property add-ons - This option will apply any taxes that are configured for a property to any add-ons that are configured for the House or Rooms of that property. (See the Manage Rooms - Add-Ons section for more information - :ref:`roomify_accommodation_properties_properties`)

	Allow bookings based on a deposit - Allow guests to make bookings by paying a deposit (percentage or fixed amount) instead of the full booking price of their stay. 

.. note:: If deposit is used, the remaining balance will be captured in person, and cannot be charged via the website.


Booking Page Settings
=====================

.. note:: These settings only apply to sites that have **deposit based** payments enabled. You can use them to choose what labels you show to your guests during checkout.

+ Deposit label - If you use %deposit% in this label, it will be replaced with the value set in the **Payment deposit Settings**.  This labels the percentage of the booking that will be charged to the guest on checkout.

+ Payable now label - This labels the amount that is due on checkout.

+ Remainder label - This labels the amount that will be due when the guest checks in at their destination.

+ Total cost label - This labels the full amount a guest will pay for the stay.
