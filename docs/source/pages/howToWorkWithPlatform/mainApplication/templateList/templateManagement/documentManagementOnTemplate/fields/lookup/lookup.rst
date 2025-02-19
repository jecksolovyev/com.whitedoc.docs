============
Lookup field
============

This field allows you to create an automatically populating field which will return a value from a specified column of a row of parent dictionary field value.

.. hint:: This field can be added to structured and PDF documents.

How to add a lookup field to the document?
==========================================

1. To add field to the document, use one of field adding methods with field icon in the Fields tab of template editor menu

.. image:: pic_lookup/lookupTile.png
   :width: 600
   :align: center

2. Field creation form will appear, where you should set field attributes

.. image:: pic_lookup/lookupCreate.png
   :width: 600
   :align: center

3. Name - this is a name of a field
4. Placeholder - this text will be shown inside the field before it is filled in (can be left empty; field`s name will be used instead)
5. Optional - this attribute specifies if this field is mandatory to fill
6. Allow custom values - this attribute specifies if field will allow free text input besides selection from predefined values

.. note:: If dictionary has optionality or custom values attributes enabled, same attributes will also be enforced on all related lookups.

7. Search - this attribute specifies if this field should be eligible for mailbox page search
8. Document - dropdown selector of a document, where desired parent dictionary is located
9. Related to - dropdown selector of a desired parent dictionary
10. Column name - dropdown selector of a desired column in a parent dictionary

When all attributes are set, you can click Save button and field will be added. You can click field to see its properties and update them. Also you can delete the field in same menu.

.. image:: pic_lookup/lookupEdit.png
   :width: 600
   :align: center

.. hint:: If this field contains a link in the envelope, it will be rendered a standard link in the browser (blue font with an underline). You can follow this link from the right-click context menu (any role) or directly click it (only if the field is inactive).