.. _Introduction to XBlocks:

#############################
Introduction to XBlocks
#############################

XBlocks are the components that combine together to build interactive
courseware.

Like HTML ``<div>`` tags, XBlocks can represent components as small as a
paragraph of text, a video, or a multiple choice input field, or as large as a
section, a chapter, or an entire course.

.. contents:: Section Contents:
 :local:
 :depth: 1

*****************************
XBlocks and the edX Platform
*****************************

The edX Platform uses many built in XBlocks that are available to course
developers. For example, `Google Drive`_ and `Open Response Assessments`_ are
both XBlocks that are imported into the edX Platform. For more information, see
:ref:`XBlock Examples`.

EdX recognizes that the ever expanding need to provide new and innovative types
of content. The XBlock API and XBlock SDK are available for developers to
create new types of XBlocks for course teams to use.

***********************
XBlocks for Developers
***********************

Developers can extend the types of content available in the edX Platform by
creating and deploying XBlocks. EdX provides the `XBlock SDK`_ to support the
creation of new XBlocks.

This tutorial is meant to guide developers through the process of creating an
XBlock, and to explain the architecture and anatomy of XBLocks.

Developers should also see the XBlock API documentation.

=========================================
XBlock Independence and Interoperability
=========================================

An XBlock must be designed to meet two goals.

* The XBlock must be independent of other XBlocks. Course staff must be able to
  use the XBlock without it being dependent on other XBlocks.

* The XBlock must also work together with other XBlocks. Course staff must be
  able to combine different XBlocks in flexible ways.

=========================================
XBlocks Compared to Web Applications
=========================================

XBlocks are similar to web applications. XBlocks maintain state in a storage
layer, render themselves through views, and process user actions through
handlers.

XBlocks differ from web applications in that they render only a small piece of
a complete web page.

.. include:: ../links.rst