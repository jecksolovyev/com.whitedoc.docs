.. role:: red

===================================
Sign document(s) with QES using API
===================================

The algorithm of signing documents on WhiteDoc using API

1. Request binary data or hashes for sign (hashes are more likely used)
2. Sign the binary data or hashes on the external signing service (or using crypto library from IIT)
3. Send sign request on WhiteDoc side to complete the signing step of the envelope processing flow


.. note::
    You can sign document if document has signature field.

    Signature field must be assigned to the role which has the same mailbox as mailbox under the signing process.

    To sign document or documents you have to retrieve required document from the envelope. To this purpose use for-sign request or for-sing-file request.


For-sing request
================

To request documents for sign you have to use request below, where you pass all required and optional params in body. Detailed information about the request you can find by `FOR SIGN LINK <https://api.whitedoc.ua/swagger-ui/index.html#/envelope-controller/getDocumentsForSign>`_

for example: normal request will include the following body, which matches the current approach on web.

- signatureAlgorithm determines from the template
- skipBinaryFiles is true because we do need to sign binary file, in our approach we're signing hashes to make the signing smoother and faster
- documentId and respective signatureName we're getting from the template and according to the active role (if role is not active or already completed the request will retrieve error)
- tin gets from the key user wants to sign (key and certificated should be already read for verification purpose). If tin passed in request will be different from tin configured for this signature, it will retrieve the error "50060".

.. code-block:: json

    [
        {
            "signingCertificate": "MIIFzzCCBXegAwIBAgIUXphNUm+C848EAAAAqnhQAVi1kQYwDQYLKoYkAgEBAQEDAQ...",
            "skipBinaryFiles": true,
            "signatureAlgorithm": "DSTU4145"
            "tin": "1234567890"
            "documents": [
                {
                    "documentId": "5d04328c-0d8e-406a-bc06-19ddd6e5600b",
                    "signatureName": "QES",
                },
                {
                    "documentId": "0920c1ec-e497-42d1-b4b3-3fa7d77acc10",
                    "signatureName": "The name",
                }
            ]
        }
    ]


.. list-table::
   :widths: 10 90

   * - Method
     - POST
   * - URL
     - ``api/v1/envelope/{envelopeUuid}/for-sign``
   * - Authorization
     - Bearer {token}
   * - content-type
     - application/json
   * - mailboxUuid
     - {uuid}
   * - Body structure
     - .. code-block:: json

        {
            "signingCertificate": "string",
            "skipBinaryFiles": true,
            "signatureAlgorithm": "DSTU4145",
            "tin": "string",
            "documents": [
                {
                    "documentId": "string",
                    "signatureName": "string"
                }
            ]
        }
   * - Body details
     - **signingCertificate**
        Certificate which will be used for signing, signing library should provide
       **skipBinaryFiles**
        Specify if original binary files are needed in response, if not, only hashes will be returned
       **signatureAlgorithm**
        Check signature algorithm in advance DSTU4145 or ECDSA_RSA
       **signatureAlgorithm**
        Check Tax Individual Number in advance, TIN usually stored within the key
       **documents** :red:`*`
        Array of the documents which are going to be signed and respective signatures names
            * **documentId** :red:`*` - the document ID from template xml which has been used to create envelope
            * **signatureName** :red:`*` - the signature field Name from template xml which has been used to create envelope

For-sing response
=================

The response returns the all required information to perform signature using crypto library. In our case described above hashes of the documents.

