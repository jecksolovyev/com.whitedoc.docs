==================
Template list page
==================

What is a template list page
============================

Template list page is the library of the templates created by mailboxes. 

1. When navigating to the templates page, the "My Templates" category of the current mailbox will be opened by default. The page will display all existing templates as well as folders (if any exist within this category)

.. image:: pic_templateListPage/myTemplatesCategoryPage.png
   :width: 300
   :align: center

2. In addition, there are four other categories accessible via the menu on the left side of the page. Each category allows users to create folders and subfolders, which are displayed in an expandable tree structure

.. image:: pic_templateListPage/categories.png
   :width: 300
   :align: center

3. In the "Account templates" category, all templates with "Account" access level will be displayed

In the "Official templates" category, all templates with "Official" access level will be displayed.
In the "Shared with you" category, all templates that have been explicitly shared with the current mailbox will be displayed.
In the "Community templates" category, it is possible to find templates with "Public" access via search.

4. Each folder can be renamed, deleted, or moved to any other existing folder or to a newly created folder

.. image:: pic_templateListPage/categoryFolderMenu.png
   :width: 300
   :align: center

How template looks like
=======================

Template is the rectangle tile on the template list page with template name, access level and creation date below tile. Each template has preview for better user experience within searching or choosing template to use. There are three types of template preview available:

1. Default image of the template. If template contains only external documents inside system can't use them as preview, so in this case preview of template would be default icon of template

.. image:: pic_templateListPage/previewExternalDocument.png
   :width: 300
   :align: center

2. First page of the document. Template with at least one structured document inside has preview, as preview of the document system takes first page of the first structured document in template

.. image:: pic_templateListPage/previewStructuredDocument.png
   :width: 300
   :align: center

3. Custom image of the template. User is able to upload custom image for template preview. How to do that described in :ref:`respective section <templatePropertyTemplate>`

4. Each template has its own menu that allows the following actions:
- Edit the template
- Copy the template UUID
- Clone the template
- Move the template to another category/folder
- Rename the template
- Delete the template
- Get a direct link to the template

.. image:: pic_templateListPage/templateMenu.png
   :width: 300
   :align: center

How to find a template
======================

1. The template search functions within each category separately. Templates can be searched by either their name or UUID. If you're looking for a specific template you created in your mailbox, you should perform the search within the "My templates" category. This applies to all other categories as well

.. image:: pic_templateListPage/searchMyTemplates.png
   :width: 400
   :align: center

2. To find a template with the "Public" access level, navigate to the "Community templates" category

.. note:: Please note that, depending on the template's access settings, it may be found by name, by UUID, or only by UUID. You can read more about template access settings :ref:`here <templateAccessLevel>`.

.. image:: pic_templateListPage/searchCommunityTemplates.png
   :width: 400
   :align: center

On template list you can create templates, clone, update and delete existing templates.