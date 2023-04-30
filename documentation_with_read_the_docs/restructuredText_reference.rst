reStructuredText Reference
++++++++++++++++++++++++++

Official Documentation
======================
This section will cover the basics, for a more full description, see the `official documentation <https://www.sphinx-doc.org/en/master/contents.html>`_

TOC tree
========
The TOC tree can appear in any reStructuredText file.  For an example, you will normally find it in the `index.rst` file.  The `toctree` specifies the outline that shows in the left pane of the documentation website.  This example assumes there are files with file name some_section_1.rst, some_section_2.rst, and some_section_3.rst in the same folder where this `toctree` is defined: 

.. code-block:: restructuredtext

   .. toctree::
      :maxdepth: 2
      :caption: Contents
      
      some_section_1
      some_section_2
      some_section_3

Hidden option 
-------------
The table of contents will display on both the left pane as well as on the page where it's list.  To only display the table of contents in the left pane and hide it from the page, you can use the `:hidden` option: 

.. code-block:: restructuredtext

   .. toctree::
      :maxdepth: 2
      :caption: Contents
      :hidden: 

      some_section_1
      some_section_2
      some_section_3

Sub-folders and relative paths
------------------------------
To organize files in sub-folders, you can specify relative paths to the sections: 

.. code-block:: restructuredtext

   .. toctree::
      :maxdepth: 2
      :caption: Contents
      :hidden: 

      folder_1\some_section_1
      folder_1\some_section_2
      folder_2\some_section_3

Main Heading, Sections, and Sub-sections
========================================
Each RST file can have a main heading and any number of sections and sub-sections: 

.. code-block:: restructuredtext

   MAIN HEADING
   ++++++++++++
   This text appears under the main heading

   SECTION
   =======
   This text appears under this section 

   Sub-Section 
   -----------
   This text appears under this sub-section 
   
   Sub-sub-section 
   ~~~~~~~~~~~~~~~
   This text appears under this other sub-sub-section

Text Decorations
================

Italics
-------
To make something *italicized*, put a single asterix before and after *the text that should be italicized*.

.. code-block:: restructuredtext

   To make something *italicized*, put a single asterix before and after *the text that should be italicized*.

Bold
----
To make something **bold**, put two asterix before and after **the text that should be bold**.

.. code-block:: restructuredtext

   To make something **bold**, put two asterix before and after **the text that should be bold**.

Code words
----------
To decorate text as ``code words``, use two backticks before and after the code word, i.e. ``StringBuilder``. 

.. code-block:: restructuredtext

   To decorate text as ``code words``, use two backticks before and after the code word, i.e. ``StringBuilder``. 

Un-numbered lists
-----------------
List items are preceeded by a minus sign -

- Item 1
- Item 2
- Item 3

Example code: 

.. code-block:: restructuredtext

  - Item 1
  - Item 2
  - Item 3

Multi-level lists
-----------------
Lists can have multiple levels by indenting the sub-items.  This will make the parent item bold and the sub-item have a different type of bullet point

- Item 1
   - Sub-item 1
   - Sub-item 2
- Item 2
   - Sub-item A
   - Sub-item B
- Item 3

Example code: 

.. code-block:: restructuredtext

  - Item 1
     - Sub-item 1
     - Sub-item 2
  - Item 2
     - Sub-item A
     - Sub-item B
  - Item 3

Numbered lists
--------------
Numbered list items should be preceeded by a #.

#. Item 1
#. Item 2
#. Item 3

Example code: 

.. code-block:: restructuredtext

   #. Item 1
   #. Item 2
   #. Item 3

Admonitions
===========
Admonitions allow you to call special attention to text by putting an info, note, or warning box around the text. Note that the text that appears in the admonition box should be tabbed under the admonition as shown in the following examples.

Note
----
.. note :: 
   The note admonition looks like this.

Example code: 

.. code-block:: restructuredtext

   .. note :: 
      The note admonition looks like this.

Tip
---
.. tip :: 
   The tip admonition looks like this.

Example code: 

.. code-block:: restructuredtext

   .. tip :: 
      The tip admonition looks like this.

Caution
-------
.. caution :: 
   The caution admonition looks like this.

Example code: 

