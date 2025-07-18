=========
Mailboxes
=========

Mailboxes page is a part of admin panel interface. This page allows to:

1. Create, manage and delete mailboxes
2. Create, manage and delete mailbox groups

.. image:: pic_mailboxes/mailboxesTab.png
   :width: 600
   :align: center

=============
Mailboxes tab
=============

**How to create a mailbox**

1. Click the "Create mailbox" button
2. Enter new mailbox name in the opened window

.. image:: pic_mailboxes/mailboxesTabCreateModal.png
   :width: 600
   :align: center

3. Click the "Create" button (it will become enabled after name is entered)

**How to generate a report by mailbox**

1. Select all necessary records
2. Click the "Generate report" button in table header
3. After click you will see the message that report will be send to you email after generation
4. Open email you got
5. Click the "Download" button

.. note:: You also can edit groups assigned to mailboxes in bulk. To do so click the "Add mailboxes to group" button in table header.

**How to check users assigned to mailbox**

To see the list of users which have access to the mailbox click the link with number in the "Users" column. After this action you will be redirected to the Users page with filter predefined by mailbox.

**How to edit a mailbox**

Edition interface allows update name of the mailbox, add and remove aliases to the mailbox, copy the mailboxs UUID, unassign all users with access to the mailbox and delete mailbox. To open mailbox edit form click the settings icon.

.. image:: pic_mailboxes/mailboxesTabEditButton.png
   :width: 600
   :align: center

Mailbox settings section
========================

**How to copy mailbox UUID**

To copy the mailbox UUID click the copy icon. After successful copying the notification message will be shown at the right corener of the page.

.. image:: pic_mailboxes/mailboxesCopyingUuid.png
   :width: 600
   :align: center

**How to edit mailbox name**

1. Name field has length validation: 1 - 255 symbols
2. To edit name just focus the name change it and click the "Save changes" button

.. image:: pic_mailboxes/mailboxesNameUpdate.png
   :width: 600
   :align: center

3. After successful edition of the mailbox the notification message will show at the right corner of the page

.. image:: pic_mailboxes/mailboxesChangesSaved.png
   :width: 600
   :align: center

**How to edit mailbox name visibility**

