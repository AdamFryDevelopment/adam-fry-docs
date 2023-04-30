Using Github for Version Control
================================
We can create a github repo to store our documentation project.  If you don't already have a github account, sign up for one at https://github.com/

GitIgnore
---------
The _build folder that is created by the make command is generally not wanted in our source control repository.  Add a .gitignore file to the project and content to specify that this should be excluded.  Create a new file in the root of the project folder named .gitignore and add the following content to the file: 

.. code-block::

   _build/

Create local repository
-----------------------
Before we can push to a remote repository, first setup the local repository in VSCode.  Click the source control icon or press CTRL+SHIFT+G to open the source control pane.  Click the initialize icon button to initialize the local repository.  If prompted for the local repository folder, select the root folder.  

Create initial commit
---------------------
Enter a message for the initial commit and click the commit button.  If prompted that no changes are staged and whether you want to stage changes, choose always.  This commits the current version of the project to the local repository.

Publish branch
--------------
Once changes are committed, they can be published to a new github repo.  Click the publish branch button.  You will be prompted to sign into your github account.  Follow the prompts to sign in and generate a github repo to push to.

Connecting Github and ReadTheDocs
---------------------------------
Once you have a github repo, sign up for an account at https://readthedocs.org/.  Once you have an account on ReadTheDocs, open your account settings and click the connected services link.  Select **Connect to Github**.  Follow the prompts to authorize your ReadTheDocs account to connect to your Github account.  Once connected, click on your account and click **Import a Project**.  ReadTheDocs should present you with a list of your GitHub repos.  Select the repo that we created in the prior step.  

.. warning :: 
   Make sure to enter the name of the branch of your github repo where the documentation is.  ReadTheDocs will default to Main.  VSCode may default to Master branch so change the setting to Master or else ReadTheDocs build will fail to pull the code down to build. 

Click **Next** and you'll be taken to a page that shows the documentation project is building.  Give it a minute and then refresh the page to see your documentation is ready.  Click the view the documentation link and see your documentation project now hosted online.

