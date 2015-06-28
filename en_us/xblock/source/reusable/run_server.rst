**************************
Run the XBlock SDK Server
**************************

To see the web interface of the XBlock SDK, you must run the SDK server. 

In the ``xblock-sdk`` directory, run the following command to start the
server.

   .. code-block:: bash

      python manage.py runserver port

.. note:: If you do not specify a port, the XBlock SDK server uses port 8000.
  To use a different port, specify it in the ``runserver`` command.

Then test that the XBlock SDK is running. In a browser, go to
``http://localhost:port-number``.  You should see the following page.

.. image:: ../Images/sdk_ui.png
  :alt: The XBlock SDK home page.
  :width: 400

The page shows the XBlocks installed automatically with the XBlock SDK. Note
that the page also shows the **MyXBlock** XBlock that you created in
:ref:`Create Your First XBlock`.
