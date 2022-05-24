# Python basics

## Prerequisites
Before starting this course, you must have installed a code editor and Python itself.
I reccomend [Visual Studio Code](https://code.visualstudio.com/). Install it, and create a file ending `.py` to signify Python. You will be prompted to install the Python extension, do this.
Then you should be able to run code by pressing <kbd>F5</kbd>

## Hello world
It is convention in programming to create a so-called hello world program as your first program in any given language. This is a program that simply outputs the text "Hello world" to the user.

In Python, we can do this using just one line.
```py
print("Hello world")
```

Here we are using the print function. The parentheses that follow signify where the arguments, or input values to this function are placed. Witin these, we have a string of text.
This is a simple data type in Python that stores text. You create these by enclosing text in either `"` or `'`.
We are passing this argument to the print function that then proceeds to output this to the user.

## Variables
One basic concept of programming, is the usage of variables to store data. This is a named variable, that allows you to access a value stored at a later point in the program. In Python, you create variables simply by setting a name equal to some value. For instance:
```py
foo = "I am a variable"
bar = 64
foobar = 3.1415
```

You can change a variable's value the same way as you would create one.
```py
foo = "I have a value"
foo = "This is my new value"
```

### Data types
The data stored in a variable are of different types. Initially, there are some basic types you need to know.

#### Integer
Integers are whole numers. That is, numbers that do not have any decimals. These are written out using numerals. You can also use the `int` function to parse, or convert, another value, for instance a string or a float, to an integer.
```py
a = 128

# This takes 4 as text, and converts it to a number
b = int("4")

# Converting a number with decimals to an ineger, removes said decimals. Here, c will equal 3.
c = int(3.14159265)
```

#### Floating-point number
Floats are numbers with decimals. The name refers to the way these values are stored on the computer, which is not important, but you should know that the way they are stored could cause some mathematical errors.

Floats are written as a number with decimals. It is important to use `.` as the decimal separator. You can also parse values to float using the `float` function. If the number is zero point something, the zero can be omitted.
```py
pi = 3.14159
e = 2.71828
half = .5

# Converts 1.2 as text to a float
a = float("1.2")

# This is a common example of mathematical errors due to floating-points. 
# b will in fact be equal to 0.30000000000000004 after this operation, rather than 0.3 as it should.
b = .1 + .2
```

#### Booleans
A boolean is a data type that can only hold two different values, `True` or `False`. These are often the result of logical operations, as we will discuss later. These can be parsed using the `bool` function.
```py
yes = True
no = False

a = 1
# This checks whether a is equal to 1, which it is. b will then equal True.
b = a == 1

# Most values evaluate to True when parsed to bool.
p = bool(2)

# However, 0 does not.
n = bool(0)
```

#### String
A string is a data type that contains text. They are enclosed in `"` or `'`. You can parse other values to string by using the `str` function.
```py
a = "I am a string"

b = "I too am one"

# This converts the number 4 to text
c = str(4)
```

## Logic
Different logical operators, and the ability to do different things when different conditions are present is a crucial element of computer programming.

### Operators
Logical operators combine or compare values to create a boolean answer.

#### Equality
The `==` operators check whether two values are the same. Do note that this is not the same as `=`, which is the assignment operator, and cannot be used for comparisons.
Similarly to the equality operator, there is a not equal operator `!=`.
```py
a = 1
b = 1

# This will evaluate to True, as both are equal to 1
a == b

# This will evaulate to False, as a is not 2
a == 2

# However this will evaluate to True, as a is not 2, and that is what we are checking for here
a != 2
```

#### Inequalties
Python also has operators to check if values are less than, greater than, or any of the preceeding or equal to a value.

`<` is the less than operator, `>` the greater than operator, `<=` is less than, or equal to, `>=` is greater than or equal to.
These can be used between two values, or with three values, for example to check if a value is in a range.
```py
x = 3
y = 2
z = 2

# False
x < y
x <= y
z > 2

# True
y <= z
x > y
z < 3

# True, because x lies between 1 and 10
1 < x < 10
```

#### Logical operators
Python has three logical operators, `not`, `and` and `or`.
The `not` operator inverts a boolean value.
```py
# This is False
not True

# This is True, as 1 == 2 evaluates to False.
not (1 == 2)
```

The `and` operator checks whether two conditions are both True.
```py
# This is False
False and True

# This is True
True and True

# True
3 == 3 and 2 < 9

# False
4 < 7 and 2 < 1
```

The `or` operator checks whether at least one of the two conditions are True.
```py
# This is True
False or True

# This is True
True or True

# This is False
False or False

# True
3 == 3 or 2 < 9

# True
4 < 7 or 2 < 1
```

### If statements
If statements execute code only if a boolean statement is `True`. You write them on the format `ìf SOME_CONDITION:`. Then on the following lines, you must indent, using either tabs or spaces. You must use the same indent style for the entire file.
If the condition provided to an `if` is not `True`, it will continue to an `elif`, if present. This is short for "else if". This functions similarly to an `if`, but will only be run if the main condition is `False`.
Finally, if neither the `if` nor any `elif`s are `True`, an `else` block will be run.
```py
if True:
    print("This will be executed")

if False:
    print("This will never be executed")
else:
    print("This however, will")
	
if 1 == 2:
    print("One is not equal to two, and hence this is not executed")
elif: 2 == 1 + 1:
    print("Two is indeed the sum of one and one.")
```

## Mathematics
You can do calculations directly in Python by using mathematical operators and functions.

### Arithmetic operators
Python has the following arithmetic operators:

`+`: addition, finds the sum of two numbers.
`-`: subtraction, finds the diference between two numbers.
`*`: multiplication, finds the product of two numbers.
`/`: division, finds the quotient of two numbers. Note that this can result in a floating-point answer to a division of two integers.
`//`: integer division, finds the integer part of two numbers. `3 / 2 == 1.5`, but `3 // 2 == 1`, since 1 is the integer part of the quotient.
`%`: modulo, finds the remainder of an integer division. Eg. `3 % 2 == 1`, since you could divide three whole things into two piles of one each, and then have one remaining.
`**`: exponentiation, evaluates a number to the power of another.

### Assignment operators
All of the previously mentioned operators can be turnt into assignment operators by appending an `=`. This is an operator that performs the operation directly on a variable.

```py
a = 10

# This will increase a's value by 1
a += 1

# This will multiply a with two
a *= 2

b = 7

# Operators can be used with variables. a will now be 15
a -= b
```

### The math library
Python has a builtin library called `math` that contains many mathematical functions, such as `sqrt`, `sin` and `cos`.
Call these by importing `math` and prefixing their names by `math.`.
```py
import math

# This is 4.0
math.sqrt(16)
```

### String operators
Strings are not numbers, so using mathematical operators on them do not make as much sense. However there are two string operators.
`+`: concatenation, this combines the values of two strings. Eg. `"hello " + "world" == "hello world"`
`*`: multiplication, this repeats a string a number of times. Eg. `"a" * 10 == "aaaaaaaaaa"`

These can also be used as assignment operators.

## Loops
Loops are used in programming when you want something to be repeated a number of times. Python has two types of loops, `while` and `for`.

### While loops
While loops execute code while their boolean condition is `True`. If that condition is not changed from within the loop, this will execute indefinitely.

```py
i = 0
# This will repeat twice
while i < 2:
    print("hello")
    i += 1
    
# This will never complete
while True:
    print("hello")
```

### For loops
For loops execute for each element in a collection, or list. One common usage is to do something a given number of times.
```py
# The range function is a collection of the natural numbers strictly less than 10.
# This means it does not include 10, though it does include 0. This code will execute 10 times.
for i in range(10):
    print("This is iteration number: " + str(i))

# You can also iterate a list
for i in ["hello", "world"]:
    print(i)
   
# Strings are also iterable. Each time, you will have a new character
for i in "foobar":
    print(i)
```

### Break and continue
There are two keywords that can be used to control loops.
`break` exits a loop, and `continue` skips the current iteration and starts on the next one.

```py
# This will only print Hello twice.
for i in range(10):
    if i == 2:
        break
    print("Hello")

# This will skip printing "Hello 2"
for i in range(10):
    if i == 2:
        continue
    print("Hello " + str(i))
 ```
 
 
 
