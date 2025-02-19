.. _templateFields:

Template dynamic fields
=======================

+----------------------------------------------------------------------------------------------------------------------------------------------------------+
|**Text field**                                                                                                                                            |
+==========================================================================================================================================================+
|`<field type="text" name="string" placeholder="string" roleId="id" optional="boolean" search="boolean" multilines="boolean" min="intager" max="integer"/>`|
+----------------------------------------------------------------------------------------------------------------------------------------------------------+

Text field may have following attributes:

- type - define if this field is text type, mandatory attribute
- name - string, length from 1 up to 128 symbols, restricted symbols &, ", <, >, field name used to fill in on envelope, unique for document, mandatory attribute
- placeholder - field placeholder displayable on template and envelope, length from 0 up to 1024 symbols, if empty on envelope will be displayed field name, optional attribute
- roleId - id of the role who should fill field on envelope, mandatory attribute
- optional - boolean, defines if field to be filled in optionally or not on envelope, if not set default value false, optional attribute
- search - boolean, defines if field is searchable on envelope search or not, if not set default value false, optional attribute
- multilines - boolean, multiline or single line text, multiline should be textarea on UI, optional, default false, optional attribute
- min - integer, allowed values range from 0 to 1000 (if multiline applied than up to 5000), define minimal quantity of symbols has to be entered to field become valid, default value empty, optional attribute
- max - integer, allowed values range from 0 to 1000 (if multiline applied than up to 5000), define maximum quantity of symbols allowed to field to be valid, default value empty, optional attribute

+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|**Number field**                                                                                                                                                                                        |
+========================================================================================================================================================================================================+
|`<field type="number" name="string" placeholder="string" roleId="id" optional="boolean" search="boolean" formatting="boolean" trailingZeros="boolean" precision="integer" min="integer" max="integer"/>`|
+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Number field may have following attributes:

- type - define if this field is number type, mandatory attribute
- name - string, length from 1 up to 128 symbols, restricted symbols &, ", <, >, field name used to fill in on envelope, unique for document, mandatory attribute
- placeholder - field placeholder displayable on template and envelope, length from 0 up to 1024 symbols, if empty on envelope will be displayed field name, optional attribute
- roleId - id of the role who should fill field on envelope, mandatory attribute
- optional - boolean, defines if field to be filled in optionally or not on envelope, if not set default value false, optional attribute
- search - boolean, defines if field is searchable on envelope search or not, if not set default value false, optional attribute
- formatting - boolean, defines conversion of field data to on UI to local format set up in User profile, optional attribute
- trailingZeros - boolean, defines how to show decimal zeros after field completion, available only with precision value, optional attribute
- precision - integer, defines quantity of decimal numbers allowed, allowed value range from 0 to 7, default value empty, optional attribute
- min - integer, allowed values range from -999999999999999 to 999999999999999, define minimal value has to be entered to field become valid, default value empty, optional attribute
- max - integer, allowed values range from -999999999999999 to 999999999999999, define maximal value allowed in field to be valid, default value empty, optional attribute

+------------------------------------------------------------------------------------------------------------------------------------------------------------+
|**Currency field**                                                                                                                                          |
+============================================================================================================================================================+
|`<field type="money" name="string" placeholder="string" roleId="id" optional="boolean" search="boolean" formatting="boolean" min="integer" max="integer" />`|
+------------------------------------------------------------------------------------------------------------------------------------------------------------+

Currency field may have following attributes:

