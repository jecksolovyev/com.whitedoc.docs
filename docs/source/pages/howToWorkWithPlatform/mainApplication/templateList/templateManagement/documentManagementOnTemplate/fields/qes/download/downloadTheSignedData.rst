=========================================
Download or send to print the signed data
=========================================

How to download the signed data?
================================

You can download either a single signed document or the full envelope archive (documents + signatures).

* Full envelope archive or document only archive becomes always available when the envelope is completed - i.e., when all roles have finished their actions.
* Downloading the full envelope archive or document only archive before completion is available only if enabled in the template settings. If this option is not enabled, the archive can be downloaded only after the envelope is completed, but you can download specific documents.

To dowload the documents archive you should do the following:

If the envelope is completed:

1. Open envelope
2. Click the respective "Download envelope" button in the header. Here you can choose 3 option, such as download the full archive, documents and printable versions or documents only.

.. image:: pic_download/downloadEnvelope.png
   :width: 600
   :align: center

3. Alternatively, click the respective "Download archive" button ahead document name to see the same options.
As soon as you click the “Download document” button, an archive containing the document(s) will be downloaded to your device.

.. image:: pic_download/downloadDocument.png
   :width: 600
   :align: center

You can also download multiple envelopes in bulk:

1. Click the "Mailbox" button on the left sidebar.
2. Select the envelopes you want to download.
3. Click the More options (⋮) menu.
4. Click the "Download envelopes" button and choose the option you need.

.. image:: pic_download/downloadEnvelopeOnListingPage1.png
   :width: 400
   :align: center


You can download the full envelope archive even when the envelope is not completed (availability depends on the template settings):

1. Open envelope
2. Click the respective "Download envelope" button in the header. Here you can choose 3 option, such as dowload the full archive, documents and printable versions or documents only.

.. image:: pic_download/downloadEnvelopeBeforeCompletion.png
   :width: 600
   :align: center

3. Alternatively, click the respective "Download archive" button ahead document name to see the same options.
As soon as you click the “Download document” button, an archive containing the document(s) will be downloaded to your device.

.. image:: pic_download/downloadDocumentBeforeCompletion.png
   :width: 600
   :align: center


What are you downloading?
=========================

You download the archive with the zip extension.

* If you download a specific document.

Inside the archive will be a file with the extension .pdf, a file with the extension .xml, files with captions in .p7s format (qunatity of files depends on qunatity of signers nultiple twice for each document), signing certificate with .pdf extension and name: DocumentName.signatures.pdf. Where DocumentName it's name of the document you downloaded and printable version of the document with .pdf extension which include visual expression of signatures and signing certificate in one file.

* If you download the entire envelope.

There will be several folders inside the archive (if the envelope consists of several documents). Folder names match document names accordingly. Inside their folders are the above-mentioned files (pdf, xml and p7s), as well as an AuditTrail file.

The signing document certificate
================================

In the signing document certificate you can find information about the document, signers, signs and stamps. 

1. Document information section contains

* Envelope UUID - unique identifier of the envelope
* Envelope subject - subject of the envelope to which document relates
* Document ID - unique identifier of the document
* Title of the document - sublject of the document
* Date of the document - it is date of creation of envelope
* Template UUID - unique identifier of the template by whcih envelope has been created
* Template version - unique identifier of the template version
* File name - name of the signed file
* Number of signatures - quantity of the document signers
* Electronic version of the document - link to the envelope on the web platform

.. image:: pic_download/firstPageAndSign.png
   :width: 600
   :align: center

2. Section about the signer, sign and/or stamp contains (if it's signature you will see key icon opposite table block with data and if it's stamp you will see stamp icon opposite table block with data)

* Owner - name of the signature owner
* Organization - name of the organiztion to which signature belongs
* Position - signer position in the compnay
* DRFO(ITN)/EDRPOU - Identification code of signer or company
* Certificate serial number - number of the certificate with which system can garantor identity of the signer
* Date of signing - date of the signing document
* File name - signed file with extension

.. image:: pic_download/stampExample.png
   :width: 600
   :align: center

3. Explanation what is QES and instructions how to check validity of the QES

.. image:: pic_download/FAQ.png
   :width: 600
   :align: center

Printable version of the document
=================================

Printable version of the document you can get in two ways. First is described before and you can it download with signed data in archive. The second one is to open document to print from envelope page.

1. As soon as document completed you will see icon "Print" near document

.. image:: pic_download/printBtn.png
   :width: 600
   :align: center

2. You can click it and document opens for print in PDF format

*Document structure is:*

1. Document with signatures labels on first page

.. image:: pic_download/signedDocument.png
   :width: 600
   :align: center

2. Signing document sertificate without instructions and explanation (described in topic above)

*Signature label contains the following information:*

.. image:: pic_download/signatureLabel.png
   :width: 600
   :align: center

1. Legal name of signer
2. Type of signature or stamp (Advanced or qualified)
3. ITN/EDRPOU/DRFO value, according to signature data
4. Data and time of the signature set
5. Certificate serial number according to legal data