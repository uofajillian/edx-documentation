.. _Set Up the XBlock Software Development Kit:

###########################################
Set Up the XBlock Software Development Kit
###########################################

Before you continue, make sure that you're familiar with the subjects in the 
:ref:`Install XBlock Prerequisites` section.

When you have installed all prerequisities, you are ready to set up the `XBlock
SDK`_ in a virtual environment. To do this, complete the following steps.

.. contents:: Section Contents:
 :local:
 :depth: 1

********************************************
Create and Activate the Virtual Environment
********************************************

The first step is to create the virtual environment where you will develop
your XBlock. You complete these steps in the command prompt.

#. Go to the directory where you will develop your XBlock.

#. At the command prompt, run the following command to create the virtual
   environment.
   
   .. code-block:: bash

      virtualenv my_xblock_development

#. When the virtual environment is created, go to the ``my_xblock_development``
   directory at the command prompt, and then run the following command.

   .. code-block:: bash

      cd my_xblock_development

#. At the command prompt in the ``my_xblock_development`` directory, run the
   following command to activate the virtual environment.

   .. code-block:: bash
  
      source bin/activate

   When the virtual environment is activated, the command prompt shows the name
   of the virtual directory in parentheses.

   .. code-block:: bash
     
      (my_xblock_development)My Computer:my_xblock_development my_username:


********************************************
Clone the XBlock Software Development Kit
********************************************

After you create and activate the virtual environment, clone the `XBlock SDK`_.
To do this, complete the following steps at a command prompt.

#. In the ``my_xblock_development`` directory, make sure that the the virtual
   environment is activated, and then run the following command to clone the
   XBlock SDK repository from GitHub.

   .. code-block:: bash

      git clone https://github.com/edx/xblock-sdk.git

#. When the XBlock SDK is cloned, run the following command to go to the
   ``xblock-sdk`` directory in the virtual environment.

   .. code-block:: bash

      cd xblock-sdk

#. From the ``xblock-sdk`` directory, run the following command to install the
   XBlock SDK requirements.

   .. code-block:: bash
  
      pip install -r requirements.txt

When the requirements are installed, you are ready to create your first XBlock.

.. include:: ../links.rst
