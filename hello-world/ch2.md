# You Don't Know Python Yet
# Chapter 1: Control Flow, Functions, Lists and iteration!


### Control Flow
In Python, When you're dealing with booleans or expressions that returns a boolean explicitly, we can make decisions and define strategies depending on their `True` or `False`.

We can do so using `if` statement:

```py
condition = True

if condition == True:
    # Do something
```
If the condition is `True`, it's block gets executed. (A block is that part that is indented one level (4 spaces usually) on the right, the block can be formed by a single line, or multiple lines as well, and it ends when you move back to the previous indentation level).

In combination with `if` you can have an `else` block, which will be executed if the condition results to `False`.

Example:
```py
condition = True

if condition == True:
    print("Condition is True")
else:
    print("Condition is False")
```
And you can have different linked if checks with elif that's executed if the previous check was False:

```py
condition = True
name = "SifuSherif"

if condition == True:
    print("Condition is True")
elif name == "SifuSherif":
    print("Hello SifuSherif")
else:
    print("Condition is False")
```
In a if statement you can have just one if and else check, but multiple series of elif checks.

`if` and `else` can be used in an inline format:

```py
a = 2
result = 2 if a == 0 else 3
print(result) # 3

```

### Functions

Functions are reusable blocks of code that perform a specific task. They allow us to reuse code instead of writing the same thing over and over. 

To define a function in Python, we use the `def` keyword followed by the name of the function. Parameters go inside the parentheses. The code block goes under the function definition, indented by 4 spaces usually.

Example:

```py

def print_greeting(name):
    print("Hello " + name + ", how are you?")

```

To call or execute this function, we simply call it by name and pass a string argument for the name parameter:

```py  

print_greeting("Flavio")

```

This will print "Hello Flavio, how are you?". 

Functions can also return a value using the `return` keyword. The return value can be stored in a variable when calling the function:

```py
def get_square(num):
    result = num * num
    return result

squared_number = get_square(5) 

print(squared_number) # 25

```

Parameters allow us to pass different arguments to functions each time. There can be multiple parameters separated by commas:

```py

def full_name(first, last):
    print(first + " " + last)

full_name("Sifu", "Sherif") 

full_name("Flavio", "Copes")

```

Default values can also be defined for parameters:

```py

def greet(name, saying="Hello"):
    print(saying + " " + name)

greet("Flavio") # Hello Flavio

greet("SifuSherif", "Hi") # Hi SifuSherif

```
