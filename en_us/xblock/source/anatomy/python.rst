.. _The XBlock Python File:

#######################
The XBlock Python File
#######################

This section of the tutorial walks through the Python file, `thumbs.py`_, for
the Thumbs XBlock example in the XBlock SDK.

In the XBlock Python file, you define :ref:`fields <XBlock Fields>`,
:ref:`views <View Methods>`, :ref:`handlers <Handler Methods>`, and workbench
scenarios.

.. contents:: Section Contents:
 :local:
 :depth: 1 

********************
Thumb XBlock Fields
********************

The ``thumbs.py`` file defines three fields for the XBlock in the
``ThumbsBlockBase`` class.

.. include:: ../reusable/code_thumbs_fields.rst

Note the following details about the fields in the Thumbs XBlock.

* ``upvotes`` and ``downvotes`` have the scope ``Scope.user_state_summary``.
  This indicates that the data in these fields are specific to the XBlock and
  the same for all users.

* ``voted`` has the scope ``Scope.user_state``. This indicates that the data in
  this field applies to the XBlock and to the specific user.

For more information, see :ref:`XBlock Fields`.  

**************************
Thumb XBlock Student View
**************************

The ``thumbs.py`` file defines the student view for the XBlock in the
``ThumbsBlockBase`` class. 

.. include:: ../reusable/code_thumbs_student_view.rst

The student view composes and returns the fragment from static HTML,
JavaScript, and CSS files. That fragment is displayed to students in a web
page.

Note the following details about student view.

* The static HTML is added when the fragment is initialized.

  .. code-block:: python

     html_str = pkg_resources.resource_string(__name__, "static/html/thumbs.html")
     frag = Fragment(unicode(html_str).format(self=self))

*  The JavaScript and CSS files are added to the fragment with the
   ``add_javascript()`` and ``add_css`` methods.

* The JavaScript in the fragment must be initialized using the name of the
  XBlock class. The name also maps to the function that initializes the XBlock in the :ref:`JavaScript file <The XBlock JavaScript File>`.

  .. code-block:: python

     frag.initialize_js('ThumbsBlock')

For more information, see :ref:`View Methods`.

**************************
Thumb XBlock Vote Handler
**************************

The ``thumbs.py`` file defines a handler that adds a user's vote to the XBlock.

.. include:: ../reusable/code_thumbs_vote_handler.rst

Note the following details about the vote handler.

* The ``upvotes`` or ``downvotes`` fields are updated based on the user's vote.

* The ``voted`` field is set to ``True`` for the user.
  
* The updated ``upvotes`` and ``downvotes`` fields are returned.

For more information, see :ref:`Handler Methods`.

.. include:: ../links.rst
