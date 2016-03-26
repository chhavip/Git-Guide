
#Git Guide for Collaborative Work

##Introduction
This page will outline a basic workflow to use when working on collaborative projects, wherein one person sets up the initial project and others are able to work on the same. Let us assume the situtation where there are three people Mo, Meggie and Darius who need to work on a project together and would like to use git/github for collaboration. Assuming they all have gitbash(windows) or git in terminal(linux) or on Mac, these are the steps to follow:

###Setting Up The Project
Only one person needs to create the initial project and push it to the remote. Let us assume it is going to be Mo. Steps needed to be followed by Mo are:
* Create an account on github.
* Create a new Repository by clicking the **NEW** repository button. 
* Give it a name.
* See the initial page and locate the https URL where this repository exists. 
* Add Meggie and Darius as **Collaborators**(to give them write permissions to this repository) by going in Settings of this repository.
* Open git bash/terminal and go into the directory where your local project exists(the one on which you plan to work on, create it like you would create any other local project of that kind). Lets say the project they plan to work exists in Mo's machine at `/Documents/PythonProjects/mysite`. The terminal would look something like: 
* The steps to follow for Mo here are
  * `git init` So that git commands start working in this directory
  * `git remote add origin URL` Here URL refers to the URL where you created the new repository in github. This is used to connect your local folder(mysite) to the one on github.
  * Now when you run `git status` you are able to see all the files that exist in the local folder. As they come in red, it means they are not ready to be sent to the remote. We need tou change that
  * Run `git add .` (to add all files at once, in future you can add one file at a time by running `git add <complete path to required file>` {without brackets}). Now when you run `git status` you will be able to see your added files in green.
  * Now these files need to be committed as only files bound by a commit are sent to the server, added files are not. This is used that in case you have made changes to 5 files and need to send only 3 of them, you can add only those three and then commit them to finalise their sending.
  * Run `git commit -m "Commit Message"` The message logically explains what changes you made in this commit.
  * Run `git push -u origin master` (The -u is required only on the first commit, afterwards you will only need to use `git push origin master`). What this command does is to push your local changes to the origin (which we added few steps before) and to the **master** branch (All we need to know about branches right now is that git works in form of branches and if none other is specified, all the work takes place on the master branch).
  * After doing this, Mo's work is finished (which was a lot!)

*Steps to follow for Meggie and Darius to get the project uploaded by Mo:
 * First of all you will be glad to know that they **dont** need to create a local project, they can get the project uploaded by Mo in their machines.
 * Now suppose Meggie wants the project to be in the `/Documents/PythonProjects` directory, she has to go to that directory in her git bash or terminal.
 * (One Time Step) Run `git clone URL` where URL is the same URL as used by Mo to upload the project. This is done just once to get a copy of the remote project locally and doesn't have to be done again.
 * And voila! The project is with Meggie and she can run it like any other project of that kind. After making any changes to the project she will have to got to the directory `/Documents/PythonProjects/mysite` (all git commands are run from this directory henceforth, this can be the path to your own directory).

That was it! Now all three, Mo, Darius and Meggie have a syncronised copy of the project and can start working locally. To push their changes to the remote they will need to follow the **Synchronisation** process as described below.

