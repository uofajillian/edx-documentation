.. _The XBlock HTML File:

#######################
The XBlock HTML File
#######################

This section of the tutorial walks through the HTML file, `thumbs.html`_,  that
is part of the Thumbs XBlock in the XBlock SDK.

In the XBlock HTML file, you define the HTML content that is added to a
:ref:`fragment <XBlock Fragments>`. The HTML content can reference the XBlock
:ref:`fields <XBlock Fields>`. The fragment is returned by the :ref:`view
method <View Methods>`, to be displayed by the :ref:`runtime <XBlock
Runtimes>` application.

.. include:: ../reusable/code_thumbs_html.rst

Note the following details about the HTML file.

* The ``class`` values reference styles in the ``thumbs.css`` file. For more
  information, see :ref:`The XBlock Stylesheets`.

* The values ``self.upvotes`` and ``self.downvotes`` reference the fields in
  the XBlock Python class that have the scope ``Scope.user_state_summary``.
  This indicates that the data in these fields are specific to the XBlock and
  are the same for all users. For more information, see :ref:`The XBlock Python
  File`.

.. include:: ../links.rst
