==============
Dropdown field
==============

This field allows you to create a dropdown menu selector from several predefined values. You can customize default option values. Minimum of 1 option is required, up to 100 options per dropdown are allowed. It looks like a dropdown menu in the envelope. After selection it will change to regular text of selected value.

.. hint:: This field can be added to structured and PDF documents.

How to add a dropdown field to the document?
============================================

1. To add field to the document, use one of field adding methods with field icon in the Fields tab of template editor menu

.. image:: pic_dropdown/dropdownTile.png
   :width: 600
   :align: center

2. Field creation form will appear, where you should set field attributes

.. image:: pic_dropdown/dropdownCreate.png
   :width: 600
   :align: center

3. Name - this is a name of a field
4. Role name - this is a role that will be assigned to fill this field
5. Placeholder - this text will be shown inside the field before it is filled in (can be left empty; field`s name will be used instead)
6. Optional - this attribute specifies if this field is mandatory to fill
7. Search - this attribute specifies if this field should be eligible for mailbox page search
8. Option 1, 2, etc. - option available for selection. Can be deleted with 'X' button. Note that at least 1 option is mandatory and options can not be blank (min 1 max 50 characters per option)
9. Add option - allows to add new options. 100 options max are allowed per field 

This field also includes additional attributes, which you can access by clicking the "Show advanced settings" button.

.. image:: pic_dropdown/dropdownAdvancedSettings.png
   :width: 600
   :align: center

10. Tooltip - enables adding a custom tooltip that will be displayed for active fields in the envelope. If left blank, the default tooltip is shown
11. Multiselect - this attribute specifies if multiple values can be selected (can not be enabled together with Allow custom value attribute)
12. Allow custom values - this attribute specifies if field will allow free text input besides selection from predefined values (can not be enabled together with Multiselect attribute)

When all attributes are set, you can click the "Save" button and the field will be added. You can click the field to view or update its properties, and also delete it in the same menu.

Please note that the "Show advanced settings" option is available only while no additional attributes have been added to the field.
Once at least one additional attribute is added — either during creation or later in edit mode — this option will no longer appear, and all available attributes will be displayed for editing instead.

.. image:: pic_dropdown/dropdownEdit.png
   :width: 600
   :align: center

.. hint:: If this field contains a link in the envelope, it will be rendered a standard link in the browser (blue font with an underline). You can follow this link from the right-click context menu (any role) or directly click it (only if the field is inactive).