.. code-block:: restructuredtext

   .. caution :: 
      The caution admonition looks like this.

Danger
------
.. danger :: 
   The danger admonition looks like this.

Example code: 

.. code-block:: restructuredtext

   .. danger :: 
      The danger admonition looks like this.

Warning
-------
.. warning :: 
   The warning admonition looks like this.

Example code: 

.. code-block:: restructuredtext

   .. warning :: 
      The warning admonition looks like this.

Images
======
To display an image in a document, include the image file in the project and provide the relative path to the image.  To keep things organized, it's good to create an images folder in the section where your image will be displayed to house your images. To display an image, use the ``.. image pathtoimagefile.abc`` as shown below.

.. image:: images/imagesFolderWithImage.png

Example code: 

.. code-block:: restructuredtext

   .. image:: images/imagesFolderWithImage.png

Code Samples
============
To display a block of code, use ``.. code-block::`` and the text that is indented will display as a code sample.  You can include the language of the code sample to get code highlighting.  You need an extra line after the ``.. code-block::`` line and before the code sample.  Any text indented will be treated as code.

.. code-block:: csharp

   public static void DoThing(int a, string b)
   {
      // things and stuff 
      if (a.toString() == b)
      {
         Console.WriteLine("This is a really strange method");
      }
   }

Example code: 

.. code-block:: restructuredtext

   .. code-block:: csharp

      public static void DoThing(int a, string b)
      {
         // things and stuff 
         if (a.toString() == b)
         {
            Console.WriteLine("This is a really strange method");
         }
      }

Tables
======
There are four methods to creating tables in restructuredtext but two methods are better than the others so I'll stick to the two good methods here. 

Equal-sign format
-----------------
The equal-sign format uses equal signs above and below the header rows and at the end of the the table.  It's very readable in the markup but cumbersome to add rows with different widths.  The format looks like this: 

=================================   ==============================   ==============================
COLUMN HEADER 1                     COLUMN HEADER 2                  COLUMN HEADER 3
=================================   ==============================   ==============================
Text for column 1, row 1            Text for column 2, row 1         Text for column 3, row 1
Text for column 1, row 2            Text for column 2, row 2         Text for column 3, row 2
This is text for column 1, row 3    Whatever - some stuff in row 3   More weird third row stuff
=================================   ==============================   ==============================

Example code: 

.. code-block:: restructuredtext

   =================================   ==============================   ==============================
   COLUMN HEADER 1                     COLUMN HEADER 2                  COLUMN HEADER 3
   =================================   ==============================   ==============================
   Text for column 1, row 1            Text for column 2, row 1         Text for column 3, row 1
   Text for column 1, row 2            Text for column 2, row 2         Text for column 3, row 2
   This is text for column 1, row 3    Whatever - some stuff in row 3   More weird third row stuff
   =================================   ==============================   ==============================

Table directive
---------------
The table directive lets you give your table a title and create a link to the table.  Use ``.. table:: NameOfTable`` and indent the table as shown here: 

.. table:: EqualSignFormatTable

   =================================   ==============================   ==============================
   COLUMN HEADER 1                     COLUMN HEADER 2                  COLUMN HEADER 3
   =================================   ==============================   ==============================
   Text for column 1, row 1            Text for column 2, row 1         Text for column 3, row 1
   Text for column 1, row 2            Text for column 2, row 2         Text for column 3, row 2
   This is text for column 1, row 3    Whatever - some stuff in row 3   More weird third row stuff
   =================================   ==============================   ==============================

Example code: 

.. code-block:: restructuredtext

   .. table:: EqualSignFormatTable
      =================================   ==============================   ==============================
      COLUMN HEADER 1                     COLUMN HEADER 2                  COLUMN HEADER 3
      =================================   ==============================   ==============================
      Text for column 1, row 1            Text for column 2, row 1         Text for column 3, row 1
      Text for column 1, row 2            Text for column 2, row 2         Text for column 3, row 2
      This is text for column 1, row 3    Whatever - some stuff in row 3   More weird third row stuff
      =================================   ==============================   ==============================

List table format
-----------------
The list-table format creates a table in a list format.  Each row is marked with a ``*`` and each column is preceeded by a ``-``.  You can specify the column widths and number of header rows within the directive: 

