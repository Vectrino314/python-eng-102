# ENGR 102 - Engineering Lab I: Computation
## Comprehensive Study Guide for Exam 1

### Introduction
This study guide covers essential concepts from ENGR 102, focusing on programming fundamentals, algorithmic thinking, and Python basics that will be assessed in Exam 1. This guide combines information from course lectures, PowerPoint slides, and lab materials.

---

## Variables and Names

### Basic Concepts
- Variables hold information that you assign to them (like a number, text, or boolean value)
- Each variable needs a distinctive name to identify it

### Naming Rules
- Names can start with a letter (lowercase or uppercase) or an underscore (_)
  - Generally avoid starting with underscore as it implies special meaning in Python
- Names can contain letters, numbers, and underscore characters
- Names cannot be reserved keywords (like `for`, `while`, `if`, etc.)
- Best practices:
  - Use descriptive names (`volume` is better than `v`)
  - Keep names reasonably short (`v_sphere` is better than `volume_of_the_sphere`)
  - Constants often use ALL_CAPITALS
  - Variables `i`, `j`, and `k` are commonly used for counting or indexing
  - Regular variables typically start with lowercase letters

### Assignment
- Process of storing a value in a variable is called assignment
- Format: `variable_name = value`
- Can assign and reassign values to variables multiple times

```python
# Simple assignment
age = 19

# Multiple assignment
x, y, z = 10, 20, 30

# Reassigning variables
age = 20  # age now contains 20 instead of 19
```

### Assignment Shorthand Operators
- `i = i + 1` can be written as `i += 1`
- Other shorthand operators:
  - Subtraction: `-=`
  - Multiplication: `*=`
  - Division: `/=`
  - Modulo Division: `%=`
  - Exponent: `**=`
  - Integer Division: `//=`

```python
# Long form vs. shorthand
count = 5
count = count + 3  # count is now 8

# Same operation with shorthand
count = 5
count += 3  # count is now 8

# Other examples
total = 10
total *= 2    # total is now 20 (10 * 2)
total -= 5    # total is now 15 (20 - 5)
total /= 3    # total is now 5.0 (15 / 3)
total //= 2   # total is now 2.0 (floor division of 5.0 / 2)
```

---

## Data Types

### Integers
- Whole numbers without decimal points
- Can be positive or negative
- Examples: `1`, `2`, `100`, `0`, `-20`

```python
age = 21
count = -5
zero = 0
```

### Floating-Point Numbers
- Numbers with decimal points
- Examples: `1.01`, `2.0`, `100.0`, `-20.05`, `0.004`

```python
pi = 3.14159
temperature = -2.5
calculation = 0.0
```

### Booleans
- Can only have values `True` or `False`
- `True` is equivalent to `1`
- `False` is equivalent to `0`
- `bool(any_non_zero_or_non_empty_value)` evaluates to `True`
- `bool()` or `bool(0)` or `bool("")` evaluates to `False`

```python
is_valid = True
has_errors = False
print(bool(5))        # Prints: True
print(bool(0))        # Prints: False
print(bool("Hello"))  # Prints: True
print(bool(""))       # Prints: False
```

### Strings
- Text enclosed in single quotes (`'text'`) or double quotes (`"text"`)
- Used to represent textual data

```python
name = "John Doe"
message = 'Hello, World!'
empty_string = ""
```

### Type Conversion
- Convert between types using functions:
  - `int()`: Convert to integer
  - `float()`: Convert to floating-point number
  - `bool()`: Convert to boolean
  - `str()`: Convert to string
- Examples:

```python
# String to integer
num_str = "42"
num_int = int(num_str)      # num_int is 42

# Integer to float
num_int = 42
num_float = float(num_int)  # num_float is 42.0

# Float to integer (truncates decimal part)
pi = 3.14159
pi_int = int(pi)            # pi_int is 3

# Number to string
num = 123
num_str = str(num)          # num_str is "123"

# Boolean conversions
print(bool(42))             # True
print(bool(""))             # False
print(int(True))            # 1
print(int(False))           # 0
```

---

## Mathematical Operations

### Order of Operations (BODMAS)
- B - Brackets
- O - Orders (powers/indices or roots)
- D - Division
- M - Multiplication
- A - Addition
- S - Subtraction

### Basic Operations
- Addition: `+`
- Subtraction: `-`
- Multiplication: `*`
- Division: `/`
- Integer Division (division without remainder): `//`
- Modulus (remainder from division): `%`
- Power: `**`

