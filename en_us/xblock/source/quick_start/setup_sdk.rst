.. _Set up the XBlock SDK:

###########################################
Set up the XBlock Software Development Kit
###########################################

Before continuing, ensure you have reviewed the 
:ref:`XBlock development requirements <XBlock Development Requirements>`.

The first step in building your XBlock is to set up the `XBlock SDK`_ in a
virtual environment. 

Complete the following tasks:

#. `Create and Activate the Virtual Environment`_.
#. `Clone XBlock Software Development Kit`_

********************************************
Create and Activate the Virtual Environment
********************************************

The first step is to create the virtual environment in which you will develop
your XBlock. You complete these steps in the command prompt.

#. Go to the directory where you will develop your XBlock.

#. In the command prompt, create the virtual environment.
   
   .. code-block:: bash

      virtualenv my_xblock_development

#. When the virtual environment is created, go to the ``my_xblock_development``
   directory in the command prompt.

   .. code-block:: bash

      cd my_xblock_development

#. Activate the virtual environment.

   .. code-block:: bash
  
      source bin/activate

   When the virtual environment is activated, the command prompt changes to
   show the name of the virtual directory in parentheses.

   .. code-block:: bash
     
      (my_xblock_development)My Computer:my_xblock_development my_username:


********************************************
Clone XBlock Software Development Kit
********************************************

When you have created and activated the virtual environment, you then clone the
the `XBlock SDK`_. You complete these steps in the command prompt.

#. In the ``my_xblock_development`` directory, with the virtual environment
   activated, clone the XBlock SDK repository from GitHub.

   .. code-block:: bash

      git clone https://github.com/edx/xblock-sdk.git

#. When the XBlock SDK is cloned, go to the ``xblock-sdk`` directory in the
   virtual environment.

   .. code-block:: bash

      cd xblock-sdk

#. Install the XBlock SDK requirements.

   .. code-block:: bash
  
      pip install -r requirements.txt

When the requirements are installed, you are then ready to create your first
XBlock.


.. include:: ../links.rst