You can enable the visibility of your mailbox for system members. To do so, activate the "Allow everyone to find my mailbox by searching for my name and/or aliases" toggle and then click the "Save changes" button. When the toggle is active, the mailbox can be found by all users on the platform by it`s name or aliases.

.. image:: pic_mailboxes/mailboxesHideAliases.png
   :width: 600
   :align: center

**How to manage mailbox aliases**

Two identical aliases can not be added to one mailbox.

.. note:: Two different mailboxes in the system can have same alias. If you need to ensure that you're alias is unique systewide, you can use qualified alias. Qualified aliases use a prefix with semicolon in the end e.g. TIN:youralias. If such prefix is used, same alias with same prefix can not be created in the system after initial one is created. For such aliases only letters, numbers and dash are allowed. Please note that not any prefix can be used - please contact your administrator for information on what unique prefix groups are used on your instance of application.

To add alias(es) to the mailbox:

1. Click the aliases area of the page 

.. image:: pic_mailboxes/mailboxesFocusOnAliasArea.png
   :width: 600
   :align: center

2. Enter the alias and press "Enter", "." or "," button on keyboard to add alias to the list, after that click the "Save changes" button

.. image:: pic_mailboxes/mailboxesTypingAliasName.png
   :width: 600
   :align: center

.. image:: pic_mailboxes/mailboxesFinishTypingOfTheAlias.png
   :width: 600
   :align: center

3. To remove alias from the mailbox, click the remove icon of the alias and click the "Save changes" button

.. image:: pic_mailboxes/mailboxesDeletionButton.png
   :width: 600
   :align: center

4. After successful edition of the mailbox the notification message will show at the right corner of the page

.. image:: pic_mailboxes/mailboxesChangesSaved.png
   :width: 600
   :align: center

**How to configure envelope forwarding**

In this section you can configure automatic forwarding of all incoming envelopes.

.. image:: pic_mailboxes/mailboxesForwarding.png
   :width: 600
   :align: center

1. Select a target mailbox which will be a delegate of yours
2. Select effective from date - it will specify a start date of the forwarding period (can be left empty to start period immediately)
3. Select effective until date - it will specify an end date of the forwarding period (can be left empty to make period indefinite)
4. Enable "Active forwarding" toggle
5. Click the "Save changes" button

Forwarding is configured now. If you wish to disable it at some point later, you can disable "Active forwarding" toggle and click the "Save changes" button.

.. _customDashboard:

Dashboard section
=================

To create custom dashboard instead of default one switch to tab "Dashboard" which contains:

1. Editor area where you able to enter your HTML code which will replace default dashboard
2. Checkbox to activate custom dashboard
3. Button "Save" changes

.. image:: pic_mailboxes/dashboard.png
   :width: 600
   :align: center

If you want to customize dashboard it's necessary to put content to html area, set checkbox in active state and save changes. Than dashboard will be changed to custom HTML for this specific mailbox and all users who has access to mailbox will see custom dashboard.

.. image:: pic_mailboxes/customDashboard.png
   :width: 600
   :align: center

.. note:: Custom HTML can not be more than 16 mb size.

Danger zone section
===================

To remove all users from mailbox or delete mailbox switch to "Danger zone" tab

.. image:: pic_mailboxes/mailboxesDangerZone.png
   :width: 600
   :align: center

.. image:: pic_mailboxes/mailboxesDangerZoneView.png
   :width: 600
   :align: center

**How to remove users from mailbox**

1. To remove all users from mailbox (remove all permissions to the particular mailbox from the all users who has it except the user who do the action) click the "Deactivate" button
2. Confirm the decision and users will be unassigned

**How to delete mailbox**

1. Click the "Delete" button to open the deletion modal window

.. image:: pic_mailboxes/deleteMailboxModal.png
   :width: 600
   :align: center

2. Enter the mailbox in upper case to the field in the modal window which opens after click the "Delete" button
3. If you wish to transfer the ownership of templates, scenarios and dictionaries of this mailbox to other mailbox from the account – check the according and select a mailbox to transfer ownership to (selector will appear after the checkbox is checked, the checkbox will be disabled if there are no other mailboxes in the account)
4. Confirm the decision and mailbox will be deleted

.. note:: `Behaviour of mailbox after deletion <delete_mailbox_behaviour.html>`_

.. _mailboxDelete:

**Delete mailbox behavior**

1. Deleted mailbox can not be restored
2. Mailbox will disappear from mailbox list at admin panel on mailbox page
3. If user tries to use deleted mailbox he will receive error 410 and will be redirected to first mailbox to which he has access. If user has no access to any of mailboxes he will be redirected to user profile page and all functionality will be blocked except profile and admin pages (if there is access to any account)

.. image:: pic_mailboxes/disabledProfileView.png
   :width: 600
   :align: center

.. _mailboxesGroup:

==========
Groups tab
==========

.. image:: pic_mailboxes/groupsTab.png
   :width: 600
   :align: center

**How to create a mailbox group**

1. Click the "Create group" button. Group creation form will appear

.. image:: pic_mailboxes/groupsTabCreate.png
   :width: 600
   :align: center

2. Fill group name (1 character min, 64 characters max)
3. Add mailboxes from Add mailbox search box
4. Added mailboxes can be searched and removed
5. Click the "Create" button when all details are filled

Group will be created and you will be returned to groups list.

**How to edit a mailbox group**

1. Click the "Settings" button (gear icon) in group row. Group properties form will appear

.. image:: pic_mailboxes/groupsTabEdit.png
   :width: 600
   :align: center

2. Update any group details which are needed to be updated
3. Click the "Save" button to save group details changes
4. Click the "Cancel" button to revert group details changes
5. Click the "Delete" button to delete group

.. note:: You can also delete a mailbox from groups list by "Delete" button (Trash bin icon) in group row.
   
6. You will be returned to groups list after taken action