.. _send-for-delegation:

===========================
Envelope delegation process
===========================

Envelope delegation is a process which allows to delegate all actions assigned to recipient mailbox in the envelope processing flow to other mailbox. In other words it can be called envelope forwarding.

How to send envelope for delegation
===================================

1. For delegation you need to open envelope in “Waiting” status and click Delegation button in the upper right corner of the envelope header

.. image:: pic_delegationProcess/delegationButton.png
   :width: 600
   :align: center

.. note:: This button will only appear for mailboxes with delegation permission.

2. In the mailbox field of opened window find and select desired delegate mailbox by name, UUID or alias (or enter email address) and click Confirm

.. warning:: Role can not be delegated to mailbox which is already participating in the specific role

.. image:: pic_delegationProcess/delegationModal.png
   :width: 600
   :align: center

3. When it is done envelope will be received by mailbox which was selected for delegation
4. Delegate will be able to perform all actions which were assigned to initiator role or perform delegation to another mailbox

.. note:: Each delegate can perform delegation to another mailbox (if it is not prohibited by envelope/template configuration or user to mailbox permissions)

.. image:: pic_delegationProcess/delegationCancel.png
   :width: 600
   :align: center

5. Initiator can cancel delegation if delegate has not completed his step in envelope processing flow. In this case delegate will lose access to the envelope. To do this, initiator has to click the Cancel button on the processing flow window

How to configure automatic incoming envelopes delegation
========================================================

It is possible to enable automatic incoming envelopes delegation for selected mailbox (enable automatic envelopes forwarding).

1. Go to Admin panel -> Mailboxes -> Selected mailbox settings

.. image:: pic_delegationProcess/autoDelegation.png
   :width: 600
   :align: center

.. note:: This section will only appear for mailboxes with delegation permission.

2. In mailbox field find and select desired delegate mailbox by name, UUID or alias (or enter email address). It will become a delegate for all incoming envelopes of your mailbox
3. You can specify Effective until date. If selected, forwarding will be automatically disabled day after selected. For example if 18.04.23 is selected, automatic delegation should turn off 19.04.23 at 00:00 (up to 2 hours delay is possible)
4. Make sure to enable Active forwarding toggle if you want to enable delegation to selected mailbox

.. image:: pic_delegationProcess/autoDelegateOptions.png
   :width: 600
   :align: center

5. Click Save changes when all options are configured

.. warning:: Envelopes with restricted delegation will not be automatically forwarded to selected mailbox and still be sent to your mailbox even when forwarding is enabled.

.. warning:: If auto-delegation configured to the delegate who is already have access to the role than delegation will not happen

How to restrict envelope delegation
===================================

It is possible to restrict delegation of any outgoing envelope. Such envelopes can be processed only by recepients specified in envelope flow settings.

1. Envelope delegation can be restricted in template editor. It will affect all envelopes created from this template and can not be overridden on envelope level. This option is disabled by default

.. image:: pic_delegationProcess/denyDelegationTemplate.png
   :width: 600
   :align: center

2. It is also possible to restrict delegation on draft page for each envelope individually if it was not done on template level

 .. image:: pic_delegationProcess/denyDelegationEnvelope.png
   :width: 600
   :align: center