- type - define if this field is money type, mandatory attribute
- name - string, length from 1 up to 128 symbols, restricted symbols &, ", <, >, field name used to fill in on envelope, unique for document, mandatory attribute
- placeholder - field placeholder displayable on template and envelope, length from 0 up to 1024 symbols, if empty on envelope will be displayed field name, optional attribute
- roleId - id of the role who should fill field on envelope, mandatory attribute
- optional - boolean, defines if field to be filled in optionally or not on envelope, if not set default value false, optional attribute
- search - boolean, defines if field is searchable on envelope search or not, if not set default value false, optional attribute
- formatting - boolean, defines conversion of field data to on UI to local format set up in User profile, optional attribute
- min - integer, allowed values range from -999999999999999 to 999999999999999, define minimal value has to be entered to field become valid, default value empty, optional attribute
- max - integer, allowed values range from -999999999999999 to 999999999999999, define maximal value allowed in field to be valid, default value empty, optional attribute
- precision - 2 (always), you can not change this value and it's not necessary to define
- trailingZeros - true (always), you can not change this value and it's not necessary to define

+--------------------------------------------------------------------------------------------------------------------------------------------------------+
|**Date field**                                                                                                                                          |
+========================================================================================================================================================+
|`<field type="datetime" name="string" placeholder="string" roleId="id" optional="boolean" time="boolean" search="boolean" min="integer" max="integer"/>`|
+--------------------------------------------------------------------------------------------------------------------------------------------------------+

Date field may have following attributes:

- type - define if this field is datetime type, mandatory attribute
- name - string, length from 1 up to 128 symbols, restricted symbols &, ", <, >, field name used to fill in on envelope, unique for document, mandatory attribute
- placeholder - field placeholder displayable on template and envelope, length from 0 up to 1024 symbols, if empty on envelope will be displayed field name, optional attribute
- roleId - id of the role who should fill field on envelope, mandatory attribute
- optional - boolean, defines if field to be filled in optionally or not on envelope, if not set default value false, optional attribute
- time - boolean, defines if time value would be acceptable on envelope, optional attribute
- search - boolean, defines if field is searchable on envelope search or not, if not set default value false, optional attribute
- min - integer, allowed values range from -9999 to 9999, define minimal offset of date which can be selected on envelope (from envelope initiation date), default value empty, optional attribute
- max - integer, allowed values range from -9999 to 9999, define maximal offset of date which can be selected on envelope (from envelope initiation date), default value empty, optional attribute

**format**: IS8601, accept both:

- 2019-12-31T23:59:59+02:00
- 2019-12-31T23:59:59Z

+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|**Dropdown field**                                                                                                                                                                                                    |
+======================================================================================================================================================================================================================+
|`<field type="dropdown" name="string" placeholder="string" roleId="id" optional="boolean" allow-custom-value="boolean" multiSelect="boolean" search="boolean"><option>string<option>...<option>string<option></field>`|
+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Dropdown field may have following attributes and values:

- type - define if this field is dropdown type, mandatory attribute
- name - string, length from 1 up to 128 symbols, restricted symbols &, ", <, >, field name used to fill in on envelope, unique for document, mandatory attribute
- placeholder - field placeholder displayable on template and envelope, length from 0 up to 1024 symbols, if empty on envelope will be displayed field name, optional attribute
- roleId - id of the role who should fill field on envelope, mandatory attribute
- optional - boolean, defines if field to be filled in optionally or not on envelope, if not set default value false, optional attribute
- allow-custom-value - boolean, defines if custom value would be acceptable on envelope, allow-custom-value and multiSelect is not possible in the same time (only one attribute can be applied), optional attribute
- multiSelect - boolean, defines if multiselect will be available on envelope, allow-custom-value and multiSelect is not possible in the same time (only one attribute can be applied), optional attribute
- search - boolean, defines if field is searchable on envelope search or not, if not set default value false, optional attribute

field options (max quantity of options 100):

- <option> value - string, min quantity 1 symbols and max quantity 50 symbols, mandatory value

+---------------------------------------------------------------------------------+
|**Choice field**                                                                 |
+=================================================================================+
|`<field type="radio" name="string" search="boolean" value="string" roleId="id"/>`|
+---------------------------------------------------------------------------------+

Choice (Radio button) field may have following attributes:

