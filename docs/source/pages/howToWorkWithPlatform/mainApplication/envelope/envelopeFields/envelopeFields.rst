===============
Envelope fields
===============

As a participant in the envelope processing workflow, you can complete the fields in the documents assigned to your role. Here, you will find several field-related hints

Text
====

A text field is used to store various types of text information, including strings, numbers, and special characters. Text field can be single line and multiline, depends on :ref:`template configuration <textFieldTemplate>` of envelope. As mentioned above, you can use any type of character as text field content, and the system will handle the necessary escaping for you. However, if you're using an API to send or fill the envelope, you must manually escape special characters.

.. note:: If your text contains one of the following special characters ", <, >, ', & and you want to send API request to fill/send envelope, wrap the content which contains special characters into <![CDATA["<content>"]]>. You can use CDATA with any type of field, text field is just as example

You may need to enter a link in the text field. Our system allows this and will display the content as a clickable link. However, there are several considerations regarding the content transferred to the link.

1. Link has to start from http:// or https://
2. Link has to contain correct domain part

.. note:: We're not making modifications to XML you've send, we just visualizing links and make them clickable. Links in correct format will be displayed in printable versions of document also as clickable links.

.. note:: Links functionality works only for text, multiline text, duplicate of text, duplicate of multiline text fields.

Some text fields may contain a prefillable value which is automatically prepopulated from the according user profile fields. Prefilled values can be edited manually. If the user who fills this field has no value saved in his user profile, it will not be prepopulated. Also, user will be prompted to save filled in data to his user profile:

.. image:: pic_envelopeFields/saveDataModal.png
   :width: 600
   :align: center

Number
======

A number field is a used to store numeric values. Precision cann be configured from 0 to 7.

Some number fields may contain a prefillable value which is automatically prepopulated from the according user profile fields. Prefilled values can be edited manually. If the user who fills this field has no value saved in his user profile, it will not be prepopulated. Also, user will be prompted to save filled in data to his user profile:

.. image:: pic_envelopeFields/saveDataModal.png
   :width: 600
   :align: center

Date
====

A date field is a used to store date (and optionally time) values.

Some date fields may contain a prefillable value which is automatically prepopulated from the according user profile fields. Prefilled values can be edited manually. If the user who fills this field has no value saved in his user profile, it will not be prepopulated. Also, user will be prompted to save filled in data to his user profile:

.. image:: pic_envelopeFields/saveDataModal.png
   :width: 600
   :align: center