```python
# Addition and subtraction
result = 5 + 3 - 2    # result is 6

# Multiplication and division
result = 4 * 5 / 2    # result is 10.0

# Integer division
result = 7 // 3       # result is 2 (not 2.33...)

# Modulus (remainder)
result = 7 % 3        # result is 1 (remainder of 7/3)

# Exponentiation
result = 2 ** 3       # result is 8 (2 raised to power 3)

# Order of operations
result = 2 + 3 * 4    # result is 14 (not 20)
result = (2 + 3) * 4  # result is 20
```

### Trigonometric Functions (in radians)
- Import math module: `import math`
- `math.cos(x)`, `math.sin(x)`, `math.tan(x)`
- `math.acos(x)`, `math.asin(x)`, `math.atan(x)`
- Note: These use radians, not degrees
- Convert: `degrees = radians * (180/math.pi)`

```python
import math

# Trigonometric functions (in radians)
sine = math.sin(math.pi/2)        # sine is 1.0
cosine = math.cos(0)              # cosine is 1.0
tangent = math.tan(math.pi/4)     # tangent is 1.0

# Convert radians to degrees
angle_rad = math.pi/2
angle_deg = angle_rad * (180/math.pi)  # angle_deg is 90.0

# Convert degrees to radians
angle_deg = 45
angle_rad = angle_deg * (math.pi/180)  # angle_rad is pi/4
```

### Other Mathematical Functions
- Import math module: `import math`
- Square root: `math.sqrt(x)`
- Logarithm: `math.log(x)` or `math.log10(x)`
- Exponential: `math.exp(x)` (equivalent to `e**x`)

```python
import math

# Square root
result = math.sqrt(25)    # result is 5.0

# Natural logarithm (base e)
result = math.log(math.e) # result is 1.0

# Base-10 logarithm
result = math.log10(100)  # result is 2.0

# Exponential (e^x)
result = math.exp(2)      # result is e² ≈ 7.389...

# Constants
pi_value = math.pi        # pi_value is approximately 3.14159...
e_value = math.e          # e_value is approximately 2.71828...
```

---

## Operators

### Relational Operators
- Equality: `==` (not `=`, which is for assignment)
- Inequality: `!=`
- Less Than: `<`
- Greater Than: `>`
- Less Than or Equal To: `<=`
- Greater Than or Equal To: `>=`
- Result is a boolean value (`True` or `False`)

```python
# Equality
print(5 == 5)       # True
print("abc" == "abc") # True
print(5 == 6)       # False

# Inequality
print(5 != 6)       # True
print(5 != 5)       # False

# Comparison
print(5 < 10)       # True
print(5 > 10)       # False
print(5 <= 5)       # True
print(5 >= 10)      # False

# Common mistake: assignment vs. equality
x = 5               # Assignment
print(x == 5)       # Equality check (True)
```

### Logical Operators
- `not`: Negation (flips `True` to `False` or vice versa)
- `and`: Conjunction (returns `True` if all operands are `True`)
- `or`: Disjunction (returns `True` if any operand is `True`)
- Order of operations: `not` → `and` → `or`

```python
# Logical NOT
print(not True)      # False
print(not False)     # True
print(not (5 > 3))   # False

# Logical AND
print(True and True)   # True
print(True and False)  # False
print(False and True)  # False
print(False and False) # False
print(5 > 3 and 10 < 20) # True

# Logical OR
print(True or True)    # True
print(True or False)   # True
print(False or True)   # True
print(False or False)  # False
print(5 > 10 or 4 == 4) # True

# Order of operations
print(not True or True and False)  # False
# Equivalent to: (not True) or (True and False)
# Equivalent to: False or False
# Result: False
```

---

## Input and Output

### Print Statement
- Basic syntax: `print(value1, value2, ...)`
- Multiple values are separated by commas
- Examples:

```python
# Basic print
print("Hello, World!")           # Output: Hello, World!

# Multiple values
print(2.0, 'is', 2)              # Output: 2.0 is 2

# Using f-strings (formatted strings)
name = "Alice"
age = 25
print(f"{name} is {age} years old")  # Output: Alice is 25 years old

# String concatenation with +
x = 3
y = 4
print(str(x) + ':' + str(y))     # Output: 3:4

# Print with custom separator
print("apple", "banana", "cherry", sep=", ")  # Output: apple, banana, cherry

# Print without newline
print("Hello", end=" ")
print("World")                   # Output: Hello World
```

