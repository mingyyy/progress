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

*To write an terminal exec file, start with this line, where "shabang" means find the executable.*

$ #!/bin/bash

* To run the file in Terminal

$ bash <file_name>

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


### Wednesday
1. Pull from codingnomads to incorporate the new change in README.md

$ git pull origin master

Pull from mingyyy to incorporate new changes in learned_concepts

$ git pull ming master

* There might be a vim window opens to ask for comments of the merge. 
* Change the comments or leave it (default), esc + :wq to continue

2. we can hide some files in .gitignore, so they won't be pushed to GitHub

3. compare the difference of TextEditors

**To get out of a system: Ctrl + v or Ctrl + c

Vim (emacs): *Access server directly, easy to use from Terminal.* 

Sublime Text (ATOM, VsCode): *More user friendly Text, editing, not a lot of functionalities. Can't enter user input.

Jupyter: *popular in DataScience, visualization, markdown files.

repl.it: *easy to put up a small piece of code and share the link with others, web-based

PyCharm: *have project structure, python consol, terminal and others 

*Alt + the line, so you can change all of them at once
*select something, right click, refactor and rename it

1. Change the apparence under Pycharm -> Preference
2. shift + shift: to search
3. alt + select same words in different lines, then all these can be changed
4. ctrl + shift + r, first time to run the program
5. ctrl + r, aftr running for the first time

### Thursday
1. chapter2 of the book, Variables and types

file extention is a way to tell the computer what to do with the file

.py - python file
.sh - bash file

*To comment on multiple lines -> select multiple lines and press **command + /

print(argument)- a function apply to any type, normally
'name = "ccc" - an instance of the string object
'name.title()- a method *title* will do someting to *name*, object of a **class

'my_list.append(3) - append method operate on the list instance *my_list*

*help(class.method) - give us the description of the method e.g. help(my_string.strip)

*print(class.method) - show the info of the method in the class

*select the method and then **command + B, shows the def of the method


### Friday

**iterables (if you can call for loop on it)**
1. list: same or different data type. 
2. range() is a class which is predefined.
3. string
4. generator: creats each itme on the go. don't need memory. 

**LIST**
1. slicing: first : defines where it starts and ends; second : defines the steps (-1) going backward
2. mutable, while tuples are not.
3. function sorted(mylist, reverse = True) which return the sorted list
4. method mylist.sort() returns nothing, however sorted permenantly

**Loop**
1. definite: 
2. indefinite:
