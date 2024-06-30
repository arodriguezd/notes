---
title: GPG
keywords: linux gpg
summary: "Use the gpg application"
sidebar: linux_sidebar
permalink: linux_gpg.html
folder: linux
---

## Create GPG keys


~~~~
$ gpg --full-generate-key
~~~~


## List keys GPG install


~~~
$ gpg --keyid-format short --list-keys
$ gpg --keyid-format long --list-keys
~~~




## Basic Command


~~~

#View gpg keys
gpg --list-secret-keys 
 
#Delete public gpg 
gpg --delete-key [ID]

#Delete private gpg
gpg --delete-secret-key [ID]

#Revoke gpg 
gpg --import [File_revoke]

#Export public key
gpg --export -a [ID]

#Export private key 
gpg --export-secret-key -a [ID]

#Export Revoke key
gpg --gen-revoke [ID]

#Import key private
gpg --import private.key

gpg --fingerprinte [ID]

~~~


