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
elements with opening and close tags and content:
6 headings in total from h1 to h6, e.g. <h1>My First Heading</h1>
boxes inside boxes:

```
<!DOCTYPE html>
<html>
 <head> <title> this is my site </title> 
        <style> ....<style>
 </head>
  <body>
     <nevigation bar>
     <h1>My First Heading</h1>
     </nevigation bar>
     <section>
       <a href="http://codingnomads.co">codingnomads </>
     </section>
  <body>
</html>
```
short-hand to type unordered list of 4 lists (use **emmet)
```ul>li*4 tab```

**HTML basic tags

head:
body: only what's here will be displayed on the page
headings from h1 to h6 (smaller)
p: paragraph
a: link
div:division, a generic box
section:
table:

**different ways of establishing a connnection between user and server: webhooks, API, uscr

1. All HTML elements can have attributes
2. The *title* attribute provides additional "tool-tip" information
3. The *href* attribute provides address information for links
4. The *width* and *height* attributes provide size information for images
5. The *alt* attribute provides text for screen readers
6. The *<hr>* tag defines a thematic break in an HTML page, and is most often displayed as a horizontal rule.
7. With HTML, you cannot change the output by adding extra spaces or extra lines in your HTML code. The browser will remove any extra spaces and extra lines when the page is displayed:
8. Use *<br>* if you want a line break (a new line) without starting a new paragraph
9. The HTML *<pre>* element defines preformatted text. The text inside a *<pre>* element is displayed in a fixed-width font (usually Courier), and it preserves both spaces and line breaks
10. syntax for *style*: <tagname style="property:value;">

text formatting
```
<b> - Bold text
<strong> - Important text
<i> - Italic text
<em> - Emphasized text
<mark> - Marked text
<small> - Small text
<del> - Deleted text
<ins> - Inserted text
<sub> - Subscript text
<sup> - Superscript text
```

1. <q>
2. <blockquote>
3. The HTML <abbr> element defines an abbreviation or an acronym.
4. The HTML <address> element defines contact information (author/owner) of a document or an article.
The <address> element is usually displayed in italic. Most browsers will add a line break before and after the element.
5. The HTML <cite> element defines the title of a work. Browsers usually display <cite> elements in italic.
6. <bdo dir="rtl"> </bdo> overwrites the current text direction.
7. adding coments <!-- Write your comments here --> 
8. In HTML, a color can be specified as an RGB value, using this formula: rgb(red, green, blue)


CSS stands for Cascading Style Sheets.

The target attribute specifies where to open the linked document.

The target attribute can have one of the following values:

_blank - Opens the linked document in a new window or tab
_self - Opens the linked document in the same window/tab as it was clicked (this is default)
_parent - Opens the linked document in the parent frame
_top - Opens the linked document in the full body of the window
framename - Opens the linked document in a named frame

Create a Bookmark

First, create a bookmark with the id attribute
```<h2 id="C4">Chapter 4</h2>```
Then, add a link to the bookmark ("Jump to Chapter 4"), from within the same page:
```<a href="#C4">Jump to Chapter 4</a>```

The <map> tag defines an image-map. An image-map is an image with clickable areas.
  
Block level elements in HTML:
A block-level element always starts on a new line and takes up the full width available (stretches out to the left and right as far as it can).
```<address><article><aside><blockquote><canvas><dd><div><dl><dt><fieldset><figcaption><figure><footer><form><h1>-<h6><header><hr><li><main><nav><noscript><ol><p><pre><section><table><tfoot><ul><video>```

Inline elements in HTML:

An inline element does not start on a new line and only takes up as much width as necessary.
```<a><abbr><acronym><b><bdo><big><br><button><cite><code><dfn><em><i><img><input><kbd><label><map><object><output><q><samp><script><select><small><span><strong><sub><sup><textarea><time><tt><var>```
  
The <div> element is often used as a container for other HTML elements.
The <div> element has no required attributes, but style, class and id are common.
  
The <span> element is often used as a container for some text.
The <span> element has no required attributes, but style, class and id are common.
  
**Using The class Attribute**
The HTML class attribute is used to define equal styles for elements with the same class name.
So, all HTML elements with the same class attribute will have the same format and style.
**classname has no space, if there is space, class is taking in multiple classes. if in conflict the last one will prevail. becuase of cascading.**

**difference between class and id

An HTML element can only have one unique id that belongs to that single element, while a class name can be used by multiple elements.

### Tuesday
CSS and HTML are languages but not a programing language
bootstrap is a framework in CSS.

