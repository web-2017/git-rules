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

	git clone [url]                      
	git clone [url] myFolder
	git clone ssh://user@host.org/project.git
	git clone -b [branchname] --single-branch [remote-repo-url]		#clone only one branch
	
**Push branch**

	git push | git push --force

**Pull remote branch**

	git pull makes 2 command: 1. git fetch 2. git merge; to local branch
	git pull

**Create new branch**

	git branch [feature/login]

**DELETE**
 
	git branch -D [feature/login]						#local branch
	git push origin -d [feature/login]					#remote branch

**Remove references to remote branches that have already been deleted**

	git fetch --prune							#local
	git fetch --prune origin						#remote

**Remove files from cache**

	git rm --cached [file_name]
	git rm --cached -r [dir_name]

**Rename branch**

	git checkout [feature/login]
	git branch -m [feature/login]

**Edit last commit without creating new commit (try not use it)**

	git commit --amend --no-edit

**Hide changes**

	git stash								#hide
	git stash save "your message" 
	git stash list  							#show list 
	git stash apply								#return stash
	git stash apply	stash@{0}  						#return stash stash@{0}
	git stash clear 							#clear all stash

**List branches**

	git branch -a


## Set default editor code for git (VSCode)

> git config --global core.editor "code --wait"