### String Formatting
- Justification:
  - `"text".ljust(10)` - Left justify in 10 characters
  - `"text".rjust(10)` - Right justify in 10 characters
  - `"text".center(10)` - Center in 10 characters

```python
# String justification
print("2.3".ljust(10) + "|")   # Output: "2.3       |"
print("2.3".rjust(10) + "|")   # Output: "       2.3|"
print("2.3".center(10) + "|")  # Output: "    2.3   |"

# Formatting with f-strings
name = "Alice"
print(f"|{name:<10}|")  # Left aligned: |Alice     |
print(f"|{name:>10}|")  # Right aligned: |     Alice|
print(f"|{name:^10}|")  # Center aligned: |  Alice   |

# Number formatting
pi = 3.14159
print(f"Pi is approximately {pi:.2f}")  # Output: Pi is approximately 3.14
```

- Escape characters:
  - `\'` or `\"` - Quotes within strings
  - `\\` - Backslash
  - `\n` - New line
  - `\t` - Tab
  - `\b` - Backspace

```python
# Escape characters
print("She said, \"Hello!\"")         # Output: She said, "Hello!"
print('It\'s a beautiful day')        # Output: It's a beautiful day
print("First line\nSecond line")      # Output: First line (newline) Second line
print("Name:\tJohn")                  # Output: Name:    John
print("C:\\Users\\John")              # Output: C:\Users\John
```

### Input Function
- Basic syntax: `input(prompt)`
- All input comes in as a string
- Convert as needed:

```python
# Basic input
name = input("Enter your name: ")
print(f"Hello, {name}!")

# Converting input to numbers
age_str = input("Enter your age: ")
age = int(age_str)
print(f"In 5 years, you will be {age + 5} years old.")

# One-line input and conversion
height = float(input("Enter your height in meters: "))
print(f"Your height is {height * 100} centimeters.")

# Error handling for invalid input
try:
    number = int(input("Enter a number: "))
    print(f"You entered: {number}")
except ValueError:
    print("That was not a valid number!")
```

---

## Python Conditional Statements

The `if`, `elif`, `else` structure provides branching logic in Python:

```python
if condition1:
    # Execute if condition1 is True
elif condition2:
    # Execute if condition1 is False and condition2 is True
else:
    # Execute if all conditions are False
```

Examples:

```python
# Simple if statement
age = 18
if age >= 18:
    print("You are an adult.")

# if-else statement
temperature = 15
if temperature > 20:
    print("It's warm outside.")
else:
    print("It's cool outside.")

# if-elif-else statement
score = 85
if score >= 90:
    grade = 'A'
elif score >= 80:
    grade = 'B'
elif score >= 70:
    grade = 'C'
elif score >= 60:
    grade = 'D'
else:
    grade = 'F'
print(f"Your grade is {grade}")

# Nested conditionals
age = 25
income = 50000
if age > 18:
    if income > 30000:
        print("You qualify for the loan.")
    else:
        print("Income too low for the loan.")
else:
    print("Age requirement not met for the loan.")

# Conditional with logical operators
is_raining = True
has_umbrella = False
if is_raining and not has_umbrella:
    print("You will get wet.")
```

---

## Writing Tests

- Test your code by trying various inputs to find and fix issues
- Create test cases to verify your program works correctly
- Test the "typical" cases first to ensure basic functionality
  - If standard cases work, you have a good foundation
- Test "edge" or "corner" cases (unusual or boundary situations)
  - These less common scenarios often reveal hidden issues
  - Examples: empty inputs, extremely large values, negative numbers

```python
# Function to test
def divide(a, b):
    return a / b

# Test typical case
result = divide(10, 2)
print(f"10 / 2 = {result}")  # Should be 5.0

# Test edge cases
try:
    result = divide(10, 0)
    print(f"10 / 0 = {result}")
except ZeroDivisionError:
    print("Error: Division by zero")  # Should detect this error

# Improved function with error handling
def safe_divide(a, b):
    try:
        return a / b
    except ZeroDivisionError:
        return "Cannot divide by zero"

# Test improved function
result = safe_divide(10, 0)
print(f"10 / 0 = {result}")  # Should handle gracefully
```

- Systematically try to "break" your code to make it more robust

```python
# Function to get a percentage
def calculate_percentage(value, total):
    return (value / total) * 100

# Test cases for the function
def test_calculate_percentage():
    # Test typical case
    assert calculate_percentage(25, 100) == 25.0
    
    # Test edge cases
    assert calculate_percentage(0, 100) == 0.0
    
    try:
        calculate_percentage(50, 0)
        print("Failed: Should have raised an error")
    except ZeroDivisionError:
        print("Passed: Correctly raised ZeroDivisionError")
    
    # Test with negative values
    assert calculate_percentage(-25, 100) == -25.0
    
    # Test with floating point values
    assert round(calculate_percentage(1.5, 3), 2) == 50.0

# Run tests
test_calculate_percentage()
```

