.. _Create Your First XBlock:

#########################
Create Your First XBlock
#########################

Before continuing, ensure you have completed the steps to 
:ref:`set up the XBlock SDK <Set up the XBlock SDK>`.

When you have set up the XBlock SDK, you use it to create the an XBlock. You
complete these steps in the command prompt.

#. In the ``my_xblock_development/xblock-sdk`` directory, with the virtual
   environment activated, create the XBlock.
   
   .. code-block:: bash

      script/startnew.py

   You see the following instructions in the command window.

   .. code-block:: bash

      You will be prompted for two pieces of information:

      * Short name: a single word, all lower-case, for directory and file
        names. For a hologram 3-D XBlock, you might choose "holo3d".

      * Class name: a valid Python class name.  It's best if this ends with
        "XBlock", so for our hologram XBlock, you might choose
        "Hologram3dXBlock".

      Once you specify those two words, a directory will be created in the
      current directory containing the new project.

      If you don't want to create the project here, or you enter a name
      incorrectly, just type Ctrl-C to stop this script.  If you don't want the
      resulting project, just delete the directory it created.

#. Enter the ``Short name`` of your XBlock at the prompt.

   .. code-block:: bash

      Short name: myxblock

#. Enter the ``Class name`` of your XBlock at the prompt.

   .. code-block:: bash
  
      Short name: myxblock
      Class name: MyXBlock

The skeleton files for the XBlock are created in the ``myxblock`` directory in
the ``XBlock SDK`` directory.

SCREEN SHOT

This completes the XBlock Quick Start section.  In the next sections, we will
learn about the structure of the XBlock, how to create a basic XBlock example,
and how to deploy the XBlock.

.. include:: ../links.rst
