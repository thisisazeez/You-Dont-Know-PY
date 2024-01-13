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

### Lists
Lists are ordered sequences of elements. They can contain different data types and can be modified after creation. Lists are defined using square brackets [].

```py
numbers = [1, 2, 3, 4] 
fruits = ['apple', 'banana', 'mango']
```

Some common list methods:

- append(item) - adds item to end of list
- insert(index, item) - inserts item at given index
- remove(item) - removes first occurrence of item 
- pop(index) - removes and returns item at index
- index(item) - returns index of first occurrence of item
- sort() - sorts items in ascending order
- reverse() - reverses order of items
- copy() - returns shallow copy of list

```py
fruits.append('orange')
fruits.insert(1, 'grape') 
fruits.remove('mango')
```

### Dictionaries 
Dictionaries are unordered collections of key-value pairs. Dicts are defined using curly brackets {} and colons to separate keys and values.

```py
student = {
  'name': 'John',
  'age': 20,
  'courses': ['Math', 'Science']
}
```

Some useful dict methods:

- get(key) - returns value for key, or default if key doesn't exist
- update(dict2) - updates dict with key/values from dict2
- values() - returns dict values as list
- keys() - returns dict keys as list 
- items() - returns (key, value) tuples as list
- pop(key) - removes and returns value for key

```py
name = student.get('name')
student.update({'age': 21}) 
```

### Tuples
Tuples are ordered, immutable sequences of elements. They are defined using parentheses (). 

```py
point = (10, 20)
```

Tuples have only two methods:

- count(item) - returns number of occurrences 
- index(item) - returns index of first occurrence

Once defined, elements in a tuple cannot be changed.

### Sets
Sets are unordered collections of unique elements. They can be defined using curly brackets {} or the set() constructor.

```py 
colors = {'red', 'blue', 'green'}
numbers = set([1, 2, 3])
```

Some set methods:

- add(item) - adds item to set
- remove(item) - removes item from set
- union(set) - returns new set with all items from both
- intersection(set) - returns set with only common items
- difference(set) - returns set with items only in first set
- issubset(set) - returns True if all items in set are in other set

```py
colors.add('violet')
colors.remove('blue')
```

### Loops

Loops allow us to repeatedly execute blocks of code. Python has two main loop structures - the `for` loop and the `while` loop. 

The for loop iterates over iterable objects like lists, tuples, sets, etc:

```py
fruits = ['apple', 'banana', 'mango']

for fruit in fruits:
  print(fruit)
```

This loops through and prints each fruit in the list.

We can also loop through strings:

```py  
for letter in 'Python':
  print(letter) 
```

The while loop executes code while a condition is true:

```py
count = 0
while count < 5:
  print(count)
  count += 1 
```

This will print 0 to 4. The while loop continues running until count is no longer less than 5.

We can combine loops with other concepts like if statements:

```py
numbers = [1, 2, 3, 4, 5]

for number in numbers:
  if number % 2 == 0:
    print(number)
```

This will print only the even numbers. The % operator checks for remainder, so number % 2 == 0 checks if it's divisible by 2.

Break and continue statements can control loop execution:

- break - exits the current loop
- continue - skips to next iteration 

```py
for x in range(10):
  if x == 5:
    break
  print(x)
  
for x in range(10):
  if x % 2 != 0:
    continue
  print(x)  
```

While loops can also have an else block that runs if the loop finishes normally without hitting break:

```py
count = 0
while count < 5:
  print(count) 
  count += 1
else:
  print('count value reached 5')
```


### Objects and Classes

Everything in python is an object.

Objects in Python are created from classes, which are like blueprints for creating objects. 

We define a class using the class keyword:

```py
class Dog:

  # Class attribute
  species = 'mammal'   

  # Initializer / Instance attributes
  def __init__(self, name, age):
    self.name = name
    self.age = age
    
  # instance method
  def description(self):
    return "{} is {} years old".format(self.name, self.age)
  
  # instance method
  def speak(self, sound):
    return "{} says {}".format(self.name, sound) 

```

This Dog class has a class attribute species, and instance attributes name and age passed to the initializer. 

We can now create Dog objects by calling the class:

```py
buddy = Dog("Buddy", 9)
miles = Dog("Miles", 4)
```

This creates two Dog objects buddy and miles, each with their own name and age.

We can access the instance attributes:

```py
print(buddy.name) # Buddy
print(miles.age) # 4
```

And call instance methods:

```py 
print(buddy.description()) # Buddy is 9 years old
print(miles.speak("Woof Woof")) # Miles says Woof Woof
```