- type - define if this field is radio type, mandatory attribute
- name - string, length from 1 up to 128 symbols, restricted symbols &, ", <, >, field name used for fill in on envelope, unique for document, mandatory attribute
- value - string, length from 1 up to 128 symbols, restricted symbols &, ", <, >, field value used for fill in value on envelope, unique for group name, mandatory attribute
- search - boolean, defines if field is searchable on envelope search or not, if not set default value false, optional attribute
- roleId - id of the role who should fill field on envelope, mandatory attribute

For one group any amount of choice options can be created, but only one of them can be selected in the envelope.

+----------------------------------------------------------------------------------------+
|**Checkbox field**                                                                      |
+========================================================================================+
|`<field type="checkbox" name="string" roleId="id" search="boolean" optional="boolean"/>`|
+----------------------------------------------------------------------------------------+

Checkbox field may have following attributes:

- type - define if this field is checkbox type, mandatory attribute
- name - string, length from 1 up to 128 symbols, restricted symbols &, ", <, >, field name used to fill in on envelope, unique for document, mandatory attribute
- roleId - id of the role who should fill field on envelope, mandatory attribute
- search - boolean, defines if field is searchable on envelope search or not, if not set default value false, optional attribute
- optional - boolean, defines if field to be filled in optionally or not on envelope, if not set default value false, optional attribute

+---------------------------------------------------------------------------------------------------------------------------+
|**File field**                                                                                                             |
+===========================================================================================================================+
|`<field type="attachment" name="string" roleId="id" placeholder="string" optional="boolean" attachmentType="enum"></field>`|
+---------------------------------------------------------------------------------------------------------------------------+

File field may have following attributes:

- type - define if this field is attachment type, mandatory attribute
- name - string, length from 1 up to 128 symbols, restricted symbols &, ", <, >, field name used to fill in on envelope, unique for document, mandatory attribute
- roleId - id of the role who should fill field on envelope, mandatory attribute
- placeholder - string, field placeholder displayable on template and envelope, length from 0 up to 1024 symbols, if empty on envelope will be displayed field name, optional attribute
- optional - boolean, defines if field to be filled in optionally or not on envelope, if not set default value false, optional attribute
- attachmentType - enum, one of the values [all, file, document, image, archive], defines file types could be uploaded on envelope, mandatory attribute

Supported document types:

1) all: .pdf, .doc, .docx, .xls, .xlsx, .xlsm, .xml, .dbf, .txt, .rtf, .csv, .xps, .eml, .msg, .emlx, .rpmsg, .png, .jpg, .jpeg, .tiff, .tif, .zip, .7z, .rar
2) file: .pdf, .doc, .docx, .xls, .xlsx, .xlsm, .xml, .dbf, .txt, .rtf, .csv, .xps, .eml, .msg, .emlx, .rpmsg
3) document: .pdf
4) image: .png, .jpg, .jpeg, .tiff, .tif
5) archive: .zip, .7z, .rar

+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|**Dictionary field**                                                                                                                                                                                            |
+================================================================================================================================================================================================================+
|`<field type="select-dictionary" name="string" placeholder="string" roleId="id" optional="boolean" allow-custom-value="boolean" search="boolean" dictionaryUuid="UUID" columnUuid="UUID" filterQuery="string"/>`|
+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Dictionary field may have following attributes:

- type - define if this field is select-dictionary type, mandatory attribute
- name - string, length from 1 up to 128 symbols, restricted symbols &, ", <, >, field name used to fill in on envelope, unique for document, mandatory attribute
- placeholder - field placeholder displayable on template and envelope, length from 0 up to 1024 symbols, if empty on envelope will be displayed field name, optional attribute
- roleId - id of the role who should fill field on envelope, mandatory attribute
- optional - boolean, defines if field to be filled in optionally or not on envelope, if not set default value false, optional attribute
- allow-custom-value - boolean, defines if custom value would be acceptable on envelope, optional attribute
- search - boolean, defines if field is searchable on envelope search or not, if not set default value false, optional attribute
- dictionaryUuid - UUID of dictionary, mandatory attribute
- columnUuid - UUID of dictionary column, which value should be taken as text value, mandatory attribute
- filterQuery - string, defines filtered query for dictionary values will be available to chose on envelope, mandatory if dictionary has filtered attribute