.. list-table:: ListTableExample   
   :widths: 33 33 33
   :header-rows: 1

   * - COLUMN HEADER 1
     - COLUMN HEADER 2
     - COLUMN HEADER 3
   * - Text for column 1, row 1
     - Text for column 2, row 1
     - Text for column 3, row 1
   * - Text for column 1, row 2
     - Text for column 2, row 2
     - Text for column 3, row 2
   * - This is text for column 1, row 3
     - Whatever - some stuff in row 3
     - More weird third row stuff

Code sample: 

.. code-block:: reStructuredText

   .. list-table:: ListTableExample   
      :widths: 33 33 33
      :header-rows: 1

      * - COLUMN HEADER 1
      - COLUMN HEADER 2
      - COLUMN HEADER 3
      * - Text for column 1, row 1
      - Text for column 2, row 1
      - Text for column 3, row 1
      * - Text for column 1, row 2
      - Text for column 2, row 2
      - Text for column 3, row 2
      * - This is text for column 1, row 3
      - Whatever - some stuff in row 3
      - More weird third row stuff


CSV table format
----------------
The CSV table format creates a table in a CSV style. 

.. csv-table:: CSVTableExample
   :header: COLUMN HEADER 1, COLUMN HEADER 2, COLUMN HEADER 3
   :widths: 33 33 33

   Text for column 1 row 1, Text for column 2 row 1, Text for column 3 row 1
   Text for column 1 row 2, Text for column 2 row 2, Text for column 3 row 2
   This is text for column 1 row 3, Whatever - some stuff in row 3, More weird third row stuff

Code sample: 

.. code-block:: reStructuredText

   .. csv-table:: CSVTableExample
      :header: COLUMN HEADER 1, COLUMN HEADER 2, COLUMN HEADER 3
      :widths: 33 33 33

      Text for column 1 row 1, Text for column 2 row 1, Text for column 3 row 1
      Text for column 1 row 2, Text for column 2 row 2, Text for column 3 row 2
      This is text for column 1 row 3, Whatever - some stuff in row 3, More weird third row stuff

Hyperlinks
==========
This section describes various types of links that can be created with reStructuredText: 

.. _HyperlinksReference:

Linking to an external site
---------------------------
To link to an external site, you can include a normal URL directly in the text and it should create a link, for example:
https://github.com/

To embed a link to an external site under any arbitrary text, you can use the syntax using backticks, angle brackets, and trailing underscore like this: 
`Github Website <https://github.com/>`_

Code sample: 

.. code-block:: reStructuredText

   To link to an external site, you can include a normal URL directly in the text and it should create a link, for example:
   https://github.com/

   To put the link to an external site under any arbitrary text, you can use this syntax: 
   `Github Website <https://github.com/>`_

Linking to another document in the project 
------------------------------------------
To link to a document, internal to the documentation project, use `:doc:`.  To link to the project setup document of this project: 
:doc:`/documentation_with_read_the_docs/project_setup`

.. code-block:: restructuredtext

   To link to the project setup document of this project: 
   :doc:`/documentation_with_read_the_docs/project_setup`

If you want to link to an internal document embeded in custom text, use this syntax: 
:doc:`HERE IS WHERE THE PROJECT SETUP SECTION IS </documentation_with_read_the_docs/project_setup>`

.. code-block:: restructuredtext

   If you want to link to an internal document embeded in custom text, use this syntax: 
   :doc:`HERE IS WHERE THE PROJECT SETUP SECTION IS </documentation_with_read_the_docs/project_setup>`

Linking to a specific spot inside a document in the project
-----------------------------------------------------------
To link to a specific location in a document, you can create a reference at any place using `.. _NamedReference:` where NamedReference can be whatever name you want to give to this location.  Above, I've created a named reference at the Hyperlink section called `HyperlinkReference`

Then you can link to that reference using the `:ref:` keyword, for example :ref:`Here is a link to the hyperlink section <HyperlinksReference>` 

Code sample: 

.. code-block:: restructuredtext

   Then you can link to that reference using the `:ref:` keyword, for example :ref:`Here is a link to the hyperlink section <LinkingToAnotherDocumentReference>` 
