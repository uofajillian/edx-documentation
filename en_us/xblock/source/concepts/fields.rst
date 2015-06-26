.. _XBlock Fields:

####################
XBlock Fields
####################

You use XBlock fields to store state data for your XBlock.

.. contents:: Section Contents:
 :local:
 :depth: 1

.. link to fields api doc

************************
XBlock Fields and State
************************

XBlock fields are Python attributes that store user and XBlock state as JSON
data.

You define the fields in the XBlock Python file. For example, the ``thumbs.py``
file in the XBlock SDK includes three fields.

.. include:: ../reusable/code_thumbs_fields.rst

When you initialize an XBlock field, you define three parameters.

* ``help``: A help string for the field that can be used in an application such
  as edX Studio.

* ``default``: The default value for the field.

* ``scope``:  The scope of the field.  For more information, see the next
  section.

.. _Field Scope:

***********
Field Scope
***********

Field *scope* is the relationship of the field to users and the XBlock.

You define the field scope when initializing the field in the XBlock Python
file. For example, in ``thumbs.py``, the ``voted`` field is initialized to have
the scope ``user_state``.

.. code-block:: python

    voted = Boolean(help="Has this student voted?", default=False, 
        scope=Scope.user_state)

===========
User Scope
===========

Fields can relate to users in the following ways.

* **No user**: the field data is not related to any users. For example, a field
  that contains course content is independent of users.

  .. note:: The XBlock cannot modify the value of a field that is not related
    to any users.

* **One user**: the field data is specific to a single user. For example, the
  answer to a problem is specific to the user who submitted it.

* **All users**: the field data is common for all users. For example, the total
  number of students who answer a question is the same for all users.

  .. note: 
    Field data related to all users is not the same as aggregate or query data.
    The same value is shared for all users, and you cannot associate specific
    actions to specific users.

===========
Block Scope
===========

Fields can relate to XBlocks in the following ways.

* **Block usage**: the field data is related to an instance, or usage, of the
  XBlock in a particular course.

* **Block definition**: the field data is related to the definition of the
  XBlock. The definition is specified by the content creator. A definition can
  be shared across one or more uses. For example, you could create a single
  XBlock definition with many uses, and those uses can appear across
  courses or within the same course.

* **Block type**: The field data is related to the Python type of the XBlock,
  and is shared across all instances of the XBlock in all courses. 

* **All**: The field data is related to all XBlocks, of all types. Any
  XBlock can access the field data.

  ..note:: 
    When you use the **All** scope, there is potential for name conflicts. If
    you have two fields of the same name with the scope **All** in different
    XBlocks types, both fields point to the same data. Therefore you should use
    caution when using **All**.

=================================
User and Block Scope Independence
=================================

The user and block scope of a field are independent of each other.  The field
scope you define specifies both. The following examples show different ways you
can combine user and block scope.

* A user's progress through a particular set of problems is stored in a field
  with the scope **One user** and **XBlock usage**.

* The content to display in an XBlock is stored in a field with the scope **No
  user** and **Block definition**.

* A user's preferences for a type of XBlock are stored in a field with the
  scope with **One user** and **XBlock type**.

* Information about the user, such as language or timezone, is stored in a
  field with the scope with **One user** and **All**.

=================================
Predefined Scopes
=================================

XBlock includes the following predefined scopes that you can use when
configuring fields. Each of these scopes includes the indicated user and block
scope settings.

* ``Scope.content``
  
  * **Block definition**
  * **No user**

* ``Scope.settings``
  
  * **Block usage**
  * **No user**

* ``Scope.user_state``
  
  * **Block usage**
  * **One user**

* ``Scope.preferences``
  
  * **Block type**
  * **One user**

* ``Scope.user_info``
  
  * **All blocks**
  * **One user**

* ``Scope.user_state_summary``
  
  * **Block usage**
  * **All users**

======================
Define a Custom Scope
======================

TBP

************************
Fields and Data Storage
************************

.. What is large?

Because XBlock fields are written and retrieved as single entities, you cannot
store a large amount of data in a single field.

To store very large amounts of data, you should split the data across many
smaller fields.

********************
Initializing Fields
********************

You do not use the ``init`` method with XBlocks.

XBlocks can be used in many contexts, and the ``init`` method might not work in
those contexts.

To initialize field values, use one of the following alternatives

* Use ``xblock.fields.UNIQUE_ID`` to set a default String value for the field. 

* Use a lazy property decorator, so that when a field is first accessed, a
  function is called to set the value.

* Run the logic to set the default field value in the view instead of the
  ``init`` method.

***************
Fields and OLX
***************

XBlock fields map to attributes in the XBlock Open Learning XML (OLX)
definition.

For example, you might include the fields ``href``, ``maxwidth``, and
``maxheight`` in a ``SimpleVideoBlock`` XBlock.  You configure the fields as in
the following example.

.. code-block:: python

  class SimpleVideoBlock(XBlock):
      """
      An XBlock providing oEmbed capabilities for video
      """

      href = String(help="URL of the video page at the provider", 
          default=None, scope=Scope.content)
      maxwidth = Integer(help="Maximum width of the video", default=800, 
          scope=Scope.content)
      maxheight = Integer(help="Maximum height of the video", default=450, 
          scope=Scope.content)

The ``SimpleVideoBlock`` XBlock is represented in OLX as in the following
example:

.. code-block:: xml

    <simplevideo 
        href="https://vimeo.com/46100581" 
        maxwidth="800" 
        maxheight="450" 
    />

*********************************************
Field Requirements in the edx Platform
*********************************************

See :ref:`edX LMS <EdX Learning Management System as an XBlock Runtime>` and
:ref:`edX Studio <EdX Studio as an XBlock Runtime>` for information about field
requirements in these applications.
