============
User profile
============

This page allows you to edit various settings of your user profile. To open user profile page navigate to https://platform_address/profile

=============
Settings page
=============

.. image:: pic_userprofile/tabSettings.png
   :width: 900
   :align: center

1. First name
2. Last name
3. Language - this is language which will be used in user interface
4. Timezone - choose your time zone
5. Display exact date - specifies if absolute (01.01.2023 12:12) or relative (fiwe minutes ago) time is used
6. Region - specifies regional formats for dates and number, example is shown below the menu
7. User UUID (can not be changed, only copied)
8. Email (can not be changed, only copied)
9. Auto deposit mailbox - specifies which mailbox will be used for incoming envelopes. If disabled - you will have to manually specify mailbox for each incoming envelope
10. Signature settings - here you can create or update your e-ink signature
11. Initials settings - here you can create or update your initials
12. Register personal account
13. Register company account

Do not forget to click on Save changes button after editing anything on this page

How to creating an e-ink signature?
===================================

1. Go to user profile page
2. Click on Replace signature button

.. image:: pic_userprofile/signatureModal.png
   :width: 600
   :align: center

3. Draw your signature in opened window
4. Alternatively, text can be used as signature
5. Click on Save changes button on the account setting page

How to create a personal account?
=================================

1. To register new personal account click on Register personal account button
2. In opened window enter a name for the account
3. Select checkbox "I agree with Terms and conditions and Privacy policy"
4. Click on Create button (button will be enable when previous steps are done)

.. image:: pic_userprofile/createPersonalAccount.png
   :width: 600
   :align: center

How to create a company account?
================================

1. To register new personal account click on Register company account button
2. In opened window enter a name, ITN and mailbox name for the account
3. Select checkbox "I agree with Terms and conditions and Privacy policy"
4. Click on Create button (button will be enable when previous steps are done)

.. image:: pic_userprofile/createCompanyAccount.png
   :width: 600
   :align: center

How to update your password?
============================

.. image:: pic_userprofile/passwordSettings.png
   :width: 600
   :align: center

1. Check Change password checkbox
2. Enter current password
3. Enter new password
4. Confirm new password in second field
5. Click on Save changes button

How to uload user icon?
=======================

.. image:: pic_userprofile/userIconSettings.png
   :width: 600
   :align: center

1. Click Upload button and select an image
2. To see allowed image formats and sizes hover over info icon

.. image:: pic_userprofile/userIconValidation.png
   :width: 600
   :align: center

3. Click Save changes button to apply new icon
4. You can return default profile logo with Set default link

===============
Forwarding page
===============

.. note:: This functionality will be disabled if you do not have 2012 mailbox level permission (Delegate envelopes).

.. image:: pic_userprofile/tabForwarding.png
   :width: 900
   :align: center

In this section you can configure automatic forwarding of all incoming envelopes. To do so:

1. Select a target mailbox which will be a delegate of yours
2. Select effective from date - it will specify a start date of the forwarding period (can be left empty to start period immediately)
3. Select effective until date - it will specify an end date of the forwarding period (can be left empty to make period indefinite)
4. Enable "Active forwarding" toggle
5. Click on "Save changes" button

Forwarding is configured now. If you wish to disable it at some point later, you can disable "Active forwarding" toggle and click on "Save changes" button.

================
Danger zone page
================

This page allows you to delete your user account. To open user profile page navigate to https://platform_address/profile?activeTab=dangerzone

.. image:: pic_userprofile/tabDangerZone.png
   :width: 900
   :align: center
	
.. note:: Ability to remove own user profile can be restricted in instance settings. In such case there will be no Danger zone tab on Profile information page.

After User profile deletion all Accounts with role "Account owner" will be deleted with all related data. User can keep all Accounts and all related data after User profile deletion.

.. image:: pic_userprofile/deleteUserProfile.png
   :width: 600
   :align: center

**Delete User profile with Accounts and all related data**

1. Click on Delete (1) button
2. Enter your e-Mail in upper case in the field (2) in the modal window which opens after click on Delete (1) button
3. Click on Confirm (4) button
4. After deletion of User profile you will be loged out and redirected to login page

**Delete User profile while keeping Accounts and all related data**

1. Before deleting User profile you should assign a new account owner to all accounts where you have role Account owner role
2. After that you should go to Danger zone tab in user profile page and click on Delete (1) button
3. Enter your e-Mail in upper case to the field (2) in the modal window which opens after click on Delete (1) button
4. Tick Keep Account and Mailboxes (3) checkbox
5. Click on Confirm (4) button
6. If all Accounts where you have Account owner role has other owners your profile will be deleted, you will be loged out and redirected to login page. Otherwise you will see an error message in the right corner of the page

.. image:: pic_userprofile/errorKeepAccount.png
   :width: 600
   :align: center

What happens with user data after deleting a user profile?
==========================================================

After User profile deletion next related data will be deleted as well:

1. Accounts where user has role "Account owner"
2. Mailboxes
3. Templates
4. Dictionaries
5. Contacts
6. Aliases
7. Envelope drafts

.. note:: Envelopes in the middle of the processing flow will not be deleted.