## Incremental Development

- Test as you go, building and verifying one component at a time
- Fix errors early - finding issues in large programs is much more difficult
- Add new features only after existing code works properly

```python
# Incremental development example

# Step 1: Define basic structure and test
def celsius_to_fahrenheit(celsius):
    return (celsius * 9/5) + 32

# Test step 1
print(celsius_to_fahrenheit(0))  # Should be 32.0
print(celsius_to_fahrenheit(100))  # Should be 212.0

# Step 2: Add input handling
def temperature_converter():
    celsius = float(input("Enter temperature in Celsius: "))
    fahrenheit = celsius_to_fahrenheit(celsius)
    return fahrenheit

# Test step 2 (manually)
# result = temperature_converter()
# print(f"Temperature in Fahrenheit: {result}")

# Step 3: Add error handling
def robust_temperature_converter():
    try:
        celsius = float(input("Enter temperature in Celsius: "))
        fahrenheit = celsius_to_fahrenheit(celsius)
        return fahrenheit
    except ValueError:
        return "Error: Please enter a valid number"

# Test step 3 (manually)
# result = robust_temperature_converter()
# print(f"Temperature in Fahrenheit: {result}")
```

## Comments

- Use comments to explain your code's purpose and functionality
- Single-line comments start with `#`
- Keyboard shortcut: `CTRL + /` to comment/uncomment multiple lines
- Write useful, informative comments that:
  - Explain "why" (not just "what") the code does
  - Document complex logic or non-obvious approaches
  - Highlight important assumptions or limitations

```python
# This is a single-line comment

"""
This is a multi-line comment or docstring.
It can span multiple lines and is often used
for function and module documentation.
"""

# Good comment examples
def calculate_area(radius):
    """
    Calculate the area of a circle given its radius.
    
    Args:
        radius (float): The radius of the circle
        
    Returns:
        float: The area of the circle
    """
    # Using the formula: Area = π * r²
    return 3.14159 * (radius ** 2)

# Explaining why a specific approach was taken
def get_user_name():
    # We use strip() to remove any leading/trailing whitespace
    # that might cause validation issues later
    name = input("Enter your name: ").strip()
    return name

# Poor comment example
x = 5  # This sets x to 5
```

## Loops

### While Loops
- Run indefinitely as long as a condition remains true
- Format:
  ```python
  while condition:
      # code to execute
  ```
- Examples:

```python
# Simple while loop
count = 0
while count < 5:
    print(count)
    count += 1
# Prints: 0, 1, 2, 3, 4

# Infinite loop with break
while True:
    response = input("Continue? (y/n): ")
    if response.lower() == 'n':
        break
    print("Continuing...")

# Loop with a sentinel value
sum_of_numbers = 0
number = 0
print("Enter numbers to add, or -1 to stop")
while number != -1:
    number = int(input("Enter a number: "))
    if number != -1:
        sum_of_numbers += number
print(f"Sum: {sum_of_numbers}")
```

### For Loops
- Run a definite number of times
- Format:
  ```python
  for variable in iterable:
      # code to execute
  ```
- Examples:

```python
# Loop through a range of numbers
for i in range(5):  # 0 to 4
    print(i)
# Prints: 0, 1, 2, 3, 4

# Loop with specific range
for i in range(2, 8):  # 2 to 7
    print(i)
# Prints: 2, 3, 4, 5, 6, 7

# Loop with step value
for i in range(0, 10, 2):  # 0 to 9, step 2
    print(i)
# Prints: 0, 2, 4, 6, 8

# Loop through a list
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
# Prints: apple, banana, cherry

# Loop with index using enumerate
for index, fruit in enumerate(fruits):
    print(f"{index}: {fruit}")
# Prints: 0: apple, 1: banana, 2: cherry
```

### Important Loop Control Statements
- `break`: Exits the loop immediately
- `continue`: Skips the rest of the current iteration and starts the next one
- `pass`: Does nothing; useful as a placeholder

