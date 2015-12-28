# Git-Guide
A collection of commands needed while working on git

##Set Up
In order to set up the user through terminal:

`git config --global user.name <name>` 

`git config --global user.email <email>` 

This is the user your commits and PR will be shown through.

##Fork, Clone,Add, Commit and Push
In order to work on an existing project that is not owned by you, follow the following steps:

1. `Fork` the project from the respective repository. This will redirect you to your fork of the project which is basically a copy of the original project but you are its owner.
2. Copy the HTTPS link of the project and go to the location through terminal or command prompt where you want to have the repository locally
3. Run `git clone <link to your fork>`. This will give you a local copy of the project which you can work with.
4. Any changes in the local repository can be tracked by running `git status` in that directory. Files in red will be the ones that have been modified, added or deleted.
5. To have your remote repository(the one hosted online also referred to as *origin*) reflect the changes, do `git add <file-path>` for all the files who's changes you wish to see in the remote. You can also run `git add .` to add all the files that have been changed (not advisable though). Run `git status` once again and you will see the files that you have added in green.
6. 

##Setting up Upstream