**Dictionary filter query example**:

\"{"dictionaryColumnUUID":{"documentId":"Id","fieldName":"string"}}\"

- dictionaryColumnUUID - UUID of dictionary column, column UUID by which dictionary values will be filtered
- documentId - id, document id where field by which value data in envelope will be filtered
- fieldName - string, name of the field by which value data in envelope will be filtered

\"{"dictionaryColumnUUID":{"roleId":"Id"}}\"

- dictionaryColumnUUID - UUID of dictionary column, column UUID by which dictionary values will be filtered
- roleId - id, id of the role by which value data in envelope will be filtered

+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|**Lookup field**                                                                                                                                                     |
+=====================================================================================================================================================================+
|`<lookup name="string" placeholder="string" optional="boolean" allow-custom-value="boolean" search="boolean" documentId="Id" relatedTo="string" columnUuid="UUID" />`|
+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Lookup field may have following attributes:

- name - string, length from 1 up to 128 symbols, restricted symbols &, ", <, >, field name used to fill in on envelope, unique for document, mandatory attribute
- placeholder - field placeholder displayable on template and envelope, length from 0 up to 1024 symbols, if empty on envelope will be displayed field name, optional attribute
- optional - boolean, defines if field to be filled in optionally or not on envelope, if not set default value false, optional attribute
- allow-custom-value - boolean, defines if custom value would be acceptable on envelope, optional attribute
- search - boolean, defines if field is searchable on envelope search or not, if not set default value false, optional attribute
- documentId - id, document id where dictionary field which will be looked up is located, mandatory attribute
- relatedTo - string, name of dictionary to which lookup will be connected, mandatory attribute
- columnUuid - UUID of dictionary column, which value should be taken as text value, mandatory attribute

+----------------------------------------------------------------------------------------------------------+
|**Dynamic table**                                                                                         |
+==========================================================================================================+
|`<table class="table-stripped" name="string" autoNumbering="boolean" iterable="true" roleId="id"></table>`|
+----------------------------------------------------------------------------------------------------------+

Dynamic table field may have following attributes:

- class - define if it's dynamic table table-stripped
- name - string, length from 1 up to 128 symbols, restricted symbols &, ", <, >, field name used to fill in on envelope, unique for document, mandatory attribute
- roleId - id of the role who should fill field on envelope, mandatory attribute
- autoNumbering - boolean, defines if rows would be numbered, default value false if not set, optional attribute
- iterable - should be true

Below you can find example of dynamic table with field inside:

.. code-block:: xml

    <div class="editor-table-field-wrapper">
        <table class="table-stripped" name="string" roleId="id" autoNumbering="boolean" iterable="true">
            <colgroup>
                <col width="325.5px"/>
                <col width="325.5px"/>
            </colgroup>
            <thead>
                <tr>
                    <th>
                        <div class="editor-div">Column name</div>
                    </th>
                    <th>
                        <div class="editor-div">Column name</div>
                    </th>
                </tr>
            </thead>
            <tbody>
                <tr iterable="true" name="*">
                    <td>
                        <div class="editor-div">
                            <field type="text" name="string" roleId=\"id\"/>
                            <br/>
                        </div>
                    </td>
                    <td>
                        <div class="editor-div">
                            <br/>
                        </div>
                    </td>
                </tr>
            </tbody>
        </table>
    </div>

+--------------------------------------------------------------------------------+
|**Duplicate field**                                                             |
+================================================================================+
|`<duplicate name="string" documentId="id" relatedTo="string" search="boolean"/>`|
+--------------------------------------------------------------------------------+

Duplicate is read-only field with the value of the related field. Duplicate field may have following attributes:

