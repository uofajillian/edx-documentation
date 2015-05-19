******************
Create an XBlock
******************

You use the XBlock SDK to create skeleton files for an XBlock. To do this,
follow these steps at a command prompt.

#. In the ``my_xblock_development/xblock-sdk`` directory, make sure that the
   the virtual environment is activated, and then run the following command to
   create the skeleton files for the XBlock.
   
   .. code-block:: bash

      script/startnew.py

   After you run this command, instructions in the command window instruct you
   to determine a short name and a class name. Follow the guidelines in the
   command window to determine the names that you want to use.

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

#. At the command prompt, enter the names you selected for your XBlock when you
   receive the Short name and Class name prompts.

   .. code-block:: bash
  
      Short name: myxblock
      Class name: MyXBlock

The skeleton files for the XBlock are created in the ``myxblock`` directory in
the ``XBlock SDK`` directory.

.. LIST FILES

