.. _envelopeForm:

==============
Envelope forms
==============

Envelope forms allow to create and send envelopes with predefined field values. Forms can be created from templates with fields and assigned roles. When a user opens an envelope form link, they will see a page where they can fill in the required fields. Please note that form creation can only be done via `API <https://docs.docstudio.com/en/latest/pages/api/openApi.html#tag/form-controller>`_.

1. It is possible to configure forms to have :ref:`metadata that will be added to all envelopes created from such forms <envelopeMetadata>`. Metadata can be used to store additional information about the envelope that is not part of the document itself. Metadata can also be used for filtering and searching envelopes in the mailbox
2. It is also posible to add callbacks to the forms which will send the envelope ID to a specified URL when an envelope is created from the form. This can be useful for integrating with other systems and automating workflows. Such callbacks will be removed automatically after the form deletion of after a single-use form was used