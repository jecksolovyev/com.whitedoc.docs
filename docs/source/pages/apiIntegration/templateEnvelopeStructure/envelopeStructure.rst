==================
Envelope Structure
==================

Envelope data block below contains all fields which can be added to document body.

.. code::

    <envelope templateUuid="1997a1b4-88e3-4f58-88ca-fcd2c6fb5869" templateVersion="4a303734-a118-44a2-aedf-67df61612628">
	    <info>
		    <subject>all fields envelope</subject>
		    <message/>
		    <forwarding delegation="true" sharing="true"/>
	    </info>
	    <flow>
		    <roles>
			    <role id="74266bb8-91ad-4e35-9d98-5862fc59cf3e" mailboxUuid="8dcde243-a918-444a-ac7d-44ac88554769"/>
			    <role id="a09d90c7-46c1-4f59-8d76-e7975dd8fab6" mailboxUuid="8dcde243-a918-444a-ac7d-44ac88554769"/>
		    </roles>
	    </flow>
	    <documents>
		    <document id="16c545db-1002-4efb-a4de-b46bc5ed4885">
			    <field name="Text 1">text</field>
			    <field name="Duplicate 1">text</field>
			    <field name="Number 1">10</field>
			    <field name="Currency 1">10.20</field>
			    <field name="Date and time 1">2024-01-11</field>
			    <field name="Dictionary 1" recordUuid="76d0b4a4-114f-45a6-9039-d654c90a2df2">one 2</field>
			    <field name="Signature 1">data:image/png;base64,iVBORw...K5CYII=</field>
			    <field name="File 1" attachmentUuid="dc317260-adf3-4231-8eaa-588759d7b6f7">Screenshot 2024-01-11 at 11.22.54.png</field>
			    <field name="A B 1">A</field>
			    <field name="Lookup 1">two 2</field>
			    <field name="Checkbox 1">1</field>
			    <field name="Dropdown 1">2</field>
			    <field name="1234">Choice 1</field>
			    <fieldgroup name="Table 1">
				    <fieldset index="0">
					    <field name="Text 2">1</field>
				    </fieldset>
				    <fieldset index="1">
					    <field name="Text 2">2</field>
				    </fieldset>
			    </fieldgroup>
		    </document>
	    </documents>
    </envelope>

.. csv-table::
  :file: envelopeStructureData.csv
  :widths:  10, 10

How to fill each single field
=============================

+----------------------------------------------------------------+
|**Text, Number, Currency, Date and time, A/B, Dropdown fields** |
+================================================================+
|`<field name="string">value</field>`                            |
+----------------------------------------------------------------+

- name - string, name of the field you want to fill
- value - the value of the field, all validation restrictions configurable on template, mandatory if field doesn't have optional attribute

+--------------------------------------------------+
|**Duplicate, Lookup and Autonumber fields**       |
+==================================================+
|``                                                |
+--------------------------------------------------+

You may not to send these types of fields if template contains it. It's automatically filled in fields.

+------------------------------------------------------+
|**Dictionary field**                                  |
+======================================================+
|`<field name="string" recordUuid="UUID">value</field>`|
+------------------------------------------------------+

- name - string, name of the field you want to fill
- recordUuid - UUID, record UUID from dictionary you want to chose
- value - the value of the field, all validation restrictions configurable on template, optional, but if you define value verification of recordUUID and value happen

+------------------------------------+
|**Signature field**                 |
+====================================+
|`<field name="string">value</field>`|
+------------------------------------+

- name - string, name of the field you want to fill
- value - the value of the field, value in base64 format (data:image/png;base64,iVBORw...K5CYII=), all validation restrictions configurable on template, mandatory

+------------------------------------+
|**Checkbox field**                  |
+====================================+
|`<field name="string">value</field>`|
+------------------------------------+

- name - string, name of the field you want to fill
- value - integer, value 1 to mark it checked, if you don't want to send value use optional field and skip fill in of particular one, all validation restrictions configurable on template

+------------------------------------+
|**Choice field**                    |
+====================================+
|`<field name="string">value</field>`|
+------------------------------------+

- name - string, name of the GROUP of radio buttons
- value - string, name of the field from the GROUP of radio buttons which should be marked as chosen

+------------------------------------+
|**Table field**                     |
+====================================+
|``                                  |
+------------------------------------+

.. code::
    <fieldgroup name="string">
        <fieldset index="0">
            <field name="Text 2">1</field>
        </fieldset>
        <fieldset index="1">
            <field name="Text 2">2</field>
        </fieldset>
    </fieldgroup>

- fieldgroup name - string, name of the table field
- fieldset index - integer, index of the table row (if you need more rows, just create more fieldsets)
