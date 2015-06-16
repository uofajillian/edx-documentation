.. _Customize myxblock.html:

#######################
Customize myxblock.html
#######################

This section describes how to modify the static HTML file of the XBlock you
created, ``myxblock.html``, to provide the functionality in the Thumbs XBlock
example in the XBlock SDK.

In ``myxblock.html``, you will define the HTML content that is added to a 
:ref:`fragment <XBlock Fragments>`. The HTML content can reference the XBlock
:ref:`fields <XBlock Fields>`. The fragment is returned by the :ref:`view
method <View Methods>`.

.. contents:: Section Contents:
 :local:
 :depth: 1 

*******************************
The Default XBlock HTML File
*******************************

When you :ref:`create a new XBlock <Create Your First XBlock>`, the default
static HTML file is created automatically, with skeletal functionality defined.
In the ``xblock-sdk/myxblock/myxblock/static/html`` directory, see the file
``myxblock.html``.

.. include:: ../reusable/code_myxblock_html.rst

The file contains HTML code to display the ``count`` field that was added by
default to the XBlock. Delete this code.

********************
Add HTML Content
********************

You must add HTML code to display the up and down votes for the XBlock. Create
a single paragraph and follow the guidelines below.

* Create two ``span`` elements, to display up-votes and down-votes.

* Use ``upvote`` and ``downvote`` as class values for the ``span`` elements.
  You will define these classes in ``myxblock.css``. For more information, see
  :ref:`Customize myxblock.css`.

* Within each ``span`` element, create another ``span`` element, each with the
  class value ``count``. For the value of each embedded ``span`` element,
  reference the ``upvotes`` and ``downvotes`` fields you defined in the
  :ref:Python file <Customize myxblock.py>` for the XBlock.

* For the value of each of the outer ``span`` elements, use the entities
  ``&uarr;`` and ``&darr`` to show thumbs up and thumbs down symbols next to
  the number of votes.

****************************************
Check HTML Against the Thumbs XBlock
****************************************

After you have defined the HTML code, check your work against the HTML in the
Thumbs XBlock.

.. include:: ../reusable/code_thumbs_html.rst

If necessary, make corrections to the HTML code in your XBlock so that it
matches the code in the Thumbs XBlock.

**********************************
Next Step
**********************************

When you have customized ``myxblock.html``, you must :ref:`customize the
XBlock JavaScript file<Customize myxblock.js>`.

.. include:: ../links.rst
