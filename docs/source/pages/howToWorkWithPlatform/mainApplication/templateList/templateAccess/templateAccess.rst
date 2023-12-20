.. _templateAccessLevel:

===============
Template access
===============

User can specify access level of the template when creating or editing it. There are four types of access on the platform:

- access for your mailbox only
- access for selected mailboxes (Selected mailboxes)
- access for all mailboxes in your account (My account)
- access for everyone on the platform (Everyone)

.. note:: Public templates can be made accessible to users not registered on the platform via direct link. To generate this link first you need to make sure that such template includes only public dictionaries (or no dictionaries at all). Also such templates should have subject field filled and all participants of the flow should have specified mailbox adresses in the flow configuration tab. When this is done, click on the template menu button in upper right corner of template on template list and click "Get link". Menu with sharing link will open where you can copy this link, generate new one to revoke access by previous link or remove access by link completely. Account on the platform will be created automatically for anyone who will create an envelope using such link.

How to edit a template access level
===================================

1. In order to set access level of template you need to go to "Template" tab and click on "Template access"

.. image:: picTemplateAccess/templateAccess1.png
   :width: 400
   :align: center

2. You can grant access to specific mailboxes. After selecting this option you will need to click on edit button

.. image:: picTemplateAccess/templateAccess2.png
   :width: 400
   :align: center

3. In the modal window you can enter mailbox name, mailbox UUID, alias, or contact name

.. image:: picTemplateAccess/templateAccess3.png
   :width: 400
   :align: center

4. When mailbox is added click "Save"

.. image:: picTemplateAccess/templateAccess4.png
   :width: 400
   :align: center

5. Save сhanges

.. image:: picTemplateAccess/templateAccess5.png
   :width: 400
   :align: center

6. After saving the template it will be available for mailboxes specified by you in the folder "Shared with me"

.. image:: picTemplateAccess/templateAccess6.png
   :width: 400
   :align: center
   
Additional sharing access configurations
========================================

At the bottom of the template tab of envelope menu you can find "Do not send files by email" attribute

.. image:: picTemplateAccess/templateAccess7.png
   :width: 400
   :align: center
   
If you will enable it and save the template, all envelopes created from it will not contain any files from the envelope in notification emails. Also such envelopes can not be shared with other mailboxes. If set on template level, it's impossible to change it on envelope level later.