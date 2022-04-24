# learning-git

## This repo was used to learn git: 

ctrl + l: to clear screen

git config --global user.name "your name in github" (1)
git config --global user.email "email used to register github" (2)

git config [<options>]: to see all options
git config -l: to see all infomation (1,2) and click Q to exit command
git config --edit: to edit 1,2

=======================================================================================
git repository contain a collection of files of various different versions of a project
mkdir learning-git
ls
cd learning-git
ls
git init: make a brand project become git repo
rm -rf .git: to remove .git in working dir
after above line, we cant git add cause working dir is no longer a git repo
git init
git add: in working dir, we have nothing here, so "nothing added", and git bash recomment to "git add ."
=======================================================================================
create file: 
touch index.html

touch index.js

touch index.css

ls: to see file inside learning-git folder

git status: give us the current state of your git working directory and staging area
		give us the status of the change that we have made
	and in status we will see 3 file that call UNTRACKED FILES and git recommend use git add <file>
	to be can commited
git add index.html: add index.html into a staging area
git rm --cached index.html: to unstage/remove a index.html file form stage area
git add index.html
git add index.js
git status: screen show html and js into a "changes to be committed"
git add . : add all the file form this current directory 
git status: show all file and see all file in a "changes to be committed"
git rm -r --cached . : to unstage all file form changes to be committed

create folder:
mkdir test

cd test: so we now at a test folder
	git add . : we just add all file in test folder
	git status: to check untracked files, we see 3 file outside of test folder do not add to stage area
git add -A: whatever we are at spectifi folder, all file will be add to stage area
=======================================================================================
vi main.css: open a file main.css 
click i to insert code into main.css
click esc -> :wq to save changes
git status
git log: to see a committed history
git commit --amend -m "added body{} in main.css": change the latest commit message
=======================================================================================
git pull: get latest changes from remote if local repo != remote repo
cat main.go: to see code inside of main.go
=======================================================================================
a branch represents an independent line of development
git branch: to check list branch in local
git branch -r: to check list branch in remote
git branch -a: to check list branch in both local and remote
git branch (feature-a): create a new branch named feature-a
git checkout feature-a: to switched to branch feature-a
git checkout - : to switched to previous branch
vi untils.js: to create untils if does't exist and open it, insert press i, save press esc and then :wq
commit in which branch, git log show commit history of that branch
after create a new branch in local, that branch is not exist in remote yet, 
so git push --set-upstream origin feature-a/git push -u origin feature-a to push new branch into remote

git checkout -b to-delete: create a to-delete branch and switched to it
git checkout -d to-delete: to delete a branch named to-delete
