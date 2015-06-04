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

.. code-block:: python

    class ThumbsBlockBase(object):
        upvotes = Integer(help="Number of up votes", default=0, 
            scope=Scope.user_state_summary)
        downvotes = Integer(help="Number of down votes", default=0, 
            scope=Scope.user_state_summary)
        voted = Boolean(help="Has this student voted?", default=False, 
            scope=Scope.user_state)

When you initialize an XBlock field, you define three parameters.

* ``help``: A help string for the field that can be used in an applicaton such
  as edX Studio.

* ``default``: The default value for the field.
* ``scope``:  The scope of the field.  For more information, see th enext
  section.

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

* **One user**: the field data is specific to a single user. For example, the
  answer to a problem is specific to the user who submitted it.

* **All users**: the field data is common for all users. For example, the total
  number of students who answer a question is the same for all users.

  .. note: 
    Field data related to all users is not the same as aggregate or query data.
    The same value is shared for all users, and you cannot link associate
    specific actions to specific users.

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


***************
Fields and OLX
***************