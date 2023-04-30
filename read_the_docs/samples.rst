Samples
=======
This is a collection of example reStructuredText code.

Index
-----
An index generally contains a table of contents and links to other files.  This sample index has a heading describes the section and a table of contents that point to several sub-sections by listing the relative pathed files that exist in the same location as the index.

.. code-block:: restructuredtext

    Creating documentation with ReadTheDocs
    =======================================
    This section covers creating and maintaining a documentation project such as this using ReadTheDocs, Github, and ReStructured Text markup syntax.  It covers setting up continuous integration and continuous delivery of the documentation by using github as source control and integrating with ReadTheDocs to automatically build and deploy updates to the documentation as they are pushed into the main branch.

    .. toctree::
    :maxdepth: 2
    :caption: Contents
    :hidden: 

    overview
    environment_setup
    project_setup
    restructuredText_reference
    hosting_on_readthedocs_website
    editing_this_project