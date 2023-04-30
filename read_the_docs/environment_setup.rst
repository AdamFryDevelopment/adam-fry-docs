Environment Setup
+++++++++++++++++
Before you can build and host your documentation using Read the Docs, you need to install some prerequisites. Follow the steps below to install the required software:

Python
======
Read the Docs is built using Python, so you'll need to have Python installed on your system. You can download the latest version of Python from the `official Python website <https://www.python.org/downloads/>`_ and follow the installation instructions.

..  note::
    When running the Python installation wizard, make sure to check the option to add Python to the path

Sphinx
======
Sphinx is the documentation generation tool that Read the Docs uses. You can install Sphinx using `pip`, the Python package manager. Open a terminal or command prompt and run the following command:

.. code-block:: bash

   pip install sphinx

Sphinx Themes
=============
Read the Docs provides several themes that you can use to customize the appearance of your documentation. You can install the themes using `pip` as well. Run the following command:

.. code-block:: bash

   pip install sphinx_rtd_theme

Visual Studio Code (Optional)
=============================
Visual Studio Code is a great free text editor that works well for a ReadTheDocs project. `Download <https://code.visualstudio.com/download>`_ and install it and once installed, add the "reStructuredText" extension. You can install this extension from the VSCode Extensions Marketplace by searching for "reStructuredText" in the Extensions view (Ctrl+Shift+X).