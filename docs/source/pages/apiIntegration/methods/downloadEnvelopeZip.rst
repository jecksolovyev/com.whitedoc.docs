===================================
Download envelope documents archive
===================================

Everyone who has access to envelope can download it. You can download a full envelope or specific document from it with following request:

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

Query parameters for ZIP contents configureation
================================================

Depending on a query parameters you can configure what will be included in the archive:

1. Send a request without query parameters — downloads full envelope (all documents contained in the envelope such as audit trail, folder with original documents for each document, printable versions, signatures, processing/signing certificates)
2. Send a request with documentId in query parameters — downloads an archive of a specific document (all documents related to a certain document in the envelope defined by documentId such as original documents, printable versions, signatures, processing/signing certificates and envelope audit trail)
3. Send a request with excludeFiles in query parameters — downloads an archive excluding specified files (if send excludeFiles=c — processing/signing certificates will be excluded from the archive; if send excludeFiles=p — printable version of the documents will be excluded from the archive; if send excludeFiles=a — audit trail will be excluded from the archive)

.. note:: You can combine mask of excludeFiles, excludeFiles=cp will exclude processing/signing certificates and printable version of documents.

ZIP archive with documents will be returned in response.

ZIP content depending on the document state
===========================================

Depending on the document state you will receive different ZIP content

1. If not all dynamic fields (such as text, number, currency, date and time, dropdown, choice, a/b, checkbox, file, dictionary, lookup, dynamic table, duplicate, formula, autonumber, signature) are filled in inside the document — you will only get audit trail in the archive, because platform is not able to generate files while document is not completed
2. If the document is completed and all dynamic fields are filled (described above) — you will get a ZIP with original documents, printable versions and processing/signing certificates
3. If the document is completed, all dynamic fields are filled (described above), and at least one QES is applied to the document — you will get a ZIP with original documents, printable versions, signatures which are already set, and processing/signing certificates

.. note:: ZIP content will change dynamically according to the processing flow step and documents state, so in different phases of envelope processing flow you may get different content in a ZIP with a same request.