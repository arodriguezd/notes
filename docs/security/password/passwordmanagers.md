# Pass

Password management should be simple and follow Unix philosophy. With Pass, each password lives inside of a gpg encrypted file whose filename is the title of the website or resource that requires the password. 
These encrypted files may be organized into meaningful folder hierarchies, copied from computer to computer, and, in general, manipulated using standard command line file management utilities.
Pass is a simple password manager for the command line.


Pass is a shell script that makes use of existing tools like GnuPG, tree and Git.

!!! note
    Before configuring Pass you need to have a GPG certificate to encrypt the credentials.

To get started with Pass, follow these steps:


#### Install 
1. Install Pass: You can install Pass by running the following command in your terminal:
    ```
    sudo apt-get install pass
    ```

2. Generate a GPG key pair: If you don't have a GPG key pair yet, you can generate one by running the following command:
    ```
    gpg --full-generate-key
    ```

3. Initialize Pass: Once you have a GPG key pair, you can initialize Pass by running the following command:
    ```
    pass init <your-email@example.com>
    ```

4. Add a password: To add a password, use the following command:
    ```
    pass insert <website-or-resource>
    ```

    This will prompt you to enter the password for the website or resource. Pass will then encrypt and store the password in a file.

5. Retrieve a password: To retrieve a password, use the following command:
    ```
    pass show <website-or-resource>
    ```

    This will display the decrypted password on the command line.

Remember to always keep your GPG key pair secure and backup your Pass password store regularly.





