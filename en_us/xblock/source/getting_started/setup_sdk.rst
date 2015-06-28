.. _Set Up the XBlock Software Development Kit:

###########################################
Set Up the XBlock Software Development Kit
###########################################

Before you continue, make sure that you are familiar with the subjects in the 
:ref:`Install XBlock Prerequisites` section.

When you have installed all prerequisites, you are ready to set up the `XBlock
SDK`_ in a virtual environment. To do this, complete the following steps.

.. contents:: Section Contents
 :local:
 :depth: 1

.. _Create and Activate the Virtual Environment:

********************************************
Create and Activate the Virtual Environment
********************************************

The first step is to create the virtual environment where you develop your
XBlock. You complete these steps at the command prompt.

#. Open a command prompt and then change to the directory where you want to
   develop your XBlock.

#. At the command prompt, run the following command to create the virtual
   environment.
   
   .. code-block:: bash

      $ virtualenv my_xblock_development

#. When the virtual environment is created, go to the ``my_xblock_development``
   directory.

   .. code-block:: bash

      $ cd my_xblock_development

#. At the command prompt in the ``my_xblock_development`` directory, run the
   following command to activate the virtual environment.

   .. code-block:: bash
  
      $ source bin/activate

   When the virtual environment is activated, the command prompt shows the name
   of the virtual directory in parentheses.

   .. code-block:: bash
     
      (my_xblock_development)My Computer:my_xblock_development my_username$

.. include:: ../reusable/clone_sdk.rst

When the requirements are installed, you are ready to create your first XBlock.

.. include:: ../links.rst
