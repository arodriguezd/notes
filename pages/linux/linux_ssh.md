---
title: SSH
keywords: linux ssh
summary: "Use the ssh client and server"
sidebar: linux_sidebar
permalink: linux_ssh.html
folder: linux
---

## Generate keys ssh

The ssh key allows us to connect to remote instances without using authentication password. 
To generate a key we execute one of the following statements:

~~~~

$ssh-keygen –t ecdsa –b 512 -C [comment] -f [name-file-private-key]
	
$ssh-keygen –t ed25519 –a 200 -C [comment] -f [name-file-private-key]
	 
$ssh-keygen –t rsa –b 4096 -C [comment] -f [name-file-private-key]

~~~~

-t type 
Specifies the type of key to create

-b bits
Specifies the number of bits in the key to create. For RSA keys.

 -a trials
Specifies the number of primality tests to perform when screening DH-GEX candidates using the -T command.

-C comment
Provides a new comment.

-f filename
Specifies the filename of the key file.


## Config in server


In order to connect to a remote server we must add the ssh public key to the user we use to access the instance. 
The recommendation is to use a non-root account. 

``
~/.ssh/authorized_keys
``
~~~

jdoen@machine:~$ pwd 
/home/jdoe

jdoe@machine:~$ ls -la
[...]
drwx------ 2 jdoe jdoe 4096 Jun 14 09:26 .ssh

jdoe@mchine:~$ ls -la .ssh/
[...]
-rw------- 1 jdoe jdoe  822 Jun 14 09:26 authorized_keys


~~~
