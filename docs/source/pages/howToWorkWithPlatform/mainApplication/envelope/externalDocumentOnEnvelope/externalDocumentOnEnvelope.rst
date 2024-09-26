=================
External Document
=================

How to upload an external document
==================================

1. Click the upload zone

.. image:: pic_externalDocument/ExternalDocument.png
   :width: 600
   :align: center

2. Select a file
3. When the upload is finished you will see name of file inside uploading section (or file itself it it was in .pdf format). Also you can choose another file before you send envelope

.. image:: pic_externalDocument/UploadedFile.png
   :width: 600
   :align: center

4. To send envelope you should fill all other mandatory fields and upload all external documents assigned to your role

How to upload an external document with embedded fields
=======================================================

1. Click the upload zone

.. image:: pic_externalDocument/ExternalDocument.png
   :width: 600
   :align: center

2. Select a file
3. Depending on the type of built-in fields you will see a modal window with different options:

- Keep signatures and fields = Preserve editable fields embedded in the document in read-only state, signature, and/or encryption.
- Keep editable fields data = Preserve editable fields embedded in the document in read-only state, remove signature and/or encryption.
- Remove editable fields = Remove embedded signatures, encryption, editable fields in the document.

.. image:: pic_externalDocument/ExternalDocumentEmbeddedModal.png
   :width: 600
   :align: center

.. note:: If the external document contains E-ink signature the option "Keep signatures and fields" will be unavailable. In this case, it is impossible to retain built-in signatures.

4. Depending on the selected option, the PDF document will be rendered, and you can continue working with the envelope in the usual manner

External document signing process
=================================

Electronic digital signature and e-ink signatures can be used to sign external documents. According signatures should be added to the documents on the template.

.. note:: Electronic ink signatures can be applied only to .pdf format external documents. Please note that if you will add e-ink signature to external document in the template, only .pdf files will be accepted for this documents in following envelopes.

Process of signing external documents with QES has one difference from signing internal document. When signing external document electronic digital signature is applied only to .pdf file version (not to .xml file). Signature interface is same as for structured documents.

.. image:: pic_externalDocument/ExternalDocumentQES.png
   :width: 600
   :align: center

How to add an e-ink signature to external document
==================================================

1. To add e-ink signature to the external document click the signature field

.. image:: pic_externalDocument/ExternalDocumentEink.png
   :width: 600
   :align: center

2. After this place signature where you want it to be and click. The signature can be changed by clicking it

.. image:: pic_externalDocument/ExternalDocumentEinkDone.png
   :width: 600
   :align: center

3. When this is done you can finish filling all mandatory fields and send the envelope - all signatures will be shown on it