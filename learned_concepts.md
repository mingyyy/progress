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

*to delete an empty folder *

$ rmdir <folder_name>

*to delete a file *

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

$ git branch -v

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
6. command + b, check definition (docstring)

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
2. range() is a class which is pre-defined. also a generator which creates a list of numbers on the fly. 
3. string
4. generator: creats each itme on the go. don't need memory. 

**LIST**
1. slicing: first : defines where it starts and ends; second : defines the steps (-1) going backward
2. mutable, while tuples are not.
3. function sorted(mylist, reverse = True) which return the sorted list
4. method mylist.sort() returns nothing, however sorted permenantly
5. index starts from 0

**Loop**
1. definite: 
2. indefinite:


## Week 2
### Monday
1. Git review
$ chsh *change shell

$ git remote add <name of the remote> <http://....>  
  *each remote (repository on github) has many branches and a master branch

$ gst (in zshell = git status)

we can put what we don't need ot push to github in *.gitignore file

$ git config --global * there are some configuration files in your pc holding information of your email and passport

$ history *shows the history of the command you used.

**git init** --> make changes --> **git add <file_name>** --> **git commit -m "commit message"** --> **git push <remote-name> master 

**git pull python-onsite everyday!
**git push crashcourse everyday! The crash course book

**git clone http://...** This will generate a folder automatically
*git branch -a 
*git branch -v
*git log

create a git branch and push to the branch
$ git push salt_remote caden_db_feature (what you are pushing: remote and branch name) 


2. tuples: lists immutable. using () to create a tuple. 

3. coding styles

4. IF statement:  elif and else are optionals.
```if x in string:
      ...
   elif condition:
   else:
```
   
5. comparison operators != <= >= == = 

6. arithmetic operators: % + - / * // **

7. short hand: -= += *= /=

8. boolean: and or not
True and True => True
True and False => False
True or False => True
False or False => False

9. is / is not: check the identity of the objects.
Aliasing: assign one list to another list. So the two lists are the same => *new_list is my_list* returns *True

ctrl t + rename: to rename all the variables in the file

10. membership operators: in / not in


### Tuesday
**eval()** is used to transfer the string to a variable!
strings starts with "_" is for private functions. so don't use it!

1. Dictionary
- why do we need a dictionary?
from a key to a value, quick look for something. A key has to be *unique* and of a *mutable* data type. So a list can't be a key. it's normally not ordered. can't have multiple value for one key. value can be another dictionary, any other immutable data structure. a value can't be empty.

search from key to value, but the other way around. value is not unique.

2. looping over dictionary
three methods:
1. .keys()
2. .values()
3. .items()

**There is no __name__ in dictionary, therefore not easy to find the name of a dictionary
dir() shows the names in strings in the namespace. Therefore can be used to find the name of the dictionaries in string.


3. While loop: Indefinite iteration 

if a list is not empty it is True, therefore can be used in While loop, as **While [1,3]:** 
when the list is empty, then the loop breaks.

use a flag to indicate
```flag = True
 while flag:
     ...
```

use a counter
``` counter = 1
    while counter <= 10:
        ...
        counter += 1
```

use a condition, e.g. when user input an "x", the while loop will stop
```
while input_user != "x":
  input_user = input("")
```

use *break* to jump out of a while loop
use *continue* to ignore what's after and go back to the loop to start again


### Wednesday
#### Function

1. if there is no *Return statement*, there will be a default "None"
2. if a variable is defined inside a function and not returned, it can't be used outside. 
3. if you just key in the name of the function, nothing happens becuase it's a defined function.
4. functionname.__call__() is functionname()

```
def my_func(parameter1, parameter2, etc):

    '''docstring'''
  
    something here
  
    return ....
```
parameter1 and parameter2 are positional argument
*args: a list with unknown length. also an optional arguments (* means create a list and collect key words)
**kwargs: a dictionary with unknown length. (** means create a dictionary and collect keywords)
There is a fixed way to pass the keywords arguments, key can't be expressions!

Recurssive. 

an empty list: l = [] has the value [], but bool(l) = False

**from** module_name **import** function_name/class_name **any name


### Thursday
OOP: object oriented programming
Attributes = qualities of a class, what it has.
Methods = how it behaves.

Normally a name of a class is started with a capital letter. 
**ANKI: revisit the subjects(space repetition) - flash cards
e.g. what's a method?

Module is a file with some code *.py 
For example: modules: random, math, time etc, are part of a standard library

1. dunder method. "__init__" takes the first argument "self" refers to the instance itself.
2. dot

__init__ method, set up the instances for the class itself. Hence, using self.attribute = attribute
In other methods, the user input should just be a user input.

### Friday

1. as soon as a subclass inherit from a super class. The instances of the superclass are available immediately. 
however as soon as an __init__ shows up in a sub class, it over-write the __init__ in superclass.

Therefore, any method in subclass with the same name of the method in superclass will over-write the method in superclass.

2. if a class A is using another class B, then to make sure A is working properly, we need to properly define/import class A

3. __repr__ is the representing what the class does

4.Comparing differen ways of copies.
*Aliasing* 
```
a = 1
b = a
b is a
```
This will return True. just referencing a, so changing b will change a as well. 

*shallow copy*: use class copy
```
a = [[0,1], [2,3]]
b = copy.copy(a)
a is b
```
This will return: False. a and b are stored in different places in memory.

If a was created by using another variable c = [0,1,2,3]; therefore changing c would change both a and b.
list.copy is a shollow copy as well

*DEEP copy*: for mutalbe objects
```
a = [[0,1], [2,3]]
b = copy.deepcopy(a)
a is b
```
The computer will just make the value of the a and b, cutting off the links to the previous objects. 

? making the class immutable


