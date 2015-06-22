.. _XBlock Examples:

#############################
XBlock Examples
#############################

This section shows example XBlocks. These example are meant to demonstrate simple XBlocks and are not meant to show the range of capabilities.

.. contents:: Section Contents:
 :local:
 :depth: 1

*******************************
Google Drive and Calendar Tools
*******************************

You use the `Google Drive and Calendar XBlock`_ to embed Google documents and
calendars in your courseware.

As you can see, the Google Drive and Calendar XBlock is created and stored in a
separate Github repository. You can explore this XBlock to learn how it is
structured and developed.

You can follow the instructions to install the XBlock on your Open edX system.
For more information, see :ref:`Deploy an XBlock`.

================================
Adding the XBlock to Courseware
================================

When the Google Drive and Calendar XBlock is installed on the edX Platform,
course staff can add Google documents and calendards to courseware.

For example, in Studio, course staff can add and configure a Google calendar
component.

.. image:: ../Images/google-calendar-edit.png
  :alt:  The Google Calendar editor in Studio.
  :width: 600

Course staff or developers can also add a Google calendar using OLX.

.. code-block:: xml

  <google-calendar 
    url_name="4115e717366045eaae7764b2e1f25e4c"
    calendar_id="abcdefghijklmnop1234567890@group.calendar.google.com"
    default_view="1" 
    display_name="Class Schedule"
  />

For more information, see `Google Calendar Tool`_ and `Google Drive Tool`_ in
the *Building and Running an Open edX Course*.

==================
Viewing the XBlock
==================

When course staff use the Google Drive and Calendar XBlock, learners view
Google documents and calendards directly in courseware.

.. image:: ../Images/google-spreadsheet.png
  :alt:  The Google Calendar in the LMS.
  :width: 600

***********
XBlock SDK
***********

The `XBlock SDK`_ that you will use in this tutorial also contains several
example XBlocks.

You will use the `Thumbs XBlock`_ in the sections :ref:`Customize Your XBlock`
and :ref:`Anatomy of an XBlock`.

You can explore these and other example XBlocks in the XBlock SDK.

.. include:: ../links.rst
