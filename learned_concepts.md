# Learned Concepts

A track record of topics and interesting facts that I've learned each week.

## Week 1
### Tuesday
**1. Command Lines**

*go to directory*

$ cd ~/desktop
  
$ cd ..

$ cd -

*to list what's in the current folder*

$ ls -alrt (or l in Zshell)

$ ls -rthl

*to make a new folder*

$ mkdir <folder_name>

*to create a new file*

$ touch <file_name>

*to write into a file (add to the end)*

$ echo "xxx" >> <file_name>

*to write into a file (overwrite)*

$ echo "xxx" > <file_name>

*to copy file and name it file_name2*

$ cp <file_name> <file_name2>

*to delete a folder permenantly (be careful with -rf!)*

$ rm -rf <folder_name>

*to delete a file permenantly*

$ rm <file_name>

*to move a file or rename*

$ mv <file_name> <file_name2>

*to print working directory - know where you are*

$ pwd

*to search for a string*

$ grep --color -i "xx"

*to look for the manual*

$ man <command>

----
$ vim <file_name>

enter "i" to insert

to save and quit -> esc + :wq <file_name>

to force quit -> esc + :q!

*To write an terminal exec file, start with this line*

$ #!/bin/bash


*To make it executable, must make sure "r w x" has the x turned on*

 2^2 = 4    r = read
 
 2^1 = 2    w = write
 
 2^0 = 1    x = execute
 
*so a file that is rwx = 7, rx = 5, x = 1, r = 4(read only)...concept of binary*



**2. Git & GitHub**

$ git init

$ git status

$ git remote add origin http://.... (origin could be any name)

$ git remote -v

$ git push -u <remote_name> <branch_name> (origin master)

$ git add <file_name>

$ git -rm -cached <file_name>

$ git commit -m "xxx"

$ git pull <remote_name> <branch_name> http://.... (origin master)

*It is possible to have more than one remote,e.g. pull from github/codingnomads and push to github/personal*

*Don't create git folders inside other git folders*


