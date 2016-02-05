.. _booking_settings:

Booking Settings
****************

Rooms has a rich set of configuration options under admin/rooms/config/bookings

Rooms Booking Settings
=======================
**How soon can a booking start:** You can define whether users can book a booking on the same time they visit your site or whether there should be some lag time (e.g. bookings can only be done for two days from today).

**Active Booking Type:** Most people will not need to change this but this option allows you to define what type of Booking entity should be created. By default there is only the standard booking entity, but using Drupal's Entity functionality you can also create you own booking types that carry richer information through fields that extend it.

**Valid availability states:** What states should be available for immediate booking.

Calendar Codes and Labels
==========================
This section allows you to customize the colours used in calendars.

Administrative settings
========================

**Cart Expiration Time:** When a booking is placed in the cart that room is made unavailable to anyone else searching at the same time. This allows you to define how long should the room be unavailable before it is removed from the cart and its availability released.

Rooms Checkout Settings
========================
**Checkout Presentation Style:** Here you can choose whether after a user views the results of an availability search and choose a unit to book they are taken to an enquiry form or they use the Commerce cart to checkout. An enquiry form means that the booking will not have actual effect on the availability while a Commerce cart checkout will update the availability state of units.

**Price Calculation:** You can choose whether cost of a room is calculated based on the number of people per night or simple per unit per night.

**Create orders for manually generated bookings:** If you do not want to create orders for manually generated bookings you can uncheck this option.

Rooms availability search settings
===================================
**Results Presentation Mode:** By default results are shown per-type, i.e. we will list that there are 'Standard' or 'Deluxe' units available. For certain use cases though it may make sense to least the individual units available (e.g. if you are renting our individual apartments or villas).

**Number of units to display:** When showing results per-type we can decide how many units we should show as available.

**Display children choice in availability search:** This will allow users to define how many children will make up the group. As a result the availability search will look for rooms that can accommodate the number of children defined.

Display unit type selector in availability search: The unit type selector allows users to choose what types of Units they are interested in (e.g. only Standard Rooms or only Deluxe Rooms).