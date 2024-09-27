==============================
Envelope management on mailbox
==============================

Envelope management on listing page includes following functionality:

1. Labels assignment to envelopes
2. :ref:`Signing envelopes with QES and Signature <qualifiedElectronicSignature>`
3. Envelope deletion functionality
4. Archiving and unarchiving envelopes
5. Downloading completed envelopes
6. Sharing envelopes
7. Chaining envelopes
8. :ref:`Sending envelopes for approval <approval>`
9. Cancelling envelopes
10. Envelopes report generation
11. Envelopes notification resend

Signing envelopes with QES and Signature
========================================

You can select one or several envelopes and sign them with specific signing method if selected envelopes contain signature fields. To do this select envelope(s) and select specific signing type you want (signature type selector available in signing modal window).

 - If you select any type of QES signature please follow the instruction in the signing :ref:`here <qualifiedElectronicSignature>`.
 - If you select Signature type of signing you need to do the following:

1. Draw signature or select text variant of the signature if you don't have saved yet. Or keep saved signature
2. Follow to third step of the signing modal window to sign all documents you need
3. When signing process completed you will see positive or negative results of signing process

.. note:: If some validation occurred with signing of document you'll be notified with toaster message in right top corner of the page and in tooltip on red alert icon against failed envelopes

Validation which can occur:

1. Active role is different from Assignee
2. Envelope contains fields except Signature fields for active role
3. Envelope contains signature without coordinates (signature the place of which define Signer instead of template creator)
4. Signature placed in uncompleted dynamic table field (table field the owner of which has not define quantity of rows yet)
    
How to send several envelopes for approve
=========================================

You can send envelope or envelopes for approve from the envelope list page. To do this you should select respective envelope or envelopes in status Draft or Waiting for you, click the "Approve" icon in the header of the table and select flow or create new one as described :ref:`here <approval>`. After successful approval request you will see modal window with results of the approval request.

How to cancel several envelopes
===============================

You can cancel envelope or envelopes from the envelope list page. To do this you should select respective envelope or envelopes in statuses Pending (if user was initiator of the envelope) or Waiting for you, click the "Cancel envelopes" icon (looks like the circle with x) in the header of the table and in the modal window enter the comment if needed and confirm action. After successful cancel action all selected envelopes change status to CANCELLED.If envelopes in statuses other then allowed are selected, error message will be displayed after confirmation of the action.