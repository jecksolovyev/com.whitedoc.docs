===================================
Download envelope documents archive
===================================

Everyone who has access to envelope can download it. You can download full envelope or specific document from this envelope with following request:

.. list-table::
   :widths: 10 90

   * - Method
     - POST
   * - URL
     - ``/api/v1/envelope/{envelopeUuid}/zip``
   * - Authorization * (required)
     - Bearer {token}
   * - content-type
     - application/json
   * - mailboxUuid * (required)
     - {uuid}
   * - envelopeUuid * (required)
     - {uuid}
   * - documentId
     - {uuid}
   * - excludeFiles
     - Mask to exclude some files. c - for signature/processing Certificate, p - for Printable version, a - for Audit trail
   * - zipStructureName
     - The name of pre-saved zip structure in the template

ZIP content depending on query params
=====================================

Depending on query parameter you can control what will be included in archive:

1. Send request without query parameter - download full envelope (all documents which contain envelope such as audit trail, folder for each document with original documents, printable versions, signatures, processing/signing certificates)
2. Send request with documentId in query parameter - download archive for specific document (all documents related to document defined as documentId such original documents, printable versions, signatures, processing/signing certificates and envelope Audit trail)
3. Send request with excludeFiles in query parameter - download archive excluding specified files (if send excludeFiles=c than processing/signing certificates will be excluded from archive, if send excludeFiles=p than printable version of documents will be excluded from archive, if send excludeFiles=a than Audit trail will be excluded from archive)

.. note:: you can combine mask of excludeFiles, excludeFiles=cp will exclude processing/signing certificates and printable version of documents

Zip archive with documents will be sent in response.

ZIP content depending on document state
=======================================

Depending on document state you will receive different ZIP content

1. If not all dynamic fields (such as text, number, currency, date and time, dropdown, choice, a/b, checkbox, file, dictionary, lookup, dynamic table, duplicate, formula, autonumber, signature) are not filled in inside the document you will get only Audit trail in archive because platform is not able to make files until document not completed
2. If document completed and all dynamic fields filled in (described above) you will be able to get ZIP with original documents, printable versions, processing/signing certificates
3. If document completed, all dynamic fields filled in (described above) and at least one QES applied to the document you will be able to get ZIP with original documents, printable versions, signature or signatures which already set, processing/signing certificates

.. note:: ZIP content would be dynamically change according to processing flow and documents state, so in different phase of envelope processing flow you may get different content in ZIP even if send same request

