# Notes #1
### Introduction to Course
Robotics compose of many engineering disciplines including Mechanical, Electrical, Computer and Software Engineering. If a robot does not have the adequate mechanical design, it could potentially break on impact/load or may not have the capabilities to complete a task. Electrical design is also very important as it determines what actuators a robot is capable of using. The computer is also important as this is the brains of the robot and houses the instructions which the robot will follow. 
These instructions is the software.  Without the software, your robot would have no way of completing tasks by itself. Mastering the software of your system is essential to the intelligence and autonomity of your platform. 
The material covered in this lab class will allow you to develop this intelligence using the Python programming language and also leveraging a robotics software framework known as ROS. In this lab we will specifically be learning about Python.


### What is Programming?
Programming is the process of creating a set of instructions that tell a computer how to perform a task. Programming can be done using a variety of computer programming languages, such as JavaScript, Python, and C++.

### What is a Computer?
All computers -- whether we are talking about a personal desktop computer or a large mainframe computer or a microcontroller -- have several things in common:

- All computers have a CPU (central processing unit) that executes programs. If you are sitting at a desktop computer right now reading this article, the CPU in that machine is executing a program that implements the Web browser that is displaying this page.
- The CPU loads the program from somewhere. On your desktop machine, the browser program is loaded from the hard disk.
- The computer has some RAM (random-access memory) where it can store "variables."
- And the computer has some input and output devices so it can talk to people. On your desktop machine, the keyboard and mouse are input devices and the monitor and printer are output devices. A hard disk is an I/O device -- it handles both input and output.
	
The desktop computer you are using is a "general purpose computer" that can run any of thousands of programs. Microcontrollers are "special purpose computers." Microcontrollers do one thing well. There are a number of other common characteristics that define microcontrollers. If a computer matches a majority of these characteristics, then you can call it a "microcontroller".

