Git
+++
This is some useful git commands

Connecting to git repo from command line 
========================================
.. code-block:: bash

    git init
    git add .
    git commit -m "YOUR COMMIT MESSAGE"
    git branch -M main
    git remote add origin url_to_github_repo.git
    git push -u origin main

Making a commit from command line 
=================================
.. code-block:: bash

    git add .
    git commit -m "YOUR COMMIT MESSAGE"
    git push -u origin main

Switching between github accounts 
=================================
Using multiple github accounts with windows is cumbersome.  One way to switch between accounts is to delete the github credential stored in windows credential manager and to change the github user name and password at command line.  This will cause you to be prompted to authenticate when you push and ensure your commits display with the correct user name.  There are other more automated ways to handle this with SSH keys and SSH config files but this manual approach is easy and works well as long as you aren't switching back and forth a lot.

Deleting existing github credential 
-----------------------------------
Remove the existing github credential from windows credential manager so that you will be prompted to authenticate with github when you push: 

   - Windows > Control panel > User accounts > Credential manager
   - Manage windows credentials
   - Remove the credential for git:https://github.com

Change github user name and email from command line
----------------------------------------------------
After removing your credential, github will prompt to authenticate on push but if you don't change your user name and email using the git command line then your commits will show the wrong user on them.  Change your git user name and email from command line with these commands: 

.. code-block:: bash

    git config --global user.name "YOUR USER NAME"
    git config --global user.email "YOUR GITHUB EMAIL"
