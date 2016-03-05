# GIT notes

Quick GIT cheat-sheet



## Repository

* **clone a repo, gets all the history & commits**
    
    git clone url

* **initialize a git repo**
    
    git init

## Configurations
* **check username, email & other configs**

    git config user.name
    
    git config user.email
    
    git config --list

* **check global username, email**

    git config --global user.name
    
    git config --global user.email


* **set username/email local to repository**

    git config user.name “Amrendra Kumar”

    git config user.email “amrendra[dot]nitb[at]gmail[dot]com”

* **set global username/email**

    git config --global user.name “Amrendra Kumar”

    git config --global user.email “amrendra[dot]nitb[at]gmail[dot]com”


## Tags

* **add tag to local commit**

    git tag "v1.0" "commit-id"

* **push all tags to remote branch**

    git push origin master --tags

* **delete a tag locally**

    git tag -d "v1.0"

* **push deletion of tag to remote branch**

    git push origin master :refs/tags/"v1.0"

## Commits

* **add a commit**

    git commit

    git commit -m "your commit message"

* **undo initial commit**

    git update-ref -d HEAD

* **list all commits**

    git log

* **list all commits single line**

    git log --pretty=oneline

* **list all commits with change stats**

    git log --stat

* **check what changes were made by particular commit**

    git show commit-id


## Difference

* **diff bw latest commit & head**

    git diff HEAD^ HEAD

* **diff bw head & particular commit**

    git diff commit-id HEAD

* **diff bw working dir & staging area**

    git diff

* **diff bw staging area & repo**

    git diff --staged

* **diff bw commit1 & commit2**

    git diff commit-1 commit-2

## Branch

* **view branches**

    git branch

    git branch -v

* **create new branch**

    git branch new-branch-name

* **create & switch to new branch from current commit**

    git checkout -b new-branch-name

## Remote

* **list all remotes**

    git remote

    git remote -v

* **add a remote branch**

    git remote add name-of-remote remote-url


* **push changes to remote**

    git push origin master

* **pull changes from remote branch**

    git pull origin master

    Note: git pull is combination of fetch & merge



## Undo

* **revert changes in working directory & staging area**

    git reset --hard

* **just undo the changes in file which has not been added to staging area**

    git checkout -- file


## Frequents

* **add all files to staging area**

    git add .

* **changing files back to state at the time of last checkout**

    git checkout

* **merge branchA into branchB**

    git checkout branchA

    git merge branchB branchA

* **remove a directory from git, but not from filesystem**

    git rm -r folder-name
