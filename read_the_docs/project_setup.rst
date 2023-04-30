Project Setup
+++++++++++++

Create a Sphinx project
=======================
To create a new project, create a new folder where the project files will be stored in your file system.  From a command prompt, change directory to the new folder and then run the sphinx-quickstart command: 

.. code-block:: bash

   cd PATH\TO\YOUR\NEW\FOLDER
   sphinx-quickstart

You will be prompted for several values to set up the documentation project.  Generally accept the defaults.  The following files will be created in your folder: 
   - conf.py - a python file that contains configurations for the project
   - index.rst - restructure text file that is the starter page for the documentation project.  We will edit this to lay out the sections of our documentation site.
   - make.bat - run this to make the documentation website from the ReStructured text files

Open the project in Visual Studio Code
======================================
To open the documentation project, click File > Open Folder, and select the directory that contains your Sphinx documentation project

Changing the theme
==================
Open the conf.py file and change the html_theme value to sphinx_rtd_theme: 

.. code-block:: python

   html_theme = 'sphinx_rtd_theme'

Build and Preview Documentation
===============================
To build and preview the project, open the VSCode terminal by clicking View > Terminal and then enter the make html command: 

.. code-block:: bash

   .\make html

When you run the make command, a `_build` folder will be created for the documentation website.  You can open the _build\\html\\index.html file in a browser to preview the documentation site.

Configure Read the Docs
=======================
Create an account on the Read the Docs website (https://readthedocs.org/) and configure your project settings, such as the repository URL, build settings, and documentation versioning. Once configured, Read the Docs can automatically build and publish your documentation whenever changes are pushed to your version control repository.

Publish the documentation
=========================
Publish your documentation to Read the Docs by pushing the generated documentation files to the appropriate branch in your version control repository. Read the Docs will automatically build and publish the documentation based on your project settings.

Access the documentation
========================
Once published, your documentation will be accessible via the Read the Docs website or the custom domain you have configured, allowing users to view and reference your documentation online.