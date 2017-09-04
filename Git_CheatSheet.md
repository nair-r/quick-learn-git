# **Some Git Commands & Examples** 
#### (basic commands,not an exhaustive list):
------------------------------------------------------------------------------------------------------------------------------------------

Git Command | Task Description | Notes 
:-----|:-----|:-----
`git init`| initializes an empty Git (local) repo in the directory it is called from|  also creates hidden .git folder
`git status`| shows status of repo| run this often especially before committing changes!!
`git add <filename>`| adds file to the staging area
`git add -A .`| same as above, but the dot stands for the current dir., so everything in & under it is added| -A ensures even file deletions are included.
`git add '*.txt'`| using wildcards to add files in the current folder and all sub-folders under it|Wildcards: We need quotes so that Git will receive the wildcard before our shell can interfere with it. Without quotes our shell will only execute the wildcard search within the current directory. Git will receive the list of files the shell found instead of the wildcard and it will not be able to add the files inside of any sub-directory if they exist.
`git reset <filename>`| to remove a file(s) from the staging area.
`git commit -m “some description here”`| This stores our stages changes to the repo.|commit command with a message describing what we've changed.
`git log`| see all commits (changes) made to the repo in the order/when they were made.
`git log --summary`|to see more information for each commit| You can see where new files were added for the first time or where files were deleted. It's a good overview of what's going on in the project. 
`git remote`|add a remote repository|This command creates a remote repo and needs a remote repo name and a repository URL (where an empty repo has been initialized) `Ex: git remote add origin https://github.com/try-git/try_git.git` 
`git push`|pushes commits to remote repo|Ex: git push -u origin master (The name of our remote is origin in above example and the default local branch name is master.
`git pull`|check for changes on our GitHub remote repo and pull down any new changes to say, a local repo.|Ex. : `git pull origin master
`git checkout <target>`| to (re)set the state of repo to target which is shown next to commit when you do a git log|Ex: git checkout 7499a39992a606fb86caa86f161ff7f33483648234287`.  You can view the previous state of your files here. To return to the master branch to see the most current state of your files, do: git checkout master
`git branch <branch name>`|creates a copy (or branch) of the main code
`git branch`| list all branches
`git checkout <branch name>`| switch to branch name
`git rm <filenames>`| to delete files and stage for commit, all in one step.
`git checkout master`|switch to master branch
`git merge <branch-name>`| to merge changes comitted to branchname back into the master
`git branch -d <branch-name>`|to delete a branch| Works for branches that have already been merged with master. For un-merged or abandoned branches, use the -f flag too.

