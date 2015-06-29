.. _Content Libraries:

##############################
Working with Content Libraries 
##############################

.. _Content Libraries Overview:

**************************
Content Libraries Overview
**************************

In Studio, you can create a library to build a pool of components for use in
randomized assignments in your courses. You can add HTML components, problems,
and video components to a library. Peer assessment and discussion components
are not supported in libraries.

.. note:: Content libraries are available only for courses that have course
   identifiers in this format: ``{key type}:{org}+{course}+{run}``. For example,
   ``course-v1:edX+DemoX+Demo_2015``. Your course identifier appears in the
   browser address bar as the final part of the URL when you open your course in
   Studio. For more details, see :ref:`Create a New Course`.

After creating a library and adding components to it, if you have :ref:`enabled
content libraries<Enable Content Libraries>` in your course, you can use these
library components in randomized assignments in your course. You do this by
adding a randomized content block to a course unit and specifying the name of
the library from which the randomized content is to drawn. You also specify the
number and type of problems that each student is assigned.

Libraries have separate users and levels of access from courses. Initially, only
the person who created the library has access. She can add other users to the
library. For details, see :ref:`Give Other Users Access to Your Library`. The
libraries that you create or have access to are listed on the **Libraries** tab
on the Studio Home page.

See the following sections for details about creating and managing content
libraries.

* :ref:`Enable Content Libraries`
* :ref:`Create a New Library`
* :ref:`Add Components to a Library`
* :ref:`View the Contents of a Library`
* :ref:`Edit Components in a Library`
* :ref:`Import a Library`
* :ref:`Export a Library`

See the following sections for details about using content library components in
a course.

* :ref:`Use Components from Libraries in a Course`
* :ref:`Add a Randomized Content Block to Your Course`
* :ref:`View the Matching Components in a Randomized Content Block`
* :ref:`Edit Components in Randomized Content Blocks`
* :ref:`Get the Latest Version of Library Content`


.. _Create a New Library:

********************
Create a New Library
********************

Use :ref:`content libraries<Content Libraries>` to build a pool of components
that can be used in randomized assignments in your courses. 

To create a new library, follow these steps.

#. Log in to Studio. 
   
#. Click **New Library**. 
#. Enter the required information for your new library, then click **Create**.

   .. note:: Enter new library information carefully. The values in these
      fields become part of the URL for your library, therefore the total number
      of characters in the **Library Name**, **Organization**, and **Library
      Code** fields must be 65 or fewer.

   .. image:: ../../../shared/building_and_running_chapters/Images/ContentLibrary_NewCL.png
      :alt: Image of the library creation page


  * For **Library Name**, enter the public display name for your library. Choose
    a meaningful name that will help you and other course team members to
    identify the library. For example, "Level 200 Math Problems". When you add a
    randomized content block to a course unit, you use the library name to
    specify this library as a source for the randomized assignment.

  * For **Organization**, enter the identifier for your university. For
    example, enter HarvardX or MITx. Do not include spaces or special
    characters.

  * For **Library Code**, enter an identifier for your library that is unique
    within your organization. This code becomes part of the URL for your
    library, so do not include spaces or special characters in the code.


4. Click **Create**.

You see the new library, to which you can now add components. For details about
adding components to a library, see :ref:`Add Components to a Library`.


.. _Edit a Library:

**************
Edit a Library
**************

After you create a library, the only change you can make to the initial library
information is to the name. However, at any time, you can make changes to the
components in your library, including adding or deleting components or editing
the settings of components. For details about editing the contents of a library,
see :ref:`Edit Components in a Library` and :ref:`Add Components to a Library`.


To change the name of a library, follow these steps.

#. Log in to Studio.
#. Click **Libraries**, then click the library whose name you want to edit.
   
#. Click the **Edit** icon next to the library name.
   
   The library name field becomes editable.
   
  .. image:: ../../../shared/building_and_running_chapters/Images/ContentLibrary_EditName.png
     :alt: The Edit icon to the right of the Library Name

4.  In the library name field, make edits or enter a new library name.
#. Click anywhere outside the library name field to save your changes.


For details about giving other users access to the library, see :ref:`Give Other
Users Access to Your Library`.


.. _Add Components to a Library:

****************************
Add Components to a Library
****************************

To add new :ref:`components<Developing Course Components>` to your library,
follow these steps.

#. Log in to Studio.
#. Click **Libraries**, then click the library that you want to add components to.

#. Click **Add Component**, then click the component type that you want to add
   under **Add New Component**.

For more information about the types of components you can add to a library, see
these topics.

* :ref:`Working with HTML Components`
* :ref:`Working with Problem Components`
* :ref:`Working with Video Components`

After you add a component to a library, you can edit its settings. These
settings are retained when the component is selected from the library and used
in a course.

