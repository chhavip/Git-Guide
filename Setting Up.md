##Setting Up git in your machine

If you don't already have github installed in your machines, follow the following steps to enable controlling your projects through git (These are instructions to install git and not specific to github, can be used with any version control).

###Windows

Install git for windows from [here](http://git-scm.com/download/win). Your download will start automatically.

###Ubuntu

For instructions on installing git for different Unix flavors see [Download for Linux and Unix](https://git-scm.com/download/linux).

###Mac

Install OSX Git installer from [here](http://git-scm.com/download/mac). Your download will start automatically.

##After installation

Now that you have git installed on your machine you should first set your name and email address.  This is important because every Git commit uses this information.

1. Open the git bash.

2. Tell git your name. Type everything after the `$` here :

   `$ git config --global user.name "YOUR NAME"`

3. Tell git your email address.

   ` $ git config --global user.email "YOUR EMAIL ADDRESS"`

> **Note** : You need to do this only once if you pass the `--global` option, because then Git will always use that information for anything you do on that system. If you want to override this with a different name or email address for specific projects, you can run the command without the `--global` option when you’re in that project.
