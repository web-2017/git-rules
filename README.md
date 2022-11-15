# Git rules cheatsheat 
### most popular commands

## Start 

**Config - setup git**

	git config --global user.name "Username"
	git config --global user.email "some@email.com"

**Create - from existing data**

	cd ~/my_project_directory
	git init
	git add . 
	
**Clone**

	git clone ~/existing_repo ~/new/repo
	git clone git://host.org/project.git
	git clone ssh://user@host.org/project.git
	git clone [url]                      
	git clone [url] myFolder 
	
**Push branch**

	git push | git push --force

**Pull remote branch**

	git pull makes 2 command: 1. git fetch 2. git merge; to local branch
	git pull

##### Create new branch

> git branch [feature/login]

##### DELETE local branch

> git branch -D [feature/login]

##### DELETE remote branch

> git push origin -D [feature/login]

##### Rename branch

> * git checkout [feature/login]
then
> * git branch -m [feature/login]

##### Edit last commit without creating new commit (try not use it)

> git commit --amend --no-edit

##### Delete all remote merged branches

> git fetch --prune

##### Hide changes

> * git stash // hide
> * git stash list // show list 
> * git stash apply // return stash
> * git stash clear // clear all stash

##### clone remote branches

> git clone [git@github.com]

##### clone remote one branch

> git clone -b [branchname] --single-branch [remote-repo-url]

##### check all remote branches

> git branch -a

##### Remove from git cache .gitignore current file

> git rm -r --cached test.js

##### Set default editor code for git (VSCode)

> git config --global core.editor "code --wait"
