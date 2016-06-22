.. _roomify_accommodations_payment_methods:

Payment Methods
***************

Working on the Quickstart?  Get back to Step 4 here: :ref:`roomify_accommodations_setup_commerce`.

Roomify for Accommodations currently supports three payment gateways and offline payments. To configure your payment method, click on 'Payment Methods' in the 'Manage Configuration' tab of your dashboard.

.. image:: images/payment_methods.png
   :width: 700 px
   :align: center

There are four options:
#. `Stripe`_
#. `Paypal`_
#. `Authorize`_
#. `Offline Payments`_

Stripe
======

To enable Stripe as your payment processor, first you will need a Stripe account.  If you do not already have one, you can sign up here:  https://dashboard.stripe.com/register.  Go through the registration process and then come back to your site, we will point you to everything you need to see in Stripe.
	Step 1. Check 'Enabled' in the Stripe tab.
	Step 2. Select your currency - Current options are CAD - EUR - GBP - USD - AUD - CHF
	Step 3. In Stripe, ensure that your account switch is set to 'Live' (See screenshot below)
	Step 4. Enter your Secret Key from Stripe: https://support.stripe.com/questions/where-do-i-find-my-api-keys
	Step 5. Enter your Publishable Key from Stripe: Ensure that both the Secret Key and the publishable key have no spaces before or after.
	Step 6. Click 'Save configuration'


.. image:: images/stripe_live.png
   :width: 700 px
   :align: center

Done!

Stripe also offers the ability to test payments on your site.  To set up your site to test payments, follow these steps:

	Step 1. Check 'Enabled' in the Stripe tab.
	Step 2. Select your currency - Current options are CAD - EUR - GBP - USD - AUD - CHF
	Step 3. In Stripe, ensure that your account switch is set to 'Test'
	Step 4. Enter your TEST Secret Key from Stripe: https://support.stripe.com/questions/where-do-i-find-my-api-keys
	Step 5. Enter your TEST Publishable Key from Stripe: Ensure that both the Secret Key and the publishable key have no spaces before or after.
	Step 6. Click 'Save configuration'

You can now make test bookings on your site without having to use a real card, or refund payments.  When Stripe is in test mode, any billing address and expiration date will work with this number: 4111 1111 1111 1111

IMPORTANT: If you use stripe in test mode, ensure that you switch it to LIVE before you start taking bookings!

Paypal
======

Docs coming soon!

Authorize
=========

Docs coming soon!

Offline Payments
================

Docs coming soon!
