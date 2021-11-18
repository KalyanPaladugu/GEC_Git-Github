Git:
====
+ Downloas Git from https://git-scm.com/downloads
+ Install it

Version controll system:
========================
+ Version control is a system that records changes to a file or set of files over time so that you can recall specific versions later

Centralized Version controll system:
====================================
+ In this centralized source control, there is server(master) and one or more users(clients)involved.Here the server is master repository which contains all the version of source code
+ The master repository contains updated version of the source code.Users can pulls the source code from the master and then do the own changes to the source code.Finally push the updated code to the central(master) repository
+ Github remote repository,SVM(Apache subversion)

Distributed Version Control System:
===================================

+ Working offline
+ Data will not be lost
+ Git,Mercurial are examples

Uses of Git& Github:
====================
+ While doing Global certifications like Udacity,Coursera they will prefer Git&Github
+ We can track history of files in the project
+ While working on a project to collaborate with team members we can use Git&Github

Git options:
============
+ Git Bash emulates a bash environment on windows. It lets you use all git features in command line plus most of standard unix commands
+ Git GUI is a Graphical User Interface letting you use Git without touching command line. It is an alternative among other Git clients

+ To check version of git use `git --version` command

Linux commands in git bash:
===========================

+ In linux to navigate from one folder to another folder we have to use cd(change directory) `cd foldername`
+ To create folder we have to use `mkidir foldername`
+ To see list of files in folder use `ls`
+ To create file `touch | vim(open editor)  filename`
+ When you create file using vim editor after writing of code use `:w` to save code and `:q` to exit from the editor
+ To edit file use `nano filename`.It will open nano editor in that write your code.To save and exit nano editor use `ctrl+x` and then click `y` it will goto save mode file path `Filename name to write : filename` and then click on `Enter`.It will go back to project folder.Then see your edited code by `cat filename`

+ To remove any file use `rm filename`
+ To remove folder `rm -r foldername`

##Git commands:
===============
+ First we need to initialize git repositroy by `git init`
+ To see  git folder use `ls -a`(It will show hidden files also)

+ Main in git we have 3 areas
	+ Untracked area(those files(red color files) are not adding to git )
	+ Staging area (Files(green color) added to git)
	+ Commit area
+ To check files are tracked or untracked we can use `git status`
+ To check the status of a file use `git status`
+ To add a single file to stage area use `git add filename`
+ To add multiple files to `git add . or git add --all`
+ To move file from staging area to untracked area use `git rm --cached filename`
+ Commit all the files by using `git commit -m "Version1`+ For every commit a SHA(Secure Hash Algorithm) key with 40 characters length will generate to theck that one use `git log`
+ if it is asking tell me who you are? like this we have to configure git with username and email

Configurations:
===============
+ We have to configure git by providing username and email globally(better to use github logins)
+ git config --global user.name "Username"
+ git config --global user.email "your email"


+ If we want check particulr n-commit data we have to use first seven chareacters of a SHA key. For that use `git log --oneline`
+ We can check the files in first commit by using SHA key with command of `git checkout xxxxxxx`(first 7characters of SHA key).Which means we can get the data at the first commit.Similary we can get the data @ nth position commit

+ After switch to particular commit you can update data and then commit finalupdated data.
+ To check the number of commits ` git rev-list --count HEAD`

Note:
=====
```In case if you updated data with new commit if you want to continue with coomit create new branch with those commit by usning `git branch branchname xxxxxxx(sha key).```


+ Then switch to master branch by using `git checkout master` 

Change commit message:
----------------------
+ To change latest commit message use `git commit --amend -m "updated".To change commit message when head-->master is possible`

Delete commit:
--------------
+ To delete latest commit use `git reset HEAD^`.If you want to delete with data with commit use `git reset --hard Head^`
+ To delete number of commits use `git reset --hard HEad~2` here i want to delete 2 latest commits
+ To delete specific commit we have to user "git rebase --onto --branchname ~ number to delete the commit branchname ~ number(Head to master is @which commit) to kept branchname "
+ `git rebase --onto master~3(delete first commit(1-commit(delete),2-commit,(3)final-commit:master will head to 3rd commit)) master~1 master`

