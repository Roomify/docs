.. _units_types:

Bookable Units and Unit Types
*****************************

Introduction
===============
Bookable Units are the main elements behind Rooms. They represent the things that your guests can book, whether those are rooms in a hotel, apartments in an apartment group, a single holiday home, etc. 

Bookable Units can be grouped in types and we can choose via admin/rooms/config/bookings whether to present guests search results per type or per single unit. Typically if you are a small B&B with just 3-4 rooms you might want to present individual units that your guests can book into while a larger hotel would like to present availability along the lines of room types.

Bookable Unit Types
====================
Your first task is to define what types of Bookable Units you have and then create Bookable Units of that type. There are a variety of possibilities here based on what type of accommodation we are dealing with. To manage Bookable Unit Types click on Bookable Units under admin/rooms and then click on the tab Bookable Unit Types - you should end up at admin/rooms/units/unit-types. Here you can add a Bookable Unit Type. You can think of a type as both a way to group similar bookable units and as a template for the bookable units of that type. Keep in mind that each bookable unit's values can then be customized further.

Settings for Bookable Unit Types
================================

* **Unit Type Name:** Bookable unit types have a name (e.g. Standard, Deluxe, etc). This is how they will be referred to and what guests looking to book them will see. 
* **Unit Base Price:** This is the default price per night (or per person per night) for units of this type. If nothing else is defined via the Pricing calendar this option will be used. 
* **Person sleeps:** The minimum and maximum number of people that can go in a unit of this type. 
* **Children sleeps:**The minimum and maximum number of children that can go in a unit of this type. This is not in addition to the number above. The aim is to possibly limit children in a room if children are discounted
* **Options:** Options allow you to define add-ons to all units of this type: whether that is surcharge for a cot, di;count for a double room used as a single, special offers, etc. Options have a label that the guest will see, possible quantity, an operation (i.e. how should they modify the rooms cost) and the value by which they should modify it. 
* **Select Unit Description Source:** This is relevant if you are showing group availability search results (i.e. users search for types of units and you want to have a single description for all standard rooms, all deluxe rooms, etc). The source is a node of type Unit Description which Rooms create. In the search results of rooms the Rooms Results Display view will be rendered. The idea here is to enable you to use the same description for say all Standard Rooms both on a standard node page that users visit as well as on availability search results simply by rendering a different view mode. Let us look at a couple of examples of how you could organize your Bookable Unit Types.

Configuring Bookable Units for a Hotel
=======================================

If we are dealing with a hotel we want to configure our bookable unit types as follows: Standard Single, Standard Double, Deluxe Double Ocean View, Quadruple Family Room. We would then create individual Bookable Units based on how many Standard Singles, Standard Double, etc we have. The search results should then be configured to present to the user results based on type and not based on individual units. If you want to be able to handle overbooking you can simply create more Units than what you have available, you will however need to reconcile guests eventually in the actually available Rooms!

Configuring Bookable Units for a B&B
=====================================

If we are dealing with a small B&B with just 3 rooms we might just have a single type called Standard and then create three Bookable Units to represent the different rooms. We would then present results of individual units rather than unit types.

Configuring Bookable Units for a holiday home
==============================================

A holiday home needs just one type and one unit of that type as we are renting the entire holiday home.

Bookable Units
===============

With our types defined we can now define the actual bookable units. Visit admin/rooms/units to add Bookable Units. There are three components to a bookable unit:

 
**Configuration Options:** This include the min/max people, base price, default availability state and also any options that can be associated with the unit.

**Availability Calendar:** This is where availability for the unit is managed.

**Pricing Calendar:** This is where pricing for the unit is managed. 
