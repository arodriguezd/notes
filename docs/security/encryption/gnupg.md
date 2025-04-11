# GNUPGP

A GPG certificate allows us to encrypt email messages, encrypt files, and authenticate code in git repositories, as well as being able to use it with Pass to have a local password manager.


#### Create keys GPG 
```
gpg --full-generate-key
```

#### View GPG keys
```
gpg --list-key
```

List keys GPG install 

Short format
```
gpg --keyid-format short --list-keys
```

Long format
```
gpg --keyid-format long --list-keys
```

Other options 
```
gpg --list-secret-keys gpg  <your_email>
```

```
gpg --fingerprint <your_email>/<ID>
```
 
#### Delete GPG keys

Delete public gpg
``` 
gpg --delete-key <your_email>
```

Delete private gpg
```
gpg --delete-secret-key <your_email>
```


#### Export GPG Keys

Export public key
```
gpg --export -a <your_email>/<ID>
```

!!! warning
    Store the private key in a safe place and with a strong password

Export private key 
```
gpg --export-secret-key -a <your_email>/<ID>
```

Export Revoke key
```
gpg --gen-revoke <your_email>/<ID>
```

#### Import GPG keys
Import public and private key 
```
gpg --import <name_file_gpg.key>
```

#### Renew subkeys 

```
gpg --edit-key <your_email>/<ID>

gpg>key [ID-subkeys] 

gpg> expire 

gpg>save
```

