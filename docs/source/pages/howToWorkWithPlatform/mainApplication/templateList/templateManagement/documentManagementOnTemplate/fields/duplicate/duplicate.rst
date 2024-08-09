===============
Duplicate field
===============

This field allows you to create a static duplicate of other field. Please note that it will not be possible to delete parent field of a duplicate untill the duplicate field is removed.

.. hint:: This field can be added to structured and PDF documents.

How to add duplicate field to the document
==========================================

1. To add field to the document, use one of field adding methods with field icon in the Fields tab of template editor menu

.. image:: pic_duplicate/duplicateIcon.png
   :width: 600
   :align: center

2. Field creation form will appear, where you should set field attributes

.. image:: pic_duplicate/duplicateCreate.png
   :width: 600
   :align: center

3. Name - this is a name of a field
4. Document - document where parent field is placed
5. Duplicate of - field which will be duplicated

.. note:: If duplicate is placed inside of a dynamic table, only fields from the same table (or outside of all tables) will be available for duplication.

When all attributes are set, you can click Save button and field will be added. You can click field to see its properties and update them. Also you can delete the field in same menu.

.. image:: pic_duplicate/duplicateEdit.png
   :width: 600
   :align: center

.. hint:: If this field contains a link in the envelope, it will be rendered a standard link in the browser (blue font with an underline). You can follow this link from the right-click context menu.