## Week 3
### Monday
1. file O/I
``` with open("file.txt", "r") as f:
        x = f.read
```
r = read, a = append, w = write, + = read and write, b = binary, x = creat a new file and open it for writing

2. error handler: exceptions
```raise Exception("your message here for the error!")
```
3. 
Successful situation: try -> else -> finally
Unsuccessful situation: try -> except -> finally
 
4. step into the function: *Command + B

5. import os (os stands for operating system)
- *os.getcwd()* returns the name of the current directory. cwd stands for “current working directory”.
- *os.path.abspath()* To find the absolute path to a file
- *os.path.exists()* checks whether a file or directory exists
- *os.path.isdir()* checks whether it’s a directory
- *os.path.isfile()* checks whether it’s a file
- *os.listdir(cwd)* returns a list of the files (and other directories) in the current directory
- *os.path.join* takes a directory and a file name and joins them into a complete path

6.The module **dbm** provides an interface for creating and updating database files.
```
import dbm
db = dbm.open('captions', 'c')
```
A limitation of dbm is that the keys and values have to be strings or bytes. If you try to use any other type, you get an error.

7. The **pickle** module can help. It translates almost any type of object into a string suitable for storage in a database, and then translates strings back into objects.
- pickle.dumps takes an object as a parameter and returns a string representation (dumps is short for “dump string”)
- pickle.loads (“load string”) reconstitutes the object

pickling and then unpickling has the same effect as copying the object

You can use pickle to store non-strings in a database

8. Pipes

Most operating systems provide a command-line interface, also known as a **shell**. Shells usually provide commands to navigate the file system and launch applications. Any program that you can launch from the shell can also be launched from Python using a **pipe object**, which represents a running program.


**Mark Directory as Source Root** solves the problem of importing

### Tuesday
Testing

TDD: Test Driven Development
1. Pseudocode
2. Write Tests
3. Write codes

Unit Test: similiar in Java, JavaScript ...

1. define a test file name it: "test_<filename>.py"
2. in test_<filename>.py file, 
```
import unittest
import <filename>
  
class Test<Filename>(unittest.TestCase):
   pass
```
3. def different test cases and write very descriptive names for each test cases, with (self).
4. use self.assertxxxxxxxxx to test what you intend to test.
5. run directly from the terminal command line: ```$ python -m unittest``` this runs ALL the unit test cases!
   
**main + tab** will produce ```if __name__ == '__main__': ```

```def setUp(self):``` set up something before every tests
```def tearDown(self):``` tear down something after every tests.

**Pdb**: adding ```breakpoint()```into .py files
Then look at the debugging.py file
```$ python debugging.py```

common command line for pdb:
    short	| long  | description
1. n	    | next  | executes the current line of code
2. s	    | step  | step inside of the function that is called on the current line
3. r	    | return|	execute until the current function's return statement
4. p	    | print |	print the variable's value
5. !<expr>|	      | execute python statements - acts just like a normal interpreter session
6. q	    | quit	| exit the python debugger
  
  
### Wednesday
1. Virtual Environtment
```
python3 --version
python3 -m venv <user_name>
.env cd bin
bin 1
cd ../..
pip freeze -l > requirements.txt 
```

alt + space: shows the photo in the folder
source .env/bin/activate
deactivate

This will give you a list of all the current environment variables present on your system. 
```printenv. ```

You can check out the variables' individual values using 
```echo $<VARNAME>```

You can add a new environment variable with the following command:
```export <NAME>=<VALUE>```
Attention: There should be no space on either side of the = sign!

Removing environment:
```unset <NAME>```

To use an environment inside Python, import the os libarary.
```
import os
secret = os.environ['MY_SUPER_SECRET_SECRET']
print(secret)
```

to make sure new VEVs(Virtual Environment Variables)are not stick arount. This code gets run everytime we deactivate our environment
```
deactivate () {
     unset MY_SUPER_SECRET_SECRET
     # lots of other code
}
```
2. Packages
```pip install <package name>
pip3 install <package name>
```




### Friday

*aggregators aggregate values within the function body, and return an aggregate value.e.g. sum of some numbers.
enumerate is an example of an aggregator.

1. A python in-built function .enumerate()
```enumerate(iterable, start=0)```
The enumerate() method adds counter to an iterable and returns it. The returned object is a enumerate object.

ctrl + g:  multi-select by clicking going to next variables.
2. list comprehension
replicate nested if statements with a list comprehension. check first if and then second if.
Nested loops can be used to perform multiple iterations in a lsit comprehension
```
my_list = [x * y for x in [20, 40, 60] for y in [2, 4, 6]]
print(my_list)

Output
[40, 80, 120, 80, 160, 240, 120, 240, 360]
```
3. generators

4. lambdas: lambda is the key word not the name of the funciton. 
lambda x, x1, x2... xn : f(x, x1, x2, x3... xn)

can't print or raise in a lambda.
Lambda expressions can be especially useful when they represent the input to another function. Good examples are python's *filter()*, *map()*, and *reduce()*
sort(key = lambda x: ...)
Note: A change in Python 3 makes  filter(), map() and reduce() return Generators instead of list objects.Thereforew, we need to explicitly convert it into a *list.

## Week4
### Monday
1. HTML:Hypertext(links) markup language, just a markup language rather than a programing language.
<div>....</div>
elements with opening and close tag:
<h1>My First Heading</h1>
boxes inside boxes:
```
<html>
  <body>
     <nevigation bar>
        <h1>My First Heading</h1>
     </nevigation bar>
     <section>
       <> </>
     </section>
     
  <body>
</html>
```

HTML basic tags
head:
body: only what's here will be displayed on the page
headings from h1 to h6 (smaller)
p: paragraph
a: link
div:division, a generic box
section:
table:

**different ways of establishing a connnection between user and server: webhooks, API, uscr