- name - string, length from 1 up to 128 symbols, restricted symbols &, ", <, >, field name used to fill in on envelope, unique for document, mandatory attribute
- documentId - id, document id where field which should be duplicated is located, mandatory attribute
- relatedTo - string, name of the field to which duplicate will be connected, mandatory attribute
- search - boolean, defines if field is searchable on envelope search or not, if not set default value false, optional attribute

+-----------------------------------------------------------------------------------------------------------------------------------------------+
|**Formula field**                                                                                                                              |
+===============================================================================================================================================+
|`<formula name="string" placeholder="string" search="boolean" precision="integer" formatting="boolean" trailingZeros="boolean">value</formula>`|
+-----------------------------------------------------------------------------------------------------------------------------------------------+

Formula is read-only field with the value calculated using EXCEL operations. Formula field may have following attributes:

- name - string, length from 1 up to 128 symbols, restricted symbols &, ", <, >, field name used to fill in on envelope, unique for document, mandatory attribute
- placeholder - field placeholder displayable on template and envelope, length from 0 up to 1024 symbols, if empty on envelope will be displayed field name, optional attribute
- search - boolean, defines if field is searchable on envelope search or not, if not set default value false, optional attribute
- precision - integer, defines quantity of decimal numbers allowed, allowed value range from 0 to 7, default value 2, optional attribute
- formatting - boolean, defines conversion of field data to on UI to local format set up in User profile, optional attribute
- trailingZeros - boolean, defines how to show decimal zeros after field completion, available only with precision value, optional attribute
- value is a formula with only one operation

SUPPORTED OPERATIONS: SUM, PRODUCT, SUBTRACT, DIVIDE, COUNTA, MAX, MIN

Example 1: SUM({field1},{doc2::field2}) where

- {field1} is a value of field1 from the same document
- {doc2::field2} is a value of field2 in document with id 'doc2'

Example 2: formula SUM({field1}) next to dynamic table where

- {field1} ia a field name from the table
- all values from all rows will summed up

+---------------------------------------------------------------------------------------+
|**Autonumber field**                                                                   |
+=======================================================================================+
|`<field type="autonumber" name="String" roleId="id" prefix="string" search="boolean"/>`|
+---------------------------------------------------------------------------------------+

Autonumber is read-only field with the value incrementally generated on each new envelope draft with current template version UUID. Autonumber field may have following attributes:

- type - define if this field is autonumber type, mandatory attribute
- name - string, length from 1 up to 128 symbols, restricted symbols &, ", <, >, field name used to fill in on envelope, unique for document, mandatory attribute
- roleId - id of the role who should fill field on envelope, mandatory attribute
- prefix - string, length from 0 up to 15 symbols, static data which will be used before incremental variable of auto numbering, option attribute
- search - boolean, defines if field is searchable on envelope search or not, if not set default value false, optional attribute

+-------------------------------------------------------------------------+
|**Signature field**                                                      |
+=========================================================================+
|`<field type="einksign" name="string" placeholder="string" roleId="id"/>`|
+-------------------------------------------------------------------------+

Field value size limited up to 10kb. Field value - base64 encoded png image, size up to 300x300. Signature field may have following attributes:

- type - define if this field is einksign type, mandatory attribute
- name - string, length from 1 up to 128 symbols, restricted symbols &, ", <, >, field name used to fill in on envelope, unique for document, mandatory attribute
- placeholder - field placeholder displayable on template and envelope, length from 0 up to 1024 symbols, if empty on envelope will be displayed field name, optional attribute
- roleId - id of the role who should fill field on envelope, mandatory attribute

PDF fields on template
======================

You can use almost all fields above with uploaded PDF. List of allowed fields: text, number, currency, date, dropdown, choice, checkbox, dictionary, lookup, duplicate, formula, autonumber, signature.

It is necessary to send additional attributes like coordinates, dimension and the page for such fields:

.. code-block:: xml

    <field x="69.05625" y="257.61597" width="30.69167" height="7.9375" page="0">