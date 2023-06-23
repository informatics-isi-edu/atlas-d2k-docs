---
title: z Access our server (obsolete)
permalink: /docs/z-access-our-server-obsolete/
---

<sub>[<- Back to Documentation Home](https://github.com/informatics-isi-edu/gudmap-rbk/wiki/)</sub>

* [Generate SSH Keys](https://github.com/informatics-isi-edu/rbk-www/wiki/Generate-SSH-Keys#generate-ssh-keys)
* [Access our server](https://github.com/informatics-isi-edu/rbk-www/wiki/Generate-SSH-Keys#access-the-server)
* [Copy files or directories to our server](https://github.com/informatics-isi-edu/rbk-www/wiki/Generate-SSH-Keys#copy-filesdirectories-from-your-client-machine-to-remote-server)

# Generate SSH Keys
## Mac OS X
1. Open a terminal by going to Spotlight and type Terminal
2. At the command prompt, type 
```
  ssh-keygen 
```
3. When prompted “Enter file in which to save the key” enter `/Users/john_smith/.ssh/john_smith` 
(where you should replace `john_smith` by the account name you have in your Mac)
4. Enter and confirm your passphrase. Remember this passphrase as it will be needed to connect to the servers later.  
5. This will save the private and public key files in `.ssh` under your home directory (e.g. `/Users/john_smith/.ssh/john_smith`)
  a. john_smith  (private key file. Never share this file with anyone)
  b. john_smith.pub (public key file)
6. Email the public key file (e.g., john_smith.pub) as an attachment. Make sure you only email the public key file. 

Example
```
localhost:~ rbkcc$ ssh-keygen 
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/rbkcc/.ssh/id_rsa): /Users/rbkcc/.ssh/john_smith
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /Users/rbkcc/.ssh/john_smith.
Your public key has been saved in /Users/rbkcc/.ssh/john_smith.pub.
The key fingerprint is:
SHA256:EOSAjMOeqkcBWYVOcZX18qPeDZDhxhpLlxa1wjc2Qec rbkcc@localhost
The key's randomart image is:
+---[RSA 2048]----+
|.=o=+o+o..+ .    |
|=.=. o.o o =     |
|.=.   o * B E    |
| oo    + @ o     |
|.  .  o S o      |
|. .  . B o .     |
|..    o . .      |
|. .    . . o     |
| .      . . .    |
+----[SHA256]-----+
localhost:~ rbkcc$ ls -al ~/.ssh
-rw-------.  1 rbkcc rbkcc 1766 May 17 16:55 john_smith
-rw-r--r--.  1 rbkcc rbkcc  406 May 17 16:55 john_smith.pub
```

## Linux
1. At the command prompt on a terminal, type 
```
  ssh-keygen 
```
3. When prompted “Enter file in which to save the key”, enter `~/.ssh/john_smith` 
where john_smith is your username.
4. Enter and confirm your passphrase. Remember this passphrase as it will be needed to connect to the servers later.  
5. This will save the private and public key files in your home directory (`~/.ssh`)
  a. john_smith  (private key file. Never share this file with anyone)
  b. john_smith.pub (public key file)
6. Email the public key file (e.g., john_smith.pub) as an attachment. Make sure you only email the public key file. 

Example:
``` 
[rbkcc ~]$ ssh-keygen 
Generating public/private rsa key pair.
Enter file in which to save the key (/home/rbkcc/.ssh/id_rsa): /home/rbkcc/.ssh/john_smith
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/rbkcc/.ssh/john_smith.
Your public key has been saved in /home/rbkcc/.ssh/john_smith.pub.
The key fingerprint is:
SHA256:aLIXeTUtiM16MFo6rk/4MzHjHzYo+1+wRfCcRgc81+c rbkcc@localhost
The key's randomart image is:
+---[RSA 2048]----+
|      ..o...     |
|       Oo+... .  |
|      = Xo+ .o   |
|     + O . o  E  |
|    = B S        |
|   o+* B         |
|  o.=+* .        |
|   *+o +         |
|  oo+=o          |
+----[SHA256]-----+
[rbkcc ~]$ ls -al ~/.ssh
-rw-------.  1 rbkcc rbkcc 1766 May 17 16:55 john_smith
-rw-r--r--.  1 rbkcc rbkcc  406 May 17 16:55 john_smith.pub
```

## Windows
1. Install `WinSCP` from [http://sourceforge.net/projects/winscp](http://sourceforge.net/projects/winscp). download the installer file and follow the installation instructions.
2. Generate SSH key pair
    * Open WinSCP and go to Tools -> Run PuTTYgen and click Generate in the PuTTY Key Generator window
    * Once the Key was generated enter your secret passphrase in the Key passphrase field. Remember this passphrase as it will be needed to connect to the servers later.
    * Click the “Save public key” button and save the file to your Documents folder and give it a `.pub` extension,e.g., `john_smith`.pub)
    * Click the “Save private key” button and save the file to the same directory you saved the public key and give it the same name but with extension .ppk (e.g., john_smith.ppk). 

![ssh_keygen_windows1](wiki_images/ssh_keygen_windows1.png)


# Copy files/directories from your client machine to remote server

User the following commands to copy a certain file or directories to our server
* `rsync -avz src/bar data-staging.isrd.isi.edu:~/data/tmp`   

This would recursively transfer all files from the directory src/bar on your local machine into ~/data/tmp/bar directory on our server. The files are transferred in "archive" mode, which ensures that symbolic links, devices, attributes, permissions, ownerships, etc. are preserved in  the  transfer.  Compression will be used to reduce the size of data portions of the transfer. If you don't want the compression, use `av` instead of `avz`. You can re-execute the same command when the content of src/bar changes. `rsync` will check for the updates and only transfer the difference to save the work. 

* `rsync -avz src/bar/ data-staging.isrd.isi.edu:~/data/tmp`

A trailing slash on the source changes this behavior to avoid creating an additional directory level at the destination.  You can think of a trailing / on a source as meaning "copy the contents of this directory" as opposed to "copy the directory by name".

* `rsync -t *.png data-staging.isrd.isi.edu:~/data/tmp` 

This  would  transfer all files matching the pattern *.png from the current directory to the directory ~/data/tmp on the remote server.

* `man rsync`
Access the help page of how to use `rsync` in more detail. 


# Access the server
* After your have uploaded your files to `data-staging.isrd.isi.edu`, you might want to access our server to check that everything is uploaded accordingly.
 
To access the server, type the following command to your terminal.
```
ssh data-staging.isrd.isi.edu
```
The ssh program will prompt you to enter the passphrase.

* After you login, use the following commands to navigate to change the directory or list files under a certain directory. 

| Command | Description |
|----|----|
|`ls` | list the current directory structure |
|`ls -al` | list the current directory structure with detailed information |
|`cd` | change to the home directory |
|`cd <path>` | change directory to what's specified in `<path>`|
|`mv <file1> <file2>` | rename `<file1>` to `<file2>` under the same directory | 
|`mv <file1> <directory>` | move `<file1>` from current directory to the specified `<directory>`|
|`mv <file1> <directory>/<file2>` | move `<file1>` from current directory to the specified `<directory>` and rename it to `<file2>` |
|`man <command>`| get access to help for a specific command e.g. `man ls`|