Taken From: [Microcontrollers: How stuff work](https://electronics.howstuffworks.com/microcontroller1.htm#:~:text=A%20microcontroller%20is%20a%20computer,have%20several%20things%20in%20common%3A&text=On%20your%20desktop%20machine%2C%20the%20keyboard%20and%20mouse%20are%20input,and%20printer%20are%20output%20devices.)

### Interpreted vs Compiled vs Markup Languages
Python code is interpreted. Interpreted code goes through line by line. At the very beginning it goes through all the words for syntactical errors and function names etc etc. But the problem with this is you could have logical code within function that is not seen unless you are executing something.

Compiled languages tend to have higher performance than interpreted ones, since compiling precludes the need for a runtime interpreter.

Usually a programming is someone who is coding an interpreted or compiled language.

How do you decide on what language to use? This is highly dependent on the application.
- do you care about optimizing speed and space?
- is this for a website?
- is there special hardware required?

### Quick History of Python
Python was created in the late 1980s and was first used around December 1989 by its inventor Guido van Rossum in the Netherlands.
It wasn't until 1991 that Python was released to the public.

### Installing Python
You could download python on any general purpose computer however important to note that python comes with Mac and Linux OS. Mac and Linux OS are built on top of the UNIX operating systems. Installation creates a python path. 

Because python requires an interpreter, generally speaking, you can not use Python on a microcontroller. Instead you need to use language which could be compiled for specific microcontroller hardware.

### Operating Systems
One of the first operating systems is UNIX. 
Windows, MacOS and Linux are the three most popular operating systems used today. 
MacOS and Linux is built on top of UNIX. Windows is unique to itself.
The terminal also known as a shell is a user interface for access to an operating system's services and files/directories.

### Python Path
What does Python do when you run the code? Where does it find the print keyword/function? The Python Path is the path of where Python and all of your Python Packages have been installed.

### Writing Python Code
Requires for you to have a text editor or Integrated Development Environment(IDE).
IDE's have nice to have features for example auto-complete, connecting to database and servers etc. IDEs usually have a button to run code.
In order to write python code you need to write this in a python file. A python file has an extension of `.py`.

### Executing/Running Python Code
A text editor or IDE sometimes come with buttons to click in order to run your files. An IDE's button to run code is using the command line tool up above to run the python code.
If you would like to run your python code from your terminal/command prompt, you would move to the directory of your python file and execute the command `python name_of_file.py`.

### Python Interactive Console
This is a unique feature to python (and some other languages). It is a great tool that allows you to writing single executable Python commands and receive an output right away. It is basically a command line interpreter that takes input from the user, one command at a time and interprets it.

### Writing your first Python script: "Hello World" with Python
```python
print("Hello World, Waseem!")
```
`print()` is a built in Python function that takes in whatever you pass to it and returns it on the screen.

### Writing your second Python script
```python
my_message = raw_input("What is your message? ")
print(my_message)
````
`raw_input()` is another built in Python function that takes in what ever you type and pass/store it into a variable.

### Python Easter Egg
Python comes with a little Easter egg.
Take a look at what happens when you run the following command in a Python Shell:
``` python
>>> import this
```

The Zen of Python, by Tim Peters
> Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!


### Two versions
python2.7 and python3.5. Python 2.7 is more sustainable however Python3.5

### Variables and Storing Data
EDIT THE NOTES BELOW:
```
\# single line comment

"""

this is a multiline

comment made by

W.Hussain

"""

  

\# print is a built in python function

print('Waseem')

print('hello')

  

\# defining a variable as a string

name = "This is Waseem's class"

print(name)

  

import this

  

input - built in function

you dont need to declare variable data types

age = input('What is your age? ')

print(type(age))

  

age = int(age)

print(age)

print(type(age))

print(age \* 5 + 2 - 100)

  

Concatenation is the process of appending one string to the end of another string.

  

statically typed languages

int age = 5;

type variable\_name = 5

  

dynamically typed language
```

#### Numbers
Python supports many types of numbers. The two that we will mostly be using are integers and floating point numbers.
```python
my_num = 19
print(my_num)
```

```python
my_num = 7.0
print(my_num)
my_num = float(7)
print(my_num)
```

Above code is also using type casting! Type Casting is when you can convert an expression of a given type into another type. 
To cast an integer to a float you use a python built in function known as `float()`.

snake_case, kebab case and camel case
variable names are not allowed to start with a number

#### Strings
Storing characters in a variable.
```python
my_message = "Hello World, Waseem!"
print(my_message)
```

A string can be defined either with a single quote or a double quotes.
The difference between the two is that using double quotes makes it easy to include apostrophes (whereas these would terminate the string if using single quotes)
```python
my_string = "Don't worry about apostrophes"
print(my_string)
```

#### Booleans
True or False
```python
my_bool = True
print(my_bool)
```

#### Lists
An ordered collection of data. It is a best practice to keep all data in the list to be the same data type however it doesn't have to be. Lists can also be understood as arrays. They can contain any type of variable, and they can contain as many variables as you wish. Lists can are known for being iterated over.
Separate with comma. represented by open and closed bracket
```python
my_list = [1,2,3]
print(my_list[10])
```

range(start, end, step) --> returns a list
access data from list with index

For loop with a list of values
```
\# for your\_variable in some\_list:

\# use your\_variable
```

Slicing

```
\# students\_list.append("Tatiana")

\# students\_list.append("John")

\# students\_list.remove("Joshua")

\# students\_list.pop()

  

\# print(len(students\_list))
```


#### Dictionaries
An unordered collection of data that follows a key value paradigm. You access data from a dictionary by knowing the key in order to get to the value.

The first example is by first starting with an empty dictionary, then adding key value pairs.
```python
phonebook = {}
phonebook["John"] = 938477566
phonebook["Jack"] = 938377264
phonebook["Jill"] = 947662781
```

This example is create a dictionary with key value pairs already.
```python
phonebook = {
    "John" : 938477566,
    "Jack" : 938377264,
    "Jill" : 947662781
}
```

You can remove values from a dictionary, access or update them.

#### Other Built in Python Functions 
`type()` and `isinstance()`

#### Indexing to Access Data
You can index strings and lists.

Strings are immutable. What does it mean to be immutable? You can't do operations to a string and change the string. In order to change a string you must reassign it to the same string variable.
```python
my_string = "Don't worry about apostrophes"
print(my_string[0:11] + " there is always next semester")
```

#### Operators
#### Operations on Numbers - Integers and Float
Addition: `+`
Subtraction: `-`
Multiplication: `*`
Division: `/`
Floor Division: `//`
Modulus: `%` 
Divmod: `divmod(x, y)`

#### DRY Code
DRY stands for Don't Repeat Yourself. It is a best practice to group logic and functionality together into functions and classes, so that you are not repeating code in multiple places.

#### Functions
Functions in programming allow you to bundle a set of instructions and code. Functions are written usually to carry out a specific task. 

To do this task, a function might need multiple inputs (or no inputs), may need to call other functions, may need to return multiple values (or maybe return nothing). Functions are flexible and defined by the programmer. 
Important to remember you must declare a function first, then use it. If a function is just declared, the code won't be executed.

unlimited number of variables
local and global variables

#### Functions vs Methods
A method refers to a function which is part of a class. 
You can access this method only with an instance or object of the class. 

#### Classes
A `Class` is the bases of an object oriented programming language. The concept allows you to create abstract **templates** for creating objects. These classes can be provided initial values for state and implementations of behavior in methods.
Example:
```python
class RobotController:
	def __init__(self, ip_address, name)
		self.connected = False
		self.connect(ip_address)
		self.name = name
	
	def connect(self, ip_address):
		if len(ip_address.split(".")) == 4:
			self.connected = True
		else:
			print("Inputted incorrect IP address format")
	
	def move_forward():
		print("Moving Forward")
```
Example of a class implantation:
- You have the class `Vehicle`. This template contains all the logic which a vehicle will use to be created and used. For example it can have the **attributes** **and**  **properties**  `make`, `year` etc. It may contain the method `move_forward`, `turn_wheel`etc.

#### Things to Remember with a Class
Using the class above `RobotController` I can instantiate an object of the class.
```python
robot_a = RobotController(ip_address="0.1.2.5", name="My Robot Friend")
robot_a.move_forward()
```

The __init__ method is the constructor. The constructor are parameters you must pass to the class in order to instantiate an object.

After creating the object I have access to all methods in the class. For example the `move_forward` method.

You also have access to all variables and attributes that start with `self.`
These attributes are global to the class and can be used anywhere within the class and can be called outside of the class. WIth that being said, with `robot_a`, I could call call on `robot_a.connected` or `robot_a.name`.

Important to mention. If there was a method in the class call `connected` and a variable name `connected`, the way you distinguish between the two is that the method would be called like this: `connected()` and the attribute would just be `connected`.

If you are interested in further your understanding of Python and OOP Concepts, take a look at:
- Inheritance
- Polymorphism
- Encapsulation

#### Naming Conventions for Python
These naming conventions are following pep8 formatting.
Reminder, these are not rules that break your code if not implemented incorrectly Instead they help keep you maintain a convention to keep your code clean, easy to read and to share with others who follow the same convention.

When defining a class we use the `PascalCase` 
This is when the first letter of each word in a compound word (containing more then one word) is capitalized.
Example:
```python
class GroundRobotTool():
	def ..
```

When naming functions/methods or attributes, we use `snake case`.
Snake case has letters all lowercase and separate words with an underscore `_`.
Example:
```python
def add_two_nums(a, b):
	return a + b
	
robot_user_name = "Bob"
robot_length = 39
robot_width = 10
```

### Space/Time Complexity - Big O
A way to determine how optimal and efficient your solution/algorithm.
You always to design an algorithm in a way which that takes up the least amount of space and takes the least amount of time.

Long story short: Always think of space and time.