bootstrap(https://getbootstrap.com/docs/4.3/getting-started/download/) 
1.mobile-first responsive design
2.easy styling

some elements don't have closing tag: link, meta, img

To link a style.css: <link rel="stylesheet" href="style.css"> in side of <head> </head>

In CSS: start with a selector, followed by { } in side which property: value;
``` p{
       color:red;
}

.highlight{color:red;
}

hightlight > p {color:red;
}
```
address all the p child element in highlight class

Grid System Rules in Bootstrap:

Rows must be placed within a .container (fixed-width) or .container-fluid (full-width) for proper alignment and padding
Use rows to create horizontal groups of columns
Content should be placed within columns, and only columns may be immediate children of rows
Predefined classes like .row and .col-sm-4 are available for quickly making grid layouts
Columns create gutters (gaps between column content) via padding. That padding is offset in rows for the first and last column via negative margin on .rows
Grid columns are created by specifying the number of 12 available columns you wish to span. For example, three equal columns would use three .col-sm-4
Column widths are in percentage, so they are always fluid and sized relative to their parent element

### Wednesday

in firefox type: ```file:/// localhost/ = 127.0.0.1``` will direct to root directory
URL: Uniform Resource Locator
file://127.0.0.0 or 127.0.0.1
http:// hyper text transfer protocol
ftp:// 
domain name(address of the computer, the server you are connected to): e.g. www.google.com
then a path like "/home" for example is walking through a file system

***protocol://domain_name/path***

DNS: domain name system translate the name of the computer to an IP address (long numbers)

 ```ping www.wikipedia.org```
www.wikipedia.org (103.102.166.224): 56 data bytes


### Thursday
web scraping: download webpages
web crawling: going through links automatically
web parsing: after scraping, taking out info needed

4 common HTTP methods:
.get() : asking for something
.post() : handing over something and asking for something
.delete : get rid of something from the server
.put : editing things on the server (update)


### Friday
API: application programing interfaace.
In computer programming, an application programming interface is a set of subroutine definitions, communication protocols, and tools for building software.

from the website itself, a structured way to directly access the data. 
providing a interface with HTTP methods. 
REST is one of the standards, frame work that post some constraints

1.find API
2. read the docs
3. integrate with other script


## week 5
### Monday
Exam:
1. Web URL load a HTML file while API URL resource holding data: json, txt, ml
2. get post put delete
3. post is creating a resource
put is overwriting and changing things
4. map to common db actions to HTTP methods
post - create 
get - read 
put - update 
delete - delete 
5. always read the doc of the API.
6. ? starts a query, & separate the parameters, parameter = value

APIs
DB 
- SQL Alchemy (interact with database from python)
- SQL (Postgres)
- server (go to different places)

Slack API
1. get token
2. pip install slackclient
3. from slackclient import SlackClient
4. sc = SlackClinet(token)
5. calling methods to retrieve info: sc.api_call()

### Wednesday
SQL & RDBMS (i.e. MS Access, SQL Server, MySQL)
relational database Vs. non-relational database(mongoDB)
1. clear table structure Vs. documents
2. primary key

query return a result set. 
syntax
```
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);

UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;

DELETE FROM table_name WHERE condition;

CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    column3 datatype,
   ....
);

DROP TABLE Shippers;

ALTER TABLE table_name
ADD column_name datatype;
```

join & conditions
 ```
 SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
ORDER BY column_name(s);
```

making connection to the postgres DB, which sit on my PC.
```$ psql``` then we get out by \q 
```$ psql -U postgres``` look at the user: \du, or \?
\l: list of all the DB
\c dvdrental: connecting to a DB called dvdrental.
\dt: list of tables in the DB
\q: quit this ps command line
\?: help with the command line

```dvdrental=# SELECT ...```Inside the DB, we can make sql queries. 

  ### Thursday
  SQLAlchemy: with SQL database connecting to Python, abstraction layer on top of the DB
  postgres: varchar, serial, decimal
  
  ### Friday
  sandman2 + postman
  ```
  $ pip install sandman2
  $ sandman2ctl postgresql+psycopg2://Ming@localhost/<db_name>
  ```
  
  ## Week 6
  ### Monday
  
  MVC: model view (HTML, static pages/templates/styles) controler (code logics)
  *in Django: MTV(model template views) = MVC (model view controler)
  ORM: object relational mapper
  
  Mostly a backend frame work, make things run on the server-side; while front end run on the client-side.
  Lots of display related to FE. 
 
 Building different logics in different apps under one project. One project could have many apps.
 
 What do we want to do with LEARNING LOGS:
 1. log learning progress
 2. for multiple topics
 3. multiple entries for each topic
 
 Tbl1. Topics: id(primary key), topic, descr, date_added, 
 Tbl2. Entries: id(primary key), id_topic(foregin key), text, date_added
 
 db.sqlites3 is just a tile not an entire database.
 
 1. create a new project $mkdir learning_log and a virtual environment: $ python3 -m venv .env then activate it
 2. install Django package. $ pip install Django 
 3. create a requirements file: $ pip freeze > requirements.txt
 4. create a project in the current folder: $ django-admin startproject learning_log . (don't forget the dot in the end)
 5. hide secrets.py in .gitignore
 6. put inside .gitigore: 
 secrets.py
 venv
 .idea
 7. create the database file which holds the default files: $ python manage.py migrate
 8. simulate another server to connect with our computer: $ python manage.py runserver
 9. create a superuser: $ python manage.py createsuperuser
 10. now we can go into our website to login as superuser: http://127.0.0.1:8000/admin/
 11. Create a README.md file
 12. git init / git commit -m "initial commit to create learning_log"
 13. create a logs folder (a django app): $ python manage.py startapp logs
 14. create new classes in models.py, inheritates from models.Model
 ```
 class Post(models.Model):
      title = models.Charfield(max_length=200)
      text = models.Text()
      author = models.Charfield(max_length=100)
      date_added = models.DateTimeField(auto_now_add=True)
      
      def __str__(self):
          return self.title
 ```
      
 15. add ```"logs",``` inside INSTALLED_APPS under settings.py
 16.
 model.py go through makemigrations to create a file in migration folder: _itin_0001. (like a commit in github)
 $ python manage.py makemigrations
 take 0001 code translate to sql and put it in the database
 $ python manage.py migrate
 check the status of the migrate sql
 $ python manage.py sqlmigrate logs 0001
 17. register under admin our new models: admin.site.register(Topic)
 
 In Django, Meta is just used to pass information into the process of creating the _meta Options object. Django's Model class specifically handles having an attribute named Meta which is a class. It's not a general Python thing.
 https://docs.djangoproject.com/en/2.1/ref/models/options/
 
 
 enter into Django shell:
 $ python manage.py shell
 
 $ from logs.models import Topic, Entry
 $ topics = Topic.objects.all()
 $ for i in topics:
 $    print(i)
 
 exit from Django shell:
 $ exit()
 
 ### Tuesday
 1. learning_logs -> urls.py. Currently only have one path "admin/" in the file; list route URLs to views
 2. include ("logs/", "logs.urls")
 3. path("", views.index)
 4. index render()
 5. create a template folder inside logs, templates/base.html
 6. incoporate some logics
 
 URL => manage urls => app urls => function in views.py => template (html files)
 
 **In the latest version of Django, the default of defining the path is not regular expression anymore. So we need to change in the Django 2.xx if you have an older version.
 And the on_delete cascade is necessary now, before might not be. 
 
 
 ### Wednesday
 building forms
 1. create form.py in my app, define a new form class inheritate form ModelForm
 2. add a function in view
 3. add urls.py, set up the route for new page
 4. add html file
 
 ### JAVA
 unlike python it is a compile language.
 
 ### Thursday
 new entry
 user login/logout
 1. if DIRS has logs and users two apps and defined. 
 2. therefore, we have to define another folder under each template: e.g. logs/template/logs/base.html
 so we can call base.html in any app. 
 
 ### Friday
 Deployment
 
 Heruko Pssa
 1). download the heroku client package and install
 2). create a free account
 3). https://medium.com/@qazi/how-to-deploy-a-django-app-to-heroku-in-2018-the-easy-way-48a528d97f9c
 
 
 ## Week7
 ### Tuesday
 git branch -b <branch_name>
 
 git branch
 
 git checkout <branch_name>
 
 (master)$git merge <branch_name>
 this is taking <branch_name> into master branch 
 
 ### Friday
 
 STEP 1. clone - run locally - push to github
 
 1. create folder
 2. create a virtual environement: $ python3 -m venv .env
 3. activate .env: $ source .env/bin/activate
 4. clone from github: $ git clone https://github.com/martin-martin/django-twitter-clone.git
 5. $ cd django-twitter-clone
 6. $ pip install -r requirements.txt
 7. $ python djitter/manage.py migrate
 8. $ cd djitter
 9. $ python manage.py makemigrations djeet
 10. $ python manage.py makemigrations djeeterprofile
 11. migrate the DB: $ python manage.py migrate
 12. check if it's running in localhost: $ python manage.py runserver
 13. create github repository, and push to github.
 $ git add /commit/ add remote <your remote name> "github repository link "
 $ git push ming master

STEP 2. 
1. register an account with AWS.
2. login to AWS management console
3. Services -> EC2 -> Instances -> Launch Instance -> Ubuntu -> next until Configure Security Group: set Source=My IP
Add one more type: Custom TCP , port range = 8000, anywhere
Add one more type: HTTP, port range = 80, anywhere
750hour a month for one instance for free for only one year
port: 8080 development 8000; 22 secured shell
4. click: Launch
5. create new key pair
6. download the key pem.txt

wait for 15 mins

7. click on View Instances on the right down corner
8. change the name and click on Connect
9. In Terminal: 
$ deactivate
$ cd 
$ l
10. if there is no .ssh folder create  one, then move pem file inside
$ cd .ssh
$ mv ../Downloads/ming_bali.pem .  
11. change security owner read only: $ chmod 400 ming_bali.pem
12. when you are in .ssh folder, connect to server, based on DNS(domain name server) or server info given by AWS
$ ssh -i "ming_bali.pem" ubuntu@ec2-34-213-211-97.us-west-2.compute.amazonaws.com
13. when asked, type: yes
14. now we are at ubuntu@ip-172-31-24-209:~$
15. 



 
 

 
 
 


  
  
 
  





