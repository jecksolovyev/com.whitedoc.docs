===========
Callbacks
===========

Envelope callback is functionality which allows to receive notification to respective URL in case of envelope appearance in mailbox and according to configured filters. You can set up callbacks for mailbox in order to receive envelope notifications outside of our platform. This is done via API. 
How to configure callbacks you can see here - :ref:`Envelope callbacks <envelopeCallback>`
The administrative panel allows you to view and partially manage callbacks.

Manage callbacks
========================================

1. Navigate to https://platform_address_here/admin/callbacks

.. image:: pic_users/callbacks.png
   :width: 600
   :align: center

2. In the drop-down list, select the mailbox whose callbacks you want to display.

.. image:: pic_users/callbacksChooseMailbox.png
   :width: 600
   :align: center

.. note:: a list of callbacks will be displayed for the selected mailbox if callbacks have been configured via the API. Otherwise the page will be displayed as an empty folder.

3. The list of callbacks contains the following information:
- callback URL (1)
- authentication type (2) - Basic, None
- success code (3)
- filter (4) - list of specified filters for a specific callback
- actions buttons (5) - settings and delete

.. image:: pic_users/callbacksColumns.png
   :width: 600
   :align: center

Check callbacks
========================================

1. Open the Settings button for the selected callback

.. image:: pic_users/callbacksSettings.png
   :width: 600
   :align: center

2. Check callback modal window will be open. Here you can add valid envelope UUID and check callback using the button of the same name.

.. image:: pic_users/callbacksCheck.png
   :width: 600
   :align: center

3. In case if the specified envelope UUID matches the configured filters a corresponding message and an active button "Send a callback" will appear

.. image:: pic_users/callbacksFilterMatch.png
   :width: 600
   :align: center   

4. Click Send callback button and the following information will be displayed in the modal window:
- envelope UUID
- responce code
- responce body

.. image:: pic_users/callbacksSend.png
   :width: 600
   :align: center 

.. note:: you can send callback again, follow back to previous step (enter envelope UUID) or cancel action.

5. In case if the specified envelope UUID doesn't match the configured filters a message listing mismatches will be displayed. After that you can just follow back to previous step and enter another envelope UUID or cancel action.

.. image:: pic_users/callbacksFilterNotMatch.png
   :width: 600
   :align: center  

Delete callbacks
========================================

1. Open the Delete button for the selected callback

.. image:: pic_users/callbacksDelete.png
   :width: 600
   :align: center

2. Delete callback modal window will be opened where you can choose Delete or Cancel action

.. image:: pic_users/callbacksDeleteOrCancel.png
   :width: 600
   :align: center

3. In case you want to delete callback click Delete button and succesful message will be displayed

.. image:: pic_users/callbacksDeleted.png
   :width: 600
   :align: center 