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

The page shows the XBlocks installed automatically with the XBlock SDK.
