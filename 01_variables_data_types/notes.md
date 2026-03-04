# Variables & Naming Conventions in Python

## 1. What is a Variable?

A variable is a named container used to store data.

In Python, variables are created using the assignment operator (=).

No special keyword like `let` or `const` is required.

---

## 2. Basic Syntax

variable_name = value

Example:

name = "John Doe"
age = 25

- Left side → variable name
- = → assignment operator
- Right side → value stored

---

## 3. Strings in Variables

Strings are text values written inside quotes.

Single quotes:
'Hello'

Double quotes:
"Hello"

Example:

name = "Tulsi"
city = 'Indore'

---

## 4. Rules for Naming Variables

✔ Must start with:
- A letter (a-z, A-Z)
- Or underscore (_)

❌ Cannot start with a number:
5name = "Tulsi"   # SyntaxError

✔ Can contain:
- Letters
- Numbers
- Underscores

❌ Cannot use Python reserved keywords:
if, class, def, etc.

✔ Case-sensitive:
age = 23
Age = 30
These are different variables.

---

## 5. Naming Conventions (Best Practices)

1. Use snake_case (lowercase + underscores)
user_name = "Tulsi"

2. Use descriptive names
user_age = 23     # Good
ua = 23           # Avoid

3. Avoid single-letter names
x = 10   # Not meaningful

Exception:
In loops, i, j, k are acceptable.

---

## 6. Comments in Python

Comments start with #

Example:
# This is a comment
```python
Multi-line comment:
# Line 1
# Line 2
# Line 3
```

Python ignores everything after # on that line.

Use comments to:
- Explain logic
- Add reminders
- Clarify complex code

Do NOT use comments to explain bad variable names.
Instead, use better variable names.

---

## 7. Common Mistakes

- Starting variable with number
- Using reserved keywords
- Using unclear names (x, a1, temp1)
- Confusing uppercase and lowercase

---

## 8. Key Points to Remember

- Variables store data.
- No keyword needed to declare variables.
- Use snake_case naming.
- Variable names must follow rules.
- Python is case-sensitive.


===================================================================


# Python Data Types & Checking Type of Variables

## 1. What is a Data Type?

A **data type** defines the type of value a variable holds.

Examples of values:
- Numbers
- Text
- Collections of items

Programming languages use data types to **store and manipulate data correctly**.

---

## 2. Python is Dynamically Typed

Python automatically detects the data type of a variable based on the value assigned.

Example:

'''python
name = "John Doe"   # Python detects string
age = 25            # Python detects integer
'''

Unlike languages like **Java, C#, C++**, Python does NOT require explicit type declaration.

---

## 3. Important Note About Dynamic Typing

In Python:

- Type errors appear **during program execution (runtime)**.
- Python checks types **while running the code line by line**.

In compiled languages:
- Type errors are detected **before execution (compile time)**.

---

# Common Python Data Types

## 4. Integer (int)

Whole numbers without decimals.

Examples:

'''python
num = 10
num2 = -5
'''

---

## 5. Float (float)

Numbers containing decimal values.

'''python
price = 4.50
temperature = -0.4
'''

---

## 6. String (str)

Text values enclosed in quotes.

'''python
name = "Tulsi"
message = 'Hello World'
'''

Strings represent **text data**.

---

## 7. Boolean (bool)

Represents **True or False** values.

'''python
is_logged_in = True
is_admin = False
'''

Used in **conditions and logical operations**.

---

## 8. List (list)

Ordered collection of items.  
Can store **different data types**.

'''python
my_list = [22, "Hello world", 3.14, True]
'''

Lists are **mutable** (can be modified).

---

## 9. Tuple (tuple)

Ordered collection similar to list but **immutable** (cannot change).

'''python
my_tuple = (7, 5, 8)
'''

---

## 10. Set (set)

Unordered collection of **unique elements**.

'''python
my_set = {7, 5, 8}
'''

No duplicate values allowed.

---

## 11. Dictionary (dict)

Stores **key-value pairs**.

'''python
person = {
    "name": "Alice",
    "age": 25
}
'''

Used for **structured data**.

---

## 12. Range (range)

Represents a sequence of numbers.

Often used in loops.

'''python
numbers = range(5)
'''

Produces sequence:
0 → 4

---

## 13. None (NoneType)

Represents **absence of a value**.

'''python
result = None
'''

Used as placeholder for empty values.

---

# Checking Data Type

## 14. type() Function

Used to check the type of a variable.

'''python
name = "Hello"
age = 21

print(type(name))   # <class 'str'>
print(type(age))    # <class 'int'>
'''

---

## 15. isinstance() Function

Checks whether a variable belongs to a specific type.

Returns **True or False**.

'''python
print(isinstance("Hello", str))   # True
print(isinstance(True, bool))     # True
print(isinstance(42, int))        # True
print(isinstance("John", int))    # False
'''

