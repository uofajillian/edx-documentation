.. _Customize myxblock.py:

#######################
Customize myxblock.py
#######################

This section describes how to modify the Python file of the XBlock you created,
``myxblock.py``, to provide the functionality in the Thumbs XBlock example in
the XBlock SDK.

In ``myxblock.py``, you will define :ref:`fields <XBlock Fields>`,
:ref:`views <View Methods>`, :ref:`handlers <Handler Methods>`, and workbench
scenarios.

.. contents:: Section Contents:
 :local:
 :depth: 1 

*******************************
The Default XBlock Python File
*******************************

When you :ref:`create a new XBlock <Create Your First XBlock>`, the default
Python file is created automatically, with skeletal functionality defined. In
the ``xblock-sdk/myxblock/myxblock/`` directory, see the file ``myxblock.py``.

.. include:: ../reusable/code_myxblock_python.rst

********************
Add Comments
********************

As a best practice and because XBlocks can be shared, you must add comments to
the ``myxblock.py`` file. Provide a description of what the XBlock does and any
details future developers or users would want to know.

********************
Add XBlock Fields
********************

You need to add three fields to the XBlock, each with the right :ref:`scope
<Field Scope>`.

* ``upvotes``, to store the number of times users up-vote the XBlock. The value
  applies to the XBlock and all users.

* ``downvotes``, to store the number of times users down-vote the XBlock. The
  value applies to the XBlock and all users.

* ``voted``, to record whether or not the user has voted. The value applies to
  the XBlock and each user.

Review the :ref:`XBlock Fields` section, then add the required fields to
``myxblock.py``. You can remove the ``count`` field, which was defined
automatically when you created the XBlock.

=======================================
Check Fields Against the Thumbs XBlock
=======================================

After you have defined the fields, check your work agains the fields in the
Thumbs XBlock.

.. include:: ../reusable/code_thumbs_fields.rst

If necessary, make corrections to the fields in your XBlock so that they match
the fields in the Thumbs XBlock.

Note the following details.

* ``upvotes`` and ``downvotes`` have the scope ``Scope.user_state_summary``.
  This indicates that the data in these fields are specific to the XBlock and
  the same for all users.

* ``voted`` has the scope ``Scope.user_state``. This indicates that the data in
  this field applies to the XBlock and to the specific user. 

**************************
Define the Student View
**************************

THe XBlock Python file must contain one or more :ref:`view methods<View
Methods>`. For the Thumbs XBlock, you must include a student view.

In ``myxblock.py``, examine the ``student_view`` method that was defined
automatically when you created the XBlock.

The student view composes and returns the :ref:`fragment <XBlock Fragments>`
from static HTML, JavaScript, and CSS files. That fragment is displayed to
students in a web page.

Note the following details about student view.

* The static HTML is added when the fragment is initialized.

  .. code-block:: python

     html = self.resource_string("static/html/myxblock.html")
     frag = Fragment(unicode(html_str).format(self=self))

*  The JavaScript and CSS files are added to the fragment with the
   ``add_javascript()`` and ``add_css`` methods.

* The JavaScript in the fragment must be initialized using the name of the
  XBlock class. The name also maps to the function that initializes the XBlock
  in the :ref:`JavaScript file <The XBlock JavaScript File>`.

  .. code-block:: python

     frag.initialize_js('MyXBlock')

It appears that the necessary functions of the view were added automatically.
Check the student view in ``myxblock.py`` against the student view in
`thumbs.py`_. Note that the only differences are the file names of the HTML,
CSS, and JavaScript files added to the fragment. As the file names are correct
for MyXBlock, you do not need to edit the student view at all.

**************************
Define the Vote Handler
**************************

Your XBlock must process votes from users, and you must add this logic in
the vote :ref:`handler <Handler Methods>`.

Define a handler method named ``vote`` in the ``MyXBlock`` class that processes
user votes. The method must perform the following functions.

* Update ``upvotes`` or ``downvotes`` fields based on the user's vote.

* Set the ``voted`` field to ``True`` for the user.
  
* Return the updated ``upvotes`` and ``downvotes`` fields.

Review the :ref:`XBlock Methods` section, then implement the ``vote`` handler
in ``myxblock.py``. You can remove the ``increment_count`` method, which was
defined automatically when you create a new XBlock.

============================================
Check the Handler Against the Thumbs XBlock
============================================

After you have defined the ``vote`` method, check your work against the handler
in the Thumbs XBlock.

.. include:: ../reusable/code_thumbs_vote_handler.rst

If necessary, make corrections to the handler in your XBlock so that it matches
the handler in the Thumbs XBlock.
  
**********************************
Next Step
**********************************

When you have customized ``myxblock.py``, you must :ref:` customize the XBlock HTML file<Customize myxblock.html>`.


.. include:: ../links.rst
