.. _Introduction to XBlocks:

#############################
Introduction to XBlocks
#############################

XBlock is edX's component architecture that you use to build courseware. Like
HTML ``<div>`` tags, XBlocks can represent components as small as a paragraph
of text, a video, or a multiple choice input field, or as large as a section, a
chapter, or an entire course.


XBlocks are components that combine together to create interactive course content. They need to satisfy two conflicting goals: work together with other blocks to build a complete course; and be independent of other blocks, so they can be combined flexibly.

XBlocks are built similarly to web applications. They maintain state in a storage layer, render themselves through views, and process user actions through handlers.

They differ from web applications, though, because each XBlock renders only a small piece of a complete web page.



***********************
XBlocks for Developers
***********************

Developers can extend the edX Platform by creating and deploying XBlocks. EdX provides the `XBlock SDK`_ to support the creation of new XBlocks. 

This tutorial is meant to guide developers through the process of creating an XBlock, and to explain the architecture and anatomy of XBLocks.

Developers should also see the XBlock API documentation.

*************************
XBlocks for Course Staff
*************************

To create rich, engaging online courses, course authors must be able to combine components from a variety of sources. 