```python
# break example
for i in range(10):
    if i == 5:
        break
    print(i)
# Prints: 0, 1, 2, 3, 4

# continue example
for i in range(10):
    if i % 2 == 0:  # If i is even
        continue
    print(i)
# Prints: 1, 3, 5, 7, 9

# pass example
for i in range(5):
    if i == 2:
        pass  # Placeholder for future code
    else:
        print(i)
# Prints: 0, 1, 2, 3, 4 (note 2 is still printed)
```

## Data Structures in Python

### Mutability
- **Immutable** data structures cannot be changed after creation
- **Mutable** data structures can be modified after creation
- Immutable types: strings, tuples, frozensets
- Mutable types: lists, dictionaries, sets

### Common Built-in Functions
- `len(A)`: Returns the number of elements in A
- `max(A)`: Returns the maximum element in A
- `min(A)`: Returns the minimum element in A
- `sum(A)`: Returns the sum of all elements in A

```python
# Example of built-in functions
numbers = [5, 3, 8, 1, 2]
print(len(numbers))  # 5
print(max(numbers))  # 8
print(min(numbers))  # 1
print(sum(numbers))  # 19

# Immutable vs mutable example
# String (immutable)
name = "John"
# This creates a new string, doesn't modify the original
new_name = name + " Doe"  
print(name)      # Still "John"
print(new_name)  # "John Doe"

# List (mutable)
numbers = [1, 2, 3]
numbers.append(4)  # Modifies the original list
print(numbers)     # [1, 2, 3, 4]
```

## Python Lists

Lists are ordered, mutable collections used to store multiple items in a single variable.

### Creating Lists

```python
# Empty list
my_list = []

# List with initial values
numbers = [1, 2, 3, 4, 5]
mixed = [1, "hello", 3.14, True]

# List from other iterables
chars = list("hello")  # ['h', 'e', 'l', 'l', 'o']

# List comprehension
squares = [x**2 for x in range(5)]  # [0, 1, 4, 9, 16]

# Nested lists
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```

### List Indexing and Slicing

```python
numbers = [10, 20, 30, 40, 50]

# Indexing (0-based)
first = numbers[0]      # 10
last = numbers[-1]      # 50
third = numbers[2]      # 30

# Slicing [start:end] (end is exclusive)
first_three = numbers[0:3]  # [10, 20, 30]
middle = numbers[1:4]       # [20, 30, 40]

# Slicing shortcuts
beginning = numbers[:2]     # [10, 20]
end = numbers[2:]           # [30, 40, 50]

# Slicing with step [start:end:step]
every_other = numbers[::2]  # [10, 30, 50]
reversed_list = numbers[::-1]  # [50, 40, 30, 20, 10]

# Creating a copy of a list
list_copy = numbers[:]
```

### Adding Elements

```python
# Append: adds an item to the end of the list
my_list = [1, 2, 3]
my_list.append(4)       # [1, 2, 3, 4]

# Extend: adds all items from another iterable
my_list.extend([5, 6])  # [1, 2, 3, 4, 5, 6]

# Insert: adds an item at a specific position
my_list.insert(0, 0)    # [0, 1, 2, 3, 4, 5, 6]
my_list.insert(2, 1.5)  # [0, 1, 1.5, 2, 3, 4, 5, 6]
```

### Removing Elements

```python
my_list = [10, 20, 30, 40, 30, 50]

# Remove: removes the first occurrence of a value
my_list.remove(30)      # [10, 20, 40, 30, 50]

# Pop with no arguments: removes and returns the last item
last = my_list.pop()    # last = 50, my_list = [10, 20, 40, 30]

# Pop with index: removes and returns item at specified position
second = my_list.pop(1) # second = 20, my_list = [10, 40, 30]

# Del statement: removes item at index
del my_list[0]          # my_list = [40, 30]

# Clear: removes all items
my_list.clear()         # my_list = []
```

### Modifying Elements

```python
numbers = [5, 2, 8, 1, 9]

# Sort: arranges items in ascending order
numbers.sort()          # [1, 2, 5, 8, 9]

# Reverse: inverts the order of items
numbers.reverse()       # [9, 8, 5, 2, 1]

# Direct assignment
numbers[0] = 10         # [10, 8, 5, 2, 1]
```

### Other List Operations

```python
numbers = [1, 2, 3, 2, 4, 2, 5]

# Index: returns the position of the first occurrence of a value
position = numbers.index(2)  # position = 1

# Count: returns the number of occurrences of a value
occurrences = numbers.count(2)  # occurrences = 3

# Membership testing
print(3 in numbers)     # True
print(6 in numbers)     # False

# List comprehension with condition
evens = [x for x in numbers if x % 2 == 0]  # [2, 2, 4, 2]
```

