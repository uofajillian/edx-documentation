.. _Customize myxblock.js:

#######################
Customize myxblock.js
#######################

This section describes how to modify the JavaScript file of the XBlock you
created, ``myxblock.js``, to provide the functionality in the Thumbs XBlock
example in the XBlock SDK.

In ``myxblock.js``, you will define code that manages user interaction
with the XBlock. The code is added to a :ref:`fragment <XBlock
Fragments>`. 

.. contents:: Section Contents:
 :local:
 :depth: 1 

***********************************
The Default XBlock JavaScirpt File
***********************************

When you :ref:`create a new XBlock <Create Your First XBlock>`, the default
JavaScript file is created automatically, with skeletal functionality defined.
In the ``xblock-sdk/myxblock/myxblock/static/js/source`` directory, see the
file ``myxblock.js``.

.. include:: ../reusable/code_myxblock_js.rst

The file contains JavaScript code to increment the ``count`` field that was
added by default to the XBlock. Delete this code.

********************
Add JavaScript Code
********************

You must add JavaScript code to increment the up and down votes for the XBlock.
Follow the guidelines below.

* Add the function ``MyXBlock`` to initializes the XBlock. 

  The ``MyXBlock`` function maps to the constructor in the :ref:`XBlock
  Python file <The XBlock Python File>` and provides access to its methods and
  fields.

* Add a runtime handler to the ``MyXBlock`` function.
  
  .. code-block:: javascript

    var handlerUrl = runtime.handlerUrl(element, 'vote');
  
* Add Post commands in the ``MyXBlock`` function to increase the up and
  down votes in the XBlock.

*******************************************
Check JavaScript Against the Thumbs XBlock
*******************************************

After you have defined the JavaScript code, check your work against the code in
the Thumbs XBlock.

.. include:: ../reusable/code_thumbs_javascript.rst

If necessary, make corrections to the code in your XBlock so that it
matches the code in the Thumbs XBlock.

.. note:: Do not change the main function name, ``MyXBlock``.

**********************************
Next Step
**********************************

When you have customized ``myxblock.js``, you must :ref:`customize the XBlock
CSS file<Customize myxblock.css>`.


.. include:: ../links.rst
