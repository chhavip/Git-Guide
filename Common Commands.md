# Common Commands 

## Making changes
* Adding Files
 * `git add <filename>` : 
 * `git add .`
* Stashing Changes
 * `git stash`
 * `git stash pop`
* Committing Files
 * `git commit -m "[descriptive message]"`
* Unstaging Files
 * `git reset <filename>`

## Reviewing Changes
* `git status` : List the files you've changed and those you still need to add or commit
* Viewing File Differences :
  * `git diff` : Shows file differences not yet staged.
  * `git diff --base <filename>` : View the changes against the base file.
  * `git diff <sourcebranch> <targetbranch>` : View changes in source branch against a target.
* `git log` : View summary of all commits made so far in the current branch.


## Receiving Files
* `git fetch` : Fetch changes from remote repository

## Searching for Files
* `git grep <search term>` : Search the current branch for given term

