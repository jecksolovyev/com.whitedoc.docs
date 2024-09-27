.. _accountSettings:

============
Settings tab
============

Settings is a page with account properties that help to identify and manage the account. Data from account is used for mailboxes creation and billing. From here you can :ref:`manage your accounts<accountSettings>`, :ref:`configure domains<domains>`, :ref:`add SSO providers<ssoProviders>`, :ref:`create external links<externalLinks>`, :ref:`configure password policy<passwordPolicyConfig>`, and :ref:`manage cloud signatures<cloudSignature>`.

.. image:: pic_accountSettings/settings.png
   :width: 600
   :align: center

How to update account name?
===========================

1. Click the "Name" input
2. Edit account name (min 3 to max 256 symbols)

.. image:: pic_accountSettings/settingsName.png
   :width: 600
   :align: center

3. CLick the "Save" button
4. Success message will appear and name will be updated

How to copy account UUID?
=========================

1. Click the "Copy account UUID" button
2. Success message will appear and UUID will be copied to the clipboard

.. image:: pic_accountSettings/settingsCopyUuid.png
   :width: 600
   :align: center

How to configure automatic mailbox creation for corporatre users?
=================================================================

.. note:: This section will be visible and active only if you have the 10014 (rolesListView) account permission and your account has at least one verified domain.

1. Enable the toggle switch in this sections

.. image:: pic_accountSettings/settingsAutomaticMailboxCreation.png
   :width: 600
   :align: center

2. In the "Mailbox role" input select the mailbox role which will be assigned to the corporate users for automatically created mailboxes
3. You can start typing in the role name in the input to narrow the roles list
4. After clicing on the required role click the "Save" button
5. Success message will appear and settings will be saved

How to upload an account and platform images?
=============================================

1. Images can be uploaded in the "Account icon settings" and "Platform logotype settings" sections

.. image:: pic_accountSettings/settingsImages.png
   :width: 600
   :align: center

2. Click the respective "Upload" button and choose the image (click the info icon to view image requirements)
3. Click the "Save" button
4. Default logo can be restored by the "Set default" button. In this case account logo will consist on two first letters of the account name, and WhiteDoc logo is used for platform logo

How to delete an account?
=========================

1. Click the "Delete" button
2. Modal window will appear

.. image:: pic_accountSettings/settingsDelete.png
   :width: 600
   :align: center

3. Type your user email in uppercase in the email input
4. Click the "Confirm" button

.. _domains:

===========
Domains tab
===========

This page allows to manage, verify and activate domains. Domains are necessary for corporate users creation.

.. image:: pic_accountSettings/domains.png
   :width: 600
   :align: center

How to add a domain?
====================

1. Click the "Add domain" button
2. Enter the name of a domain that you own and confirm your action

.. image:: pic_accountSettings/domainsAdd.png
   :width: 600
   :align: center

3. If domain is existing, we can ping it and if the domain has not been verified by anyone else yet, it will be added to the domains list

How to verify a domain?
=======================

1. Add a domain
2. You will see a window with instructions

.. image:: pic_accountSettings/domainsVerify.png
   :width: 600
   :align: center

3. Copy data from the modal and enter to the respective field on the DNS configuration of your domain
4. Click the "Verify" button on modal window and system automatically tries to confirm you ownership
5. As soon as system get proofs of your ownership admin get email notification related to successful domain verification on the platform

How to activate a domain?
=========================

1. Click the "Activate" button near an inactive domain
2. Domain is active

How to delete a domain?
=======================

1. Click the "Delete" buttoin near a domain
2. Confirm you action

.. note:: If verified domain is deleted you will lose the ability to manage user in it.

.. image:: pic_accountSettings/domainsDelete.png
   :width: 600
   :align: center

.. _ssoProviders:

=================
SSO providers tab
=================

You can set authorization via SSO for your corporate users. To do this, you need to create a domain and verify it on the platform. Next, you need to create an ISP SSO and connect it to the domain.

.. image:: pic_accountSettings/ssoProviders.png
   :width: 600
   :align: center

How to add an SSO provider?
===========================

1. Click the "Add SSO provider" button. A  window will open. Fill in the main fields. You can choose the Metadata type. Provide URL or XML. Once you have filled in all the data click the "Add" button

.. image:: pic_accountSettings/ssoProvidersAdd.png
   :width: 600
   :align: center

2. Go to the :ref:`domains tab <domains>`. Chose active domain and click the "Manage SSO setting" button near it. Window will open

.. image:: pic_accountSettings/ssoProvidersDomain.png
   :width: 600
   :align: center

3. Select the available SSO procider and confirm your action
4. After SSO is connected to the domain, your corporate users will be able to log in via SSO
5. Corporate user enters your corporate domain and fills out an authorization page, as a result of which he will be successfully authorized or receive a message that he needs to register via SSO.

.. _externalLinks:

==================
External links tab
==================

This page allow to manage list of the links to the external resources.

.. image:: pic_accountSettings/externalLinks.png
   :width: 600
   :align: center

How to add an external link?
============================

1. Click the "Add link" button. Window will appear