.. code-block:: json

    [
        {
            "documentId": "5d04328c-0d8e-406a-bc06-19ddd6e5600b",
            "xmlName": "New document.xml",
            "xml": null,
            "xmlHash": "9HHJjqqldGXzzPJJi/Bdt91YLPw3TKvJF5m4V0mjoAM=",
            "binaryFileName": "New document.pdf",
            "binaryFile": null,
            "binaryHash": "b7GzpxMgeCB52VQYwHtsEf4ouZzFMUp20j19PZuDGcE=",
            "stampHash": "b7GzpxMgeCB52VQYwHtsEf4ouZzFMUp20j19PZuDGcE=",
            "signatureAlgorithm": "DSTU4145",
            "signatureContainer": "P7S",
            "signatures": [
                {
                    "name": "QES",
                    "stampRequired": false,
                    "type": "P7S",
                    "tin": null
                }
            ]
        },
        {
            "documentId": "0920c1ec-e497-42d1-b4b3-3fa7d77acc10",
            "xmlName": null,
            "xml": null,
            "xmlHash": null,
            "binaryFileName": "New external document - docsChooseNoTitle.png",
            "binaryFile": null,
            "binaryHash": "3YZBSCujWc9VFOkFnKySJAXIBIQAseTGUBtfY17olhk=",
            "stampHash": "3YZBSCujWc9VFOkFnKySJAXIBIQAseTGUBtfY17olhk=",
            "signatureAlgorithm": "DSTU4145",
            "signatureContainer": "P7S",
            "signatures": [
                {
                    "name": "The name",
                    "stampRequired": false,
                    "type": "P7S",
                    "tin": null
                }
            ]
        }
    ]

Below you can find information related to response fields.

.. list-table::
   :widths: 10 90

   * - Response structure
     - .. code-block:: json

        [
            {
                "documentId": "string",
                "xmlName": true,
                "xml": "DSTU4145",
                "xmlHash": "string",
                "binaryFileName": "string",
                "binaryFile": "string",
                "binaryHash": "string",
                "stampHash": "string",
                "signatureAlgorithm": "string",
                "signatureContainer": "string",
                "signatures": [
                    {
                        "name": "string",
                        "stampRequired": "string"
                        "type": "string",
                        "tin": "string"
                    }
                ]
            }
        ]
   * - Response details
     - **documentId**
        The document ID from template xml which has been used to create envelope
       **xmlName**
        The name of the document XML file which need to be signed (may be empty if no xml in the document)
       **xml**
        The document XML which need to be signed (may be empty if no xml in the document) or if skipBinaryFiles === true
       **xmlHash**
        The Hash of the document XML which need to be signed (may be empty if no xml in the document)
       **binaryFileName**
        The name of the document file which need to be signed
       **binaryFile**
        The binary data of the document file which need to be signed
       **binaryHash**
        The hash data of the document file which need to be signed
       **stampHash**
        The hash for the stamp data of the document file which need to be signed
       **signatureAlgorithm**
        Signature algorithm which has to be used for signing the document "DSTU4145"|"ECDSA_RSA"
       **signatureContainer**
        Signature container which need to be used for signing (can be determined from template XML) "P7S"|"ASICE"
       **signatures**
        Array of the documents which are going to be signed and respective signatures names
            * **name** - Signature field name
            * **stampRequired** - determines if the stamp required for this signature or not
            * **type** - the type of the signature "PADES", "P7S" or "ASICE"
            * **tin** - is TIN validation required for the signature (if in request it has not been passed but in the response you get it means the validation will be required on the signing step)

Sing request
============

When documents are signed on external service or using crypto library from IIT the results may be used for signing on WhiteDoc and completion the envelope processing step. Detailed information about the request you can find by `SIGN LINK <https://api.whitedoc.ua/swagger-ui/index.html#/envelope-controller/sign>`_

.. list-table::
   :widths: 10 90

   * - Method
     - PUT
   * - URL
     - ``/api/v1/envelope/{envelopeUuid}/sign``
   * - Authorization
     - Bearer {token}
   * - content-type
     - application/json
   * - mailboxUuid
     - {uuid}
   * - Body structure
     - .. code-block:: json

        [
            {
                "documentId": "string",
                "signatureName": "string",
                "signatures": [
                    {
                        "source": "string",
                        "stamp": "true"
                        "data": "string"
                        "certificate": "string"
                    }
                ]
            }
        ]
   * - Body details
     - **documentId** :red:`*`
        The document ID from template xml which has been used to create envelope
       **signatureName** :red:`*`
        The signature field Name from template xml which has been used to create envelope
       **signatures** :red:`*`
        Array of the documents which are going to be signed and respective signatures names
            * **source** :red:`*` - signature source type "binary"|"text", if it is xml/xmlHash should be "text", otherwise "binary"
            * **stamp** :red:`*` - if the signature is a stamp, should be true
            * **data** :red:`*` - signature in base64 format
            * **certificate** - optional X.509 certificate in base64

As the response of the request above will be status code 200 or error in case of any validation issues