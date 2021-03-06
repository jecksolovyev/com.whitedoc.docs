Dynamic fields
===============

.. toctree::

**Text field**

+---------------------------------------------------------------------------------------------------------------------------------+
|                                                       Text field                                                                |
+=================================================================================================================================+
|               `<field type="text" name="name" placeholder="Placeholder text" roleId="UUID" multilines="true|false" />`          |
+---------------------------------------------------------------------------------------------------------------------------------+

 - multilines - boolean, multiline or single line text, multiline should be textarea on UI, optional, default false

**Number field**

+---------------------------------------------------------------------------------------------------------------------------------+
|                                                       Text field                                                                |
+=================================================================================================================================+
|  `<field type="number" name="name" placeholder="Placeholder text" roleId="UUID" precision="integer" min="float" max="float" />` |
+---------------------------------------------------------------------------------------------------------------------------------+

 - min, max - default 'infinite'
 - precision - default 0


**Money field**

+---------------------------------------------------------------------------------------------------------------------------------+
|                                                       Text field                                                                |
+=================================================================================================================================+
|         `<field type="money" name="name" placeholder="Placeholder text" roleId="UUID" min="float" max="float" />`               |
+---------------------------------------------------------------------------------------------------------------------------------+

 - max - default 'infinite'
 - min - default 0
 - precision = 2 (always)


**Datetime field**

+---------------------------------------------------------------------------------------------------------------------------------+
|                                                   Datetime field                                                                |
+=================================================================================================================================+
|         `<field type="datetime" name="name" placeholder="Placeholder text" roleId="UUID" time="boolean" />`                     |
+---------------------------------------------------------------------------------------------------------------------------------+

 - format: IS8601
   accept both:
     - 2019-12-31T23:59:59+02:00
     - 2019-12-31T23:59:59Z
 - time - optional (send only if true)


**Select-dictionary field**

+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                                                                       Dropdown field                                                                              |
+===================================================================================================================================================================+
| `<field type="select-dictionary" name="name" placeholder="Placeholder text" roleId="UUID" dictionaryUuid="UUID" columnUuid="UUID" allow-custom-value="true" />`   |
+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+

 - "allow-custom-value" - allow choose custom value if not exists in dictionary
 - dictionaryUuid - dictionary uuid for dict|strict-dict subtypes, optional, required for dict|strict-dict
 - columnUuid - uuid of dictionary column, which value should be taken as text value


**Lookup field**

+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                                                                       Dropdown field                                                                              |
+===================================================================================================================================================================+
| `<lookup name="name" relatedTo="dictionary field name" documentId="uuid of document" columnUuid="uuid of dictionary column" placeholder="text when not set" />`   |
+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+

 - relatedTo - name of dictionary to which lookup will be connected
 - documentId - document id from which we take dictionary field
 - columnUuid - uuid of dictionary column, which value should be taken as text value

**E-sign**

+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                                                                       Text field                                                                                  |
+===================================================================================================================================================================+
|                                      `<field type="einksign" name="name" placeholder="Placeholder text" roleId="UUID" />`                                         |
+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Field value size limited up to 10kb. Field value - base64 encoded png image, size up to 300x300

**Yes/No**

+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                                                                       Text field                                                                                  |
+===================================================================================================================================================================+
|                           `<field type="yesno" name="name" roleId="UUID" valueYes="Так, я згоден" valueNo="Ні, не згоден!" />`                                    |
+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Values: exact value from template attribute valueYes or from template attribute valueNo.

**Table**

+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                                                                       Text field                                                                                  |
+===================================================================================================================================================================+
|`"<table name="priceList" class="table-stripped" iterable="true" roleId="UUID"> <thead><tr><th>Name</th></tr><tr iterable="true" name="name"><th><field .../></th> |
| </tr></thead><tbody> </tbody></table>"`                                                                                                                           |
+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Values: exact value from template attribute valueYes or from template attribute valueNo.

**Attachment**

+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                                                                       Text field                                                                                  |
+===================================================================================================================================================================+
|    `<field type="attachment" name="fieldName" roleId="Uuid" placeholder="Some text" attachmentType="all | document | image | archive"></field>`                   |
+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+

AttachmentType should be one of the presented above (all, document, image, archive).
Supported document types:

1) All: pdf, docx, xlsx, txt, png, jpg, jpeg, zip;

2) Document: pdf, docx, xlsx, txt;

3) Image: png, jpg, jpeg;

4) Archive: zip.