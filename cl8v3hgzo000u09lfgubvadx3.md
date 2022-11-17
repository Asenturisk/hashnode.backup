# Learn Python in 5 Minutes

## Introduction
Guido van Rossum created Python in the 1990s.
The name relates to his interest in the show Monty Python's Flying Circus rather than the snake.
It is an interpreted language than a compiled language, so all the work is done while the program is running. (And also why it is so slow!)

## Commenting
Comments are contextual 'notes' in a program, to provide some information about particular parts of a program. Comments are ignored by the compiler (runner) of the code.
- use # for single lines
- and ''' (3 speech marks) for multiple lines
```python
# this is a comment and has no effect on the program
this is not a comment and will cause syntax errors
'''
these are multiple lines of comments
easy, effective and perhaps even juvenile
'''
```

## Variables
Like algebra, they define values and store them.
certain rules apply to naming Python variables, however!
   1. Start with a letter (ABC) or an underscore (_ABC)
   2. NOT start with a number (123abc), (4good), (69chan)
   3. Are case-sensitive ('vName' and 'VName' are different)
   4. Supports only alphanumeric 
       characters and numbers

## Data Types
Traditional built-in data types for variables/objects include :
> **int** integers
```python
maxSize = 800
myNumber = 23
```
> **float** floating point numbers/decimals
```python
x_coordinate = 67.98
y_coordinate = 79.099812
```
> **str** string/text
```python
userName = "Dimitri"
current_status = "idle"
```
> **bool** Boolean logic
```python
isWarm = True
playerReady = False
lightSwitch01 = 1
mainEngine = 0
```

More built-in data types include :

- complex (complex numbers)
- list (Arrays, lists)
- tuple
- range
- dict (dictionaries)
- set
- frozenset
- bytes
- bytearray
- memoryview

You can also define your own CUSTOM data types such as

- LinkedList
- Tree
- LinkedTree
- DoublyLinkedList
- CircularList

etc.

## Data Conversion
You can convert between certain primitive data types
```python
# converting float to int
a = int(31.34) # returns 31
b = float(48) # returns 48.0
c = int("69420") # returns 69420
```

## Display Output
The simplest way is via `print()`
```python
print("My name is Jede Mortano")
```
You can use `input()` to assign input data to a variable
```python
print("What is your name?")
yourName = input("Enter : ")
```

## Escape Characters
In order to bypass the String's own boundaries, e.g. single speech marks or double quotes, you need to use special notation to mark them.
```python
# this line below will have errors
string1 = "Dolor's dollar is "gone" for good"
# this line below is the correct way to 'bypass' the speech marks
string2 = "Dolor's dollar is \"gone\" for good"
```
Sometimes the escape characters can be an efficient way to convey other functions and/or meanings.
```python
# printing separate lines in the normal way
print("A")
print("B")
print("C")

# printing separate lines in a single print statement
print("A \nB \nC")

# or also
print("""
A
B
C""")
```
In other words, escape characters are special 'signals' for Python to know that you want to intend some special action at a particular spot. Or, more simply, so that Python doesn't get confused. Here are some common escape characters and their purpose :
- \' (single quote)
- \" (double quote)
- \\ (backslash)
- \/ (forwardslash)
- \n (new line)
- \r (carriage return)
- \t (tab)
- \b (backspace)
- \f (form feed)

## First Program
Prints what to do, takes input from user and stores it as a variable. Prints the output as a greeting to the user.

The code:
```python
print("What is your name?")
yourName = input("Enter : ")
print("Hi " + yourName + "! Nice to meet you")
```
> Strings are seperated by a + or , to attach a variable to the print statement

The output (terminal):
```bash
What is your name?
Enter: Jede
Hi Jede! Nice to meet you
```

## Functions & Methods
In Python, there can be a set of instructions or a block of code that can perform a specific task. These can be in the form of functions or methods.

#### Functions
Declaration:
```python
def functionName(...):
....
```
Usage:
```
functionName(Object)
```

#### Methods
Declaration:
```python
def methodName(self, ...):
...
```
Usage:
```
Object.methodName()
```

## Logic (Conditionals)
Python uses a very simple if-else scheme of following logical and conditional statements.

```python
# Takes 2 integers as input
# Must convert to int since the raw data is a string
numA = int(input("Enter first number: "))
numB = int(input("Enter second number: "))
# logical comparison
# if SOMETHING happens: do this... blah blah blah
if numA > numB:
  print("The first number is larger")
# elseif (elif) SOMETHING happens: do that... blah
elif numA < numB:
  print("The second number is larger")
# else SOMETHING ELSE happens: do it, yeah... blah
else:
  print("The numbers are equal")
```

Sample output with random inputs:
```
============== RESTART ~
Enter first number: 12
Enter second number: 4
The first number is larger
>>>
============== RESTART ~
Enter first number: 5
Enter second number: 6
The second number is larger
>>>
============== RESTART ~
Enter first number: 39
Enter second number: 39
The numbers are equal
>>>
```

The program was run 3 times to demonstrate all the 3 possible outcomes. The number of possibilities (obviously) depends on the number of conditions and the ways things could've been different.

Boolean logic also applies to Python.

```python
# Takes in input from the user
userAge = int(input("Enter your age: "))
userInCollege = input("Are you in university? (y/n) ")

'''
the .lower() method is used for converting all text characters (letters) to lowercase. It's a built-in 'method' (a type of function) for Strings in the Python library (many preset programs).
'''
if userInCollege.lower() == "y":
  userInCollege = bool(1) # Sets this particular variable to a Boolean type
else:
  userInCollege = bool(0) # Sets this particular variable to a Boolean type

# Main conditionals for the outcomes
if userAge >= 18 and userInCollege == True:
  print("Good luck on your studies!")
elif userAge < 18 and userInCollege == True:
  print("You're too young to be in university!")
else:
  print("Enjoy your free time before joining college!")
```

Sample output with random inputs:
```
============== RESTART ~
Enter your age: 12
Are you in university? (y/n) n
Enjoy your free time before joining college!
>>>
============== RESTART ~
Enter your age: 20
Are you in university? (y/n) Y
Good luck on your studies!
>>>
============== RESTART ~
Enter your age: 9
Are you in university? (y/n) y
You're too young to be in university!
>>>
```

## Lists
In Python, a 'list' is an array of various objects. Can be either of the same data type or even different data types.

Example 1:
```python
myList = [] # defining a list
myList.append("23") # adding data to the list
myList.append("Hello")
myList.append("abc")
myList # just calling the list so that it returns its contents
```

Output:
```
['23', 'Hello', 'abc']
```

Example 2:
```python
list2 = [1,1,2,3]
list2.append(8)
list2.append("Fibonacci")
list2
```
Output:
```
[1, 1, 2, 3, 5, 8, Fibonacci]
```

Accessing data from lists:
```python
list2[0] # index 0, the first element of list2
list2[2] # index 2, the third element
list2[6] # index 6, the seventh element
```
Output:
```
1
2
'Fibonacci'
```

Lists have some built-in methods, e.g. `pop( )`, `append( )`, `remove( )` and also functions, e.g. `len( )`.

```python
list2.pop() # removes and returns the last element of the list
list2 # calling the list again to see what happened to it
print(len(list2)) # printing the length of the list
```
Output:
```
'Fibonacci'
[1, 1, 2, 3, 5, 8]
6
```

## Loops
For repetitive tasks, it is favorable to use loops in Python. Either 
for-loops (for a countable number of 'repeats'), or while-loops (for unknown/uncountable number of 'repeats').

#### 'While' loops

```python
# 'initialize' (freshen up and create) the variables
bankBalance = 5000
numOfCourses = 0
# output the test balance
print("Your bank balance is: ", bankBalance)

'''
a while-loop is useful here since we don't know how many times we
can take courses for the amount in the test bank balance
'''
# while-loop for undefined number of 'iterations' (repeat cycles)
while bankBalance > 0:
  numOfCourses = numOfCourses + 1 # adding a course each time
  bankBalance = bankBalance - 200 # deducting money each time, assuming 200 dollars for each course

# after calculation, the number of courses the user can afford is displayed
print("The number of courses you can afford is: ", numOfCourses)
```

Output:
```
Your bank balance is: 5000
The number of courses you can afford is: 25
```

#### 'For' loops
For-loops are easier, and can be used with a set 'limit' (range)
for the total number of 'iterations' (repeats/runs) that will occur.

```python
# simple declaration of a list
yourList = ['Subscribe', 'to', 'Code Crunchers', 'please']
# simple for-loop for as many 'steps' as there are in the list's range
for i in range(len(yourList)):
  print(yourList[i])
```
Output:
```
Subscribe
to
Code Crunchers
please
>>>
```

## Functions
```python
# an example function
def functionName():
  # what the function does
  return
'''
functions need to return back to the main part of the program it was running on, often also bringing an 'output' result or object with it
'''
```
Quick example of how a function works in Python:
```python
# in Python, by convention, constant variables are named in all capital letters
CONVERSION_RATE = 0.305

# a basic function that converts a given value in feet to metres
def convertToMetres(ft):
  metres = ft * CONVERSION_RATE
  return metres

# converting 23 ft to metres
convertToMetres(23) # simply running the function may not output anything
# so we add a print statement
print(convertToMetres(23))
```
Output:
```
7.015
```

## Classes & Objects
Basically, a Python class is a data type (or an object type). And an object is an 'instance' (example) of that particular class.

```python
class className:
  def __init__(self, field_1, field_2):
    self.field01 = field_1
    self.field02 = field_2
  def methodName(self):
    # does something
    return # because we gotta return something!
  def methodName2(self, a, b):
    resultName = a + b # whatever
    return resultName
  def getField01(self):
    return self.field01
  def getField02(self):
    return self.field02

myVariable = className(2,3)
print(myVariable.getField01())
print(myVariable.getField02())
print(myVariable.methodName2("kod","bell"))
```
Output:
```
2
3
kodbell
```

## Error Handling
Sometimes, you can expect some errors to show up on your program. So, to point out what went wrong (otherwise the program would just crash), use the try-except scheme (similar to if-else).

```python
print("Testing error handling \n\n")
try:
  newNumber = int(input("Enter a number : "))
except:
  print("You didn't enter a number!")
print("Response recorded")
``` 
Output with normal circumstance :
```
Testing error handling


Enter a number : 25
Response recorded
```
Output with an error :
```
Testing error handling


Enter a number : what
You didn't enter a number!
Response recorded
```

Ready to learn Python? Stay subscribed to [Code Crunchers](https://www.youtube.com/channel/UCn_QqSQyqyWE3fGogK0u3bA) on YouTube for more in-depth tutorials and lessons. Hopefully coming soon!