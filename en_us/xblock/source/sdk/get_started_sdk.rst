########################################
Getting Started with the XBlock SDK
########################################

This section describes how to get started with the XBlock SDK.

.. contents:: Section Contents:
 :local:
 :depth: 1

.. include:: ../reusable/clone_sdk.rst

.. include:: ../reusable/create_xblock.rst

.. include:: ../reusable/install_xblock.rst

.. include:: ../reusable/create_db.rst

.. include:: ../reusable/run_server.rst

**************************
Run the XBlock SDK Server
**************************

To see the web interface of the XBlock SDK, you must run the SDK server. 

In the ``xblock-sdk`` directory, run the following command to start the
server.

   .. code-block:: bash

      python manage.py runserver

Then test that the XBlock SDK is running. In a browser, go to
``http://localhost:8000``.  You should see the following page.

.. image:: ../Images/sdk_ui.png
  :alt: The XBlock SDK home page.
  :width: 400

The page shows the XBlocks installed automatically with the XBlock SDK. Note
that the page also shows the **MyXBlock** XBlock that you created in
:ref:`Create Your First XBlock`.

.. include:: ../links.rst