.. image:: pic_accountSettings/externalLinksAdd.png
   :width: 600
   :align: center

2. Enter link name, url and access level. If you choose account access level for link all users who have access to mailboxes from this account will see the link. If you set as access level specific mailbox only users who have access to this mailbox will see the link
3. Popup will be closed and new link will be added to the end of the existing links list
4. You can edit and delete links by clicking the "Edit and "Delete" buttons
5. Drag the links by the "Reorder" icon to update links order

.. _passwordPolicyConfig:

===================
Password policy tab
===================

You're able to configure password and session policy for all users with verified domains in your account. You can make it more strict than default system configuration. To do that follow next instructions. More info on password policy can be found :ref:`here <passwordPolicy>`.

.. image:: pic_accountSettings/passwordPolicy.png
   :width: 600
   :align: center

How to change password or session policy?
=========================================

1. First of all verify any domain. It's necessary to do, because without users with verified domains rules won't work
2. Open /admin/account-settings?activeTab=password-policy page
3. Make rule stricter than default system rule and save changes

After actions above password or session policy will be applied for any user with email from verified domain.

How to make password policy more strict?
========================================

There are a lot of password policy and session policy options:

1. Minimum password length. It means that minimal quantity of symbols in password should be not less than configured, so to make this option stricter you can use value bigger or equal than default value "min-length" in configuration
2. Maximum password length. It means that maximum quantity of symbols in password shouldn't be bigger than configured, so to make this option stricter you can user value lower or equal than default value "max-length" in configuration
3. Require uppercase letters. It means that password should contain at least N uppercase letters where N is value "uppercase" in configuration. To make it stricter use value bigger or equal as in configuration. But don't use quantity of symbols bigger than maximum available length of password
4. Require lowercase letters. It means that password should contain at least N lowercase letters where N is value "lowercase" in configuration. To make it stricter use value bigger or equal as in configuration. But don't use quantity of symbols bigger than maximum available length of password
5. Require numeric value. It means that password should contain at least N numeric symbols where N is value "digit" in configuration. To make it stricter use value bigger or equal as in configuration. But don`t use quantity of symbols bigger than maximum available length of password
6. Require at least one special character. It means that password should contain at least N special characters where N is value "special-symbol" in configuration. To make it stricter use value bigger or equal as in configuration. But don't use quantity of symbols bigger than maximum available length of password
7. Do not allow repeat. It means that password shouldn't contain repeated symbols. So if in configuration is "Don't allow repeat" value 3, you can't use three repeated characters ("111", "aaa" or etc.). To make this option stricter use lower or equal value "repeat-character" as in configuration
8. Allow whitespace in password. This option allows or disallows to use whitespaces in password
9. Do not allow the use of forbidden passwords. This option allows or disallows to use forbidden passwords
10. Do not allow the use of forbidden words. This option allows or disallows to use forbidden words in password
11. Enable password expiration. This is option which responsible for password expiration. If you want to make stricter rules set value lower than value "expiration-days" in configuration
12. Send password expiration notification. This is option which responsible for quantity of days for password expiration notification. To make it stricter set value "notify-before-days" lower than in configuration
13. Do not allow reuse of passwords. Option which is responsible for period of time which password can't be re-used. To make it stricter set value "prevent-reuse-months" bigger than in configuration
14. Do not allow reuse of recent. Option which is responsible for quantity of previous password which can't be re-used. To make it stricter set value "prevent-reuse-count" bigger than in configuration

How to make session policy more strict?
=======================================

1. Keep session during idle period. Option which is responsible for time while session is active in idle. To make it stricter set value "session-hours" lower than in configuration
2. Single session for one user. Option which allows or disallows single browser session
3. Single user session per IP. Option which allows or disallows single IP session
4. Maximum login attempts before locking. Option which is responsible for quantity of incorrect password user enters before locking. To make it stricter set value "max-login-attempts" lower than in configuration
5. Lock time after multiple login attempts. Option which is responsible for period of time on which user will be locked. To make it set value "max-attempts-timeout-minutes" bigger than in configuration
6. The list of allowed IPs. The list of IP addresses from which users are able to log in on platform
7. The list of blocked IPs. The list of IP addresses from which users aren't able to log in on platform

.. _cloudSignature:

===================
Cloud signature tab
===================

Cloud signature is one of the many ways to sign document with Qualified Electronic Signature. And on this page will be described how to configure cloud signature for your corporate account.

.. image:: pic_accountSettings/cloudSignature.png
   :width: 600
   :align: center

How to add a cloud signature?
=============================

Owner or user who has respective permissions to corporate account can configure Cloud signature for all corporate users and users with verified corporate domains can use Cloud signature. The short instruction here: Go to Admin panel, select Account Settings. On Account Settings page, select Cloud Signature tab.

1.  Click the "Add setting" button
2.  Fill configuration form. Name of the signature can be any you want, URL should contain address to the signature server and port should respect to available port to connect

.. image:: pic_accountSettings/cloudSignatureAdd.png
   :width: 600
   :align: center

3. After filling, click the "Save" button
4. You can edit and delete configurations by clicking the "Edit and "Delete" buttons