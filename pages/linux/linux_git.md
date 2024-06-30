---
title: Git
keywords: linux git
summary: "Use the git application"
sidebar: linux_sidebar
permalink: linux_git.html
folder: linux
---

## Show config 


~~~
#List the config 
git config --list
git config --list --show-origin
~~~

## Config 


~~~
#Display the editor the config local
git config --local core.editor "vim" / "code --wait"
git config --local user.name "[Name]"
git config --local user.email [e-mail]
git config --local user.signingkey [sec]
git config --local gpg.program gpg2 //   Install the packages gnupg2
git config --local color.ui [true / false / auto / always]
git config --local color.diff [true / false / auto / always]


#Display the editor the config global
git config --global core.editor "vim" / "code --wait"
git config --global user.name "[Name]"
git config --global user.email [e-mail]
git config --global user.signingkey [sec]
git config --global gpg.program gpg2 //   Install the packages gnupg2
git config --global color.ui [true / false / auto / always]
git config --global color.diff [true / false / auto / always]
~~~


## Basic Command


~~~
#See branch
git show-branch

#View current branch 
git branch

#Create new branch
git [Name_branch]

#Change de current branch other
git checkout [Name_branch]

#Create new branch and you move to it
git checkout -b [Name_branch]

#Delete branch
git branch -d [Name_branch]
git branch -D [Name_branch]

~~~

