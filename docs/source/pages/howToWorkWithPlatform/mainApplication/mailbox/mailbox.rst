============
Mailbox page
============

Mailbox page contains envelope list divided by folders according to the envelopes statuses. It also allows you to apply next mass action to envelopes:

1. Assigning labels to envelopes
2. :ref:`Signing envelopes with QES and Signature <qualifiedElectronicSignature>`
3. Envelope deletion and restoring
4. Envelope archiving and unarchiving
5. Downloading completed envelopes
6. Sharing envelopes
7. Envelopes chaining and unchaining
8. Envelopes delegation
9. :ref:`Adding envelopes for approval <approval>`
10. Approving envelopes
11. Rejecting envelopes
12. Envelopes report generation
13. Envelopes notification resend

.. image:: pic_mailbox/mailboxPage.png
   :width: 600
   :align: center

.. image:: pic_mailbox/buttons.png
   :width: 400
   :align: center

.. note:: Note for API users: if envelope scope is not defined in envelope search request, only inbox envelopes will be returned.

How to sign envelopes?
======================

You can select envelopes and sign them with specific signing method if selected envelopes contain signature fields.

1. Select required envelopes (envelopes in "Waiting for you" status are eligible for signing)
2. Click the "Sign envelopes" button

.. image:: pic_mailbox/signButton.png
   :width: 400
   :align: center

3. In the opened modal window select a signature type

.. image:: pic_mailbox/signModal.png
   :width: 400
   :align: center

4. If you have selected any type of QES signature please follow the the signing instructions from :ref:`here <qualifiedElectronicSignature>`
5. If you have selected Simple electronic signature please follow the the signing instructions from :ref:`here <simpleElectronicSignature>` (starting from step 3)
6. Follow to third step of the signing modal window to sign all required documents
7. After a successful process you will see a modal window with the results

Next errors can occur during the mass signing process:

1. Active role is different from the Assignee
2. Envelope contains fields except signature fields for active role
3. Envelope contains signature without coordinates (signature the place of which is define by Signer instead of template owner)
4. Signature is placed in an uncompleted dynamic table (table field the assignee of which has not defined final rows quantity yet)

.. _envelopeChain:

How to chain and unchain envelopes?
===================================

You can create envelope chains by linking several envelopes or by adding an envelope to an existing chain.

1. Select required envelopes
2. Click the "Add envelope to chain" button

.. image:: pic_mailbox/chainButton.png
   :width: 400
   :align: center

3. All selected envelopes will be chained after this
4. If you need to add an envelope to existing chain or chain envelope which can't be filtered to be shown on one page, you can select this single envelope and click "Add envelope to chain" button. Modal window will be shown where and you can search for envelope you want to be chained with selected envelope by subject or UUID

.. image:: pic_mailbox/chainModal.png
   :width: 400
   :align: center

5. After selecting an envelope click the "Save" button. Two envelopes will be chained after this

.. image:: pic_mailbox/chainModalSave.png
   :width: 400
   :align: center

6. To remove envelopes from a chain select chained envelopes from the list

.. image:: pic_mailbox/chainedEnvelopesSelected.png
   :width: 400
   :align: center

7. After selecting envelopes click the "Remove envelopes from chain" button

.. image:: pic_mailbox/unchainButton.png
   :width: 400
   :align: center

8. To see a list of envelopes in a chain, open a chained envelope and look for the "Chain" section in the header

.. image:: pic_mailbox/chainSection.png
   :width: 400
   :align: center

9. You can expand it by clicking it to see a list of envelopes in this chain ordered by receive date in a descending order. Current envelope is highlighted. Each envelope in the list can be clicked to open it

.. image:: pic_mailbox/chainSectionExpanded.png
   :width: 400
   :align: center

How to delegate envelopes?
==========================

You can delegate your role in envelopes to other mailbox.

1. Select required envelopes (envelopes in "Waiting for you" status are eligible for delegation)
2. Click the "Delegate envelopes" button

.. image:: pic_mailbox/delegateButton.png
   :width: 400
   :align: center

3. In the opened modal window select a mailbox or enter an email of a user to whom you want to delegate envelopes

.. image:: pic_mailbox/delegateModal.png
   :width: 400
   :align: center

4. Confirm the modal window
5. After a successful process you will see a modal window with the results

How to add envelopes for approval?
==================================

You can request an approval of envelopes from a mailbox which does not participates in the envelope processing flow.

1. Select required envelopes (envelopes in "Waiting for you" and "Draft" statuses are eligible for adding for approval)
2. Click the "Add envelopes for approval" button

.. image:: pic_mailbox/approvalButton.png
   :width: 400
   :align: center

3. Following modal window will open:

.. image:: pic_mailbox/approvalModal.png
   :width: 400
   :align: center

4. Follow the instructions from :ref:`here <approval>`
5. After a successful process you will see a modal window with the results

How to approve envelopes?
=========================

You can complete your active approver role in envelopes.

1. Select required envelopes (envelopes in "Waiting for you" status with active approver role are eligible for approval)
2. Click the "Approve envelopes" button

.. image:: pic_mailbox/approveButton.png
   :width: 400
   :align: center

3. Confirm the following modal window:

.. image:: pic_mailbox/approveModal.png
   :width: 400
   :align: center

5. After a successful process you will see a modal window with the results

How to reject envelopes?
========================

You can reject envelopes if they are not completed yet.

1. Select required envelopes (envelopes in "Waiting for you" and "Pending" statuses are eligible for rejection)
2. Click the "Reject envelopes" button

.. image:: pic_mailbox/rejectButton.png
   :width: 400
   :align: center

3. Following modal window will open:

.. image:: pic_mailbox/rejectModal.png
   :width: 400
   :align: center

4. Enter a cancellation reason anc click the "Reject" button
5. After a successful processed all applicable envelopes from the selection will change status to "Cancelled"

How to generate an envelopes report?
====================================

You can generate a .xlsx report by envelopes.

1. Select required envelopes
2. Click the "Generate report" button

.. image:: pic_mailbox/reportButton.png
   :width: 400
   :align: center

3. Confirm the following modal window:

.. image:: pic_mailbox/reportModal.png
   :width: 400
   :align: center

4. Envelopes report will be sent to your email after this. Note that this can take some time depending on the number of envelopes in the report
5. Filter details is the first tab of the report. It contains the filter configuration of the envelope selection
6. Report data is the second tab of the report. It contains envelope list with details

.. note:: Note for API users: single envelope search request used for mass actions is limited to 1000 envelope UUIDs and will fail if more UUIDs are sent. Also, a limit of 200 UUIDs is applied for next mass action requests: delegate, add for approval and reject. The rest of mass action requests have a limit of 1000 UUIDs, same to search request.