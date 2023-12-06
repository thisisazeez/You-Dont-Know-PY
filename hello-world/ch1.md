# You Don't Know Python Yet
# Chapter 1: What *Are* Variables?

Just printing `hello world` is not enough, is it? You might later on want to take some input, manipulate it and get something out of it. We can achieve this in Python using constants, variables, etc and we'll learn some other concepts as well in this chapter.

## Variables
Variables are name-given containers found in many programming languages, not exclusive to Python. They serve as storage units for information, much like the human brain processes data from the eyes, nose, and ears. The scope of a variable determines where it can be accessed in the code either locally within a specific part or globally throughout the entire program. These containers hold values that can be manipulated or retrieved as needed.

In Python, we can create a new variable by assigning a value to a label using the `=` assignment operator.

```py

name = 'SifuSherif'

```

In this example we created a new variable called `name` and assigned a the value of `SifuSherif` to it.

```py

age = 12

```

In the above example we followed the same pattern as the first example but this time around using numbers as our value, which can be of various types such as integers, floats, strings, lists, etc.

However when declaring your variables they are certain name conventions that must be followed like using composed characters, numbers and utilizing the `_` underscore character all of these are **Valid** variable names. For example: 

```py
name1
AgE
_user
11booth
super_user
```
Now, **Invalid** Variable conventions:

```py
123
test!
user%
```
Other than that, anything can be used except it is a Python **Keyword**. Some of the Python Keywords are as follows:

```py
for
while
def
import
if
else
```
Python will automatically alert you if you use one of these as a variable, you will gradually start to recognize them as part of the python syntax paradigm. So no need to memorize them.

## Expressions and Statements

In Python, you can express a wide variety of code that returns a value. It is a versatile language that allows you to create diverse expressions because it supports various data types, operations, functions and libraries. For example:

```py
test_result = 3 + 5 * 2 / 4
```

A statement on the other hand is an instruction the the Python Interpreter can execute. Each statement is on it's own line, but utilizing a semicolon allows you to have more than one statement in a single line. For example:

```py
# 2 Statements
social = "x.com/sifusherif"
print(social)

# more than one statement on a single line
social = "x.com/sifusherif"; print(social)
```

## Comments

In Python, any text to the right of the `#` symbol is completely ignored, and considered a comment. Comments can be used to deliver message to the reader of your program. For example:

```py
# Commented line

social = "x.com/sifusherif" # Inline Comments
```

## Indentation

In Python, indentation plays a crucial role. Unlike some languages that do not assign meaning to whitespaces, Python relies heavily on proper indentation. Even with flawless code, a single indentation error can have serious **consequences**. Typically, a standard practice is to use four spaces for each indentation level in your script. For example:

```py
# Correct indentation
if True:
    print("This block is properly indented.")

# Incorrect indentation
if True:
print("This will result in an indentation error.")
```

## Data Types

In Python, we have several built-in data types. For instance, when we created a variable called `social` and assigned it the value "x.com/sifusherif," this variable became a `String` data type. You can determine the type of a variable using the `type()` function by providing the variable as an argument. For example:

```py
# Creating a variable
social = "x.com/sifusherif"

# Checking the data type
data_type = type(social)

# Displaying the result
print(f"The data type of 'social' variable is: {data_type}")
```

We used `str` class in our example but the same applies to other data types.

Firstly, we have numbers. Integers are represented by the `int` class, while floating-point numbers (fractions) belong to the `float` type. For example:

```py
# Integer example
integer_number = 42

# Floating-point example
float_number = 3.14
```

You can also check the data type for these variables:

```py
# Checking the data types
type_of_integer = type(integer_number)
type_of_float = type(float_number)

# Displaying the results
print(f"The data type of 'integer_number' is: {type_of_integer}")
print(f"The data type of 'float_number' is: {type_of_float}")
```
You can also create a variable of a specific type by utilizing the class constructor and passing the value literal. For example:

```py
age = int(22) # Using the int contructor to create an integer.

ratings = float(0.1) # Using the float constructor to create a fraction.
```

### Casting

You can also convert from one type to the other by using the class constructor. Python will attempt to determine the correct value. For example:

```py
# Converting an integer to float

age = 32
floatingAge = float(age) # 32.0

# Converting float to integer

ratings = 2.1
badFood = int(ratings) # 2
```

Ofcouse, those are just basics of types. We have alot more types in Python:

```py
# Some Of Python Data Types.

# 1. int
x = 10

# 2. float
y = 3.14

# 3. str (string)
social = "x.com/sifusherif"

# 4. bool (boolean)
is_learning = True

# 5. list
numbers = [1, 2, 3, 4]

# 6. tuple
coordinates = (3, 4)

# 7. dict (dictionary)
person = {'name': 'SifuSherif', 'age': 30}

# 8. set
unique_numbers = {1, 2, 3, 4}

# 9. complex
complex_number = 2 + 3j

# 10. bytes
byte_data = b'learning'
```
and more!

## Python Operators

In Python, Operators allows us to perform common operations on variables. They are the special symbols that can manipulate the values of one or more operands.

List of Python Operators

* Assignment Operators
* Arithmetic Operators
* Logical Operators
* Bitwise Operators
* Comparison Operators
* is and in Operators

### Assignment Operators

This includes the basic assignment operator equal to sign (=) used to assign a value to a variable.

```py
name = "SifuSherif"


# Also you can assign a variable value to another variable:

speed = 3
anotherSpeed = speed
```

