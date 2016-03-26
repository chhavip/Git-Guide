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
* * `git init` So that git commands start working in this directory