## Python Dictionaries

Dictionaries are collections of key-value pairs, where each key is unique.

### Basic Concept

- Keys must be immutable (strings, numbers, tuples)
- Values can be of any type
- Example: username as key, password as value

### Creating Dictionaries

```python
# Empty dictionary
empty_dict = {}

# Dictionary with initial values
user_data = {'username': 'john_doe', 'password': 'secret123', 'active': True}

# Alternative creation method
student = dict(name='Alice', age=20, gpa=3.9)

# Creating from sequence of tuples
items = [('apple', 0.99), ('banana', 0.59), ('orange', 1.29)]
prices = dict(items)
```

### Dictionary Operations

```python
# Accessing values
user = {'name': 'John', 'age': 30, 'city': 'New York'}
print(user['name'])     # John
print(user.get('age'))  # 30
print(user.get('email', 'Not found'))  # Not found (default value)

# Adding or updating entries
user['email'] = 'john@example.com'  # Add new key-value pair
user['age'] = 31                    # Update existing value

# Removing entries
removed_city = user.pop('city')     # Removes and returns the value
del user['age']                     # Removes the key-value pair

# Checking if a key exists
if 'name' in user:
    print(f"User's name is {user['name']}")

# Iterating through keys
for key in user:
    print(key)

# Iterating through values
for value in user.values():
    print(value)

# Iterating through key-value pairs
for key, value in user.items():
    print(f"{key}: {value}")
```

### Common Dictionary Methods

```python
user = {'name': 'John', 'age': 30, 'city': 'New York'}

# Get all keys and values
keys = user.keys()
values = user.values()
items = user.items()

# Create a copy
user_copy = user.copy()

# Clear all entries
user.clear()

# Create with default values
counts = dict.fromkeys(['apple', 'banana', 'cherry'], 0)
# Result: {'apple': 0, 'banana': 0, 'cherry': 0}

# Update with another dictionary
user = {'name': 'John'}
user.update({'age': 30, 'city': 'New York'})
# Result: {'name': 'John', 'age': 30, 'city': 'New York'}
```

## Procedural Thinking

Procedural thinking is a fundamental concept in programming, focusing on defining clear steps to solve problems. It's the basis for creating effective algorithms and computer programs.

### Algorithm

An **algorithm** is a finite sequence of precise instructions for performing a computation or solving a problem.

#### Types of Algorithms

1. **Sequential**
   - Instructions executed in order: first do X, then do Y, then do Z
   - Example: A recipe where steps must be followed in sequence

   ```python
   # Sequential algorithm example
   def make_sandwich():
       print("1. Get two slices of bread")
       print("2. Add spread to both slices")
       print("3. Add fillings")
       print("4. Put slices together")
       print("5. Cut sandwich in half")
   ```

2. **Conditional**
   - Decision-based execution: if some condition is met, then do X; otherwise do Y
   - Example: If temperature > 30°C, turn on AC; otherwise, keep AC off

   ```python
   # Conditional algorithm example
   def check_temperature(temp):
       if temp > 30:
           print("Turn on the air conditioner")
       else:
           print("AC can remain off")
           
       if temp < 5:
           print("Turn on the heater")
   ```

3. **Repetition**
   - Repeat X N times
   - Repeat X as long as condition C is met
   - Example: While there are dirty dishes, continue washing

   ```python
   # Repetition algorithm example
   def count_down(n):
       # Repeat exactly n times
       for i in range(n, 0, -1):
           print(i)
       print("Blast off!")
       
   def process_items(items):
       # Repeat until condition is met
       while len(items) > 0:
           item = items.pop(0)
           print(f"Processing {item}")
   ```

4. **Concurrent**
   - Execute multiple instructions simultaneously: do X and Y at the same time
   - Example: Multi-threading in applications

   ```python
   # Pseudo-code for concurrent execution
   """
   thread1 = start_new_thread(function_1)
   thread2 = start_new_thread(function_2)
   
   # Both functions run simultaneously
   wait_for_all_threads()
   """
   ```

5. **Nested**
   - Placing one algorithm type inside another
   - Example: A loop containing conditional statements

   ```python
   # Nested algorithm example
   def analyze_numbers(numbers):
       for num in numbers:  # Repetition
           if num % 2 == 0:  # Conditional inside repetition
               print(f"{num} is even")
           else:
               print(f"{num} is odd")
               
           if num > 0:  # Another conditional inside same repetition
               print(f"{num} is positive")
   ```
