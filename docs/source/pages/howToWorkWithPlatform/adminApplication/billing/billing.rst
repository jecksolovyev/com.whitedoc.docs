=======
Billing
=======

.. note:: Billing page will not appear in the admin panel if it is not enabled in the instance settings.

Billing functionality allows you to manage :ref:`tariffs <tariffs>`, :ref:`invoices <invoices>`, :ref:`payment methods <paymentDetails>` and see the account balance details.

.. image:: pic_billing/billing.png
   :width: 600
   :align: center

.. _tariffs:

Tariffs tab
===========

This page lists available instance tariffs and which tariff is currently applied to the account.

.. image:: pic_billing/tariffsPage.png
   :width: 400
   :align: center

Tariff may be applied by clicking the respective button "Select tariff". After clicking the "Select tariff" button modal window with confirmation will be displayed. By confirming, the applicable tariff will be assigned to the account.

.. note:: If instance contains payment provider "Stripe" the following verifications and actions will be performed

**Account doesn't have billing address or payment details or both**

1. By confirming, the applicable tariff the system will verify if account has billing address and :ref:`payment method <paymentDetails>`
2. If one of the billing address and :ref:`payment method <paymentDetails>` is not added to the account, modal window with respective configuration will be displayed
3. As soon as user enters payment and billing details it will be added to the account as :ref:`payment method <paymentDetails>`
4. On this step, if tariff has prepay configuration (most tariffs has), tariff will be assigned to the account, :ref:`invoice <invoices>` will be generated and paid (if the added payment method has sufficient funds)

**Account has payment details and billing address**

1. By confirming, the applicable tariff the system will verify if account has billing address and :ref:`payment method <paymentDetails>`
2. If tariff has prepay configuration (most tariffs has), tariff will be assigned to the account, :ref:`invoice <invoices>` will be generated and paid (if the added payment method has sufficient funds)

.. note:: You can choose only one tariff at the moment. You can change tariff not more that 1 time per hour.

.. _invoices:

Invoices tab
============

This page contains account invoices. Here you can see paid, unpaid and cancelled invoices, download and pay them. Invoice can be issued manually or, more often, automatically. Automatic invoice issuing works according to the tariff configuration.

**Invoice download options**

You can download invoices by clicking the respective button in the specific invoice and choosing one of the invoice options.

.. image:: pic_billing/invoicesPageDownloadInvoice.png
   :width: 400
   :align: center

1. Without details - will be downloaded basic invoice without any details about the account events
2. With details - will be downloaded basic invoice with positive and negative details about the account events (positive and negative events are events that made positive or negative impact for account balance)
3. With zero details - will be downloaded basic invoice with positive, negative and zero details about the account events (zero events the events that did zero impact for account balance)

**Invoice payment options**

If you have unpaid invoices, you are able to pay the invoices manually by clicking the respective button in the specific invoice and choose the one of the available payment provider

.. image:: pic_billing/invoicesPageUnpaid.png
   :width: 400
   :align: center

As soon as you click the "Pay invoice" button, a modal window will appear

.. image:: pic_billing/invoicesPagePayInvoiceModal.png
   :width: 400
   :align: center

You can choose one of the appropriate payment provider to pay the invoice and proceed with payment provider, as soon as invoice paid you will observe paid invoice

.. image:: pic_billing/invoicesPagePaid.png
   :width: 400
   :align: center

.. _balanceDetails:

Balance details
===============

Balance details page represents details related to account events activities that impact the account balance and the account counters (f.e.: envelopes quantity left, mailboxes quantity can be created and etc.(each counter depends on tariff configuration))

.. image:: pic_billing/balanceDetailsPage.png
   :width: 400
   :align: center

.. _paymentDetails:

Payment details
===============

.. warning:: We are not storing your payment details. The payment details are stored by "Stripe" payment provider

Payment details page represents payment details of the "Stripe" payment provider assigned to the account.

.. note:: If payment provider "Stripe" is presented on the instance the page will be available otherwise page will not be accessible

By default page doesn't contain payment details

.. image:: pic_billing/paymentMethodsPageWithoutPayment.png
   :width: 400
   :align: center

You can add them by clicking the "Add payment details" button

.. image:: pic_billing/paymentMethodsPageAddPayment.png
   :width: 400
   :align: center

By default you are able to add payment method only, but if you need to add/update the billing address withing the payment details you will set checkbox on "Change billing address"

.. image:: pic_billing/paymentMethodsPageAddPaymentWithAddress.png
   :width: 400
   :align: center

As soon as you added payment details and/or billing address you will observe payment details with possibility to update them

.. image:: pic_billing/paymentMethodsPageWithPayment.png
   :width: 400
   :align: center

.. note:: Only one payment method can be active at the moment for one account. If you update payment method the updated one will be active and previous payment method will no longer be available.