When a component from the library is used in a randomized content block, you can
further edit the component as it exists in the unit, without affecting the
original version in the library. For details, refer to :ref:`Edit Components in
a Library` and :ref:`Get the Latest Version of Library Content`.


.. _View the Contents of a Library:

******************************
View the Contents of a Library
******************************

To view the entire contents of a library in Studio, follow these steps.

#. Log in to Studio.
#. Click **Libraries**, then click the library whose components you want to
   view.
#. Optionally, click **Hide Previews** at the top right of the library page to
   collapse the component previews and see only the list of component display
   names. To return to the full preview of components in the library, click
   **Show Previews**.

The components in the library display in the order in which they were added,
with the most recently added at the bottom. If your library has more than 10
components, additional components are shown on other pages.

The range of the components shown on the current page, and the total number of
components, are shown at the top of the page.

You can navigate through the pages in these ways:

* Use the **<** and **>** buttons at the top and bottom of the list to navigate
  to the previous and next pages.

* At the bottom of the page, you can edit the first number in the page range.
  Click the number to place your cursor in the field, then enter the page number
  you want to jump to.

  .. image:: ../../../shared/building_and_running_chapters/Images/file_pagination.png
     :alt: Image showing a pair of page numbers with the first number circled

To view the list of matching components in the library, see :ref:`View the Matching Components in a Randomized Content Block`.

To view the randomized content as a student would see it, see :ref:`View the
Randomized Content as a Student`.


.. _Edit Components in a Library:

****************************
Edit Components in a Library
****************************

After you have added components to a library, you can edit, duplicate, or delete
them.

For step-by-step instructions for editing, duplicating, or deleting components,
refer to the following topics.

* :ref:`Edit a Component`
* :ref:`Duplicate a Component`
* :ref:`Delete a Component`

.. note:: If you modify components in your library that are in use in a course,
   these updates in the "source" library are not reflected in the course unless
   you manually update the randomized content block in the course unit. For
   details about updating library components used in your course to match the
   latest version in the library, see :ref:`Get the Latest Version of Library
   Content`.


.. _Delete a Library:

*****************
Delete a Library
*****************

You cannot delete a library. Instead, you can discontinue use of an unwanted
library. To do so, first make sure that none of its components are in use in any
courses, then delete all components in the library. You can also :ref:`edit the
name of the library<Edit a Library>` to make it clear to other course staff that
the library should not be used as a source of randomized assignment content in
courses.

For details about deleting components in a library, see :ref:`Edit Components in
a Library`.



.. _Exporting and Importing a Library:

*********************************
Exporting and Importing a Library
*********************************

You can :ref:`export<Export a Library>` and :ref:`import<Import a Library>` a
content library in Studio.

.. _Export a Library:

================
Export a Library
================

There are several reasons why you might want to export your library.

* To save your work in progress
* To edit the XML in your library directly
* To create a backup copy of your library
* To share with another course team member

When you export your library, Studio creates a **.tar.gz** file (that is, a .tar
file compressed using GNU Zip). This export file contains the problems in the
library, including any customizations you made in the library to problem
settings. The export does not include library settings such as user access
permissions.

To export a library, follow these steps.

#. In Studio, select the **Libraries** tab.
#. Locate the library that you want to export.
#. From the **Tools** menu, select **Export**.
#. Click **Export Library Content** and specify where you want the file to be saved.

When the export process finishes, you can access the .tar.gz file on your
computer.


.. _Import a Library:

================
Import a Library
================

You might want to import a library if you developed or updated library content
outside of Studio, or if you want to overwrite a problematic or outdated version
of the library.

.. warning:: When you import a library, the imported library completely replaces
   the existing library and its contents. You cannot undo a library import.
   Before you proceed, we recommend that you export the current library, so that
   you have a backup copy of it.

The library file that you import must be a .tar.gz file (that is, a .tar file
compressed using GNU Zip). This .tar.gz file must contain a library.xml file.

To import a library, follow these steps.

#. In Studio, select the **Libraries** tab. 
   
#. Locate the library to which you want to import the new library content.
    
#. From the **Tools** menu, select **Import**.
   
#. Click **Choose a File to Import** and select the .tar.gz file that you want
   to import.

#. Click **Replace my library with the selected file**.
   
.. warning:: The import process has five stages. During the first two stages
   (Uploading and Unpacking), do not navigate away from the **Library Import** page.
   Doing so causes the import process to end. You can leave the page only after
   the Unpacking stage completes. We recommend that you do not make important
   changes to the library until all stages of the import process have finished.

6. When the import process finishes, click **View Updated Library** to view the
   imported library.

.. note:: If your imported library includes changes to components that are in
   use in a course, the course does not reflect these library updates until you
   manually update the randomized content block in the course unit. For details
   about updating library components used in your course to match the latest
   version in the content library, see :ref:`Get the Latest Version of Library
   Content`.
   