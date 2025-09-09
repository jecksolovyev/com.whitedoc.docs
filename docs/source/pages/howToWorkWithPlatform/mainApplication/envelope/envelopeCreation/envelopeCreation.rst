=================
Envelope creation
=================
    
There are several ways to create an envelope:

1. Create an envelope via Quick send button on the dashboard. More details on this can be found :ref:`here <dashboard>`

2. By clicking "New envelope" button on the dashboard

.. image:: picEnvelopeCreation/createFromDashboard.png
   :width: 400
   :align: center

3. By clicking any template panel on the dashboard

.. image:: picEnvelopeCreation/createFromDashboardTemplate.png
   :width: 400
   :align: center

4. By clicking any template panel on the templates list page

.. image:: picEnvelopeCreation/createFromTemplates.png
   :width: 400
   :align: center

5. By clicking "Send" button in the template editor

.. image:: picEnvelopeCreation/createFromEditor.png
   :width: 400
   :align: center

6. By cloning existing envelope. Please note that if mailbox has no access to the template of origin or envelope is created via Quick-send, 'Clone' button will not be shown

.. image:: picEnvelopeCreation/createFromExisting.png
   :width: 400
   :align: center

7. Envelope draft will be opened

.. image:: picEnvelopeCreation/envelopeFlow.png
   :width: 400
   :align: center

From this page you will have to fill all roles that take part in envelope processing flow (unless they are predifined on the template level). Note that you can enable "I am assignee/approver/signer" attribute to predefine your own mailbox for specified role. After all mandatory fields will be filled you can send envelope to the next participant of the flow.

.. note:: You can also save an envelope draft with some values filled in to send it later. You can do so by clicking "Save draft" button (not available for quick-send). After draft is saved, it will be automatically re-saved after any changes are made. Saving process is indicated by save icon near "Save draft" button. Same auto-save feature is also used in envelopes in "Waiting for you" status.

.. note:: It is possible to `add <https://docs.docstudio.com/en/latest/pages/api/openApi.html#tag/envelope-controller/operation/updateEnvelopeMetadata>`_ and `delete <https://docs.docstudio.com/en/latest/pages/api/openApi.html#tag/envelope-controller/operation/deleteEnvelopeMetadata>`_ metadata to the envelopes. It is only available for API users and this data will also only be visible to API users only. Metadata can also be `added to envelope forms <https://docs.docstudio.com/en/latest/pages/api/openApi.html#tag/form-controller>`_ and will be used in all envelopes created from such forms.