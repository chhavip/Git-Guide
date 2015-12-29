# Git-Guide
A collection of commands needed while working on git

##Set Up
In order to set up the user through terminal:

`git config --global user.name <name>` 

`git config --global user.email <email>` 

This is the user your commits and PR will be shown through.

##Fork, Clone, Add, Commit and Push
In order to work on an existing project that is not owned by you, follow the following steps:

1. `Fork` the project from the respective repository. This will redirect you to your fork of the project which is basically a copy of the original project but you are its owner.
2. Copy the HTTPS link of the project and go to the location through terminal or command prompt where you want to have the repository locally
3. Run `git clone <link to your fork>`. This will give you a local copy of the project which you can work with.
4. Any changes in the local repository can be tracked by running `git status` in that directory. Files in red will be the ones that have been modified, added or deleted.
5. To have your remote repository(the one hosted online also referred to as *origin*) reflect the changes, do 
`git add <file-path>` for all the files who's changes you wish to see in the remote. You can also run `git add .` to add all the files that have been changed (not advisable though).
6. Run `git status` once again and you will see the files that you have added in green.
7. In case you need to un-add any file, run `git reset HEAD -- <file path>`
8. To commit the changes (equivalent to locking down the changes you have made), run `git commit -m "Your commit message"`
9. So far you have made and saved the changes in your local repository, to send the changes to your fork in github, run
`git push` which will ask for your username and password. Fill and you are ready to go. 

  NOTE: This by default pushes all your local branches to remote with the same name. We will go through branching later.


##Setting up Upstreams
When a repository is cloned, it has a default remote called `origin` that points to your fork on GitHub, not the original repository it was forked from. To keep track of the original repository, you should add another remote named `upstream`:

1. Open terminal or git bash in your local repository and type:

   `git remote add upstream https://github.com/systers/powerup-android.git`
  
1. Run `git remote -v` to check the status, you should see something like the following:

  > origin    https://github.com/YOUR_USERNAME/powerup-android.git (fetch)
  
  > origin    https://github.com/YOUR_USERNAME/powerup-android.git (push)
  
  > upstream  https://github.com/systers/powerup-android.git (fetch)
  
  > upstream  https://github.com/systers/powerup-android.git (push)

1. To update your local copy with remote changes, run the following:

   `git fetch upstream`

   `git merge upstream/master`

   This will give you an exact copy of the current remote, make sure you don't have any local changes.
