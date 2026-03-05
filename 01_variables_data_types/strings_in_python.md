# Strings & String Immutability

## 1. What is a String?

A **string** is a sequence of characters enclosed in quotes.

Strings can be written using:
- Single quotes `' '`
- Double quotes `" "`

Example:

'''python
my_str_1 = 'Hello'
my_str_2 = "World"
'''

Both are treated the same in Python.

---

## 2. Multi-line Strings

Multi-line strings are created using **triple quotes**.

my_str_3 = """Multiline
string"""

my_str_4 = '''Another
multiline
string'''

Used when writing long text or documentation.

---

## 3. Quotes Inside Strings

### Method 1 — Use opposite quotes

'''python
msg = "It's a sunny day"
quote = 'She said, "Hello World!"'
'''

### Method 2 — Escape characters using backslash `\`

'''python
msg = 'It\'s a sunny day'
quote = "She said, \"Hello!\""
'''

---

## 4. Check if Text Exists in a String

Use the **`in` operator**.

Returns **True or False**.

'''python
my_str = "Hello world"

print('Hello' in my_str)   # True
print('hey' in my_str)     # False
print('e' in my_str)       # True
print('f' in my_str)       # False
'''

---

## 5. Length of a String

Use the built-in function **`len()`**

'''python
my_str = "Hello world"

print(len(my_str))   # 11
'''

It counts the number of characters including spaces.

---

## 6. String Indexing

Each character in a string has an **index position**.

Indexing starts from **0**.

'''python
my_str = "Hello world"

print(my_str[0])   # H
print(my_str[6])   # w
'''

---

## 7. Negative Indexing

Negative indexing starts from the end of the string.

'''python
my_str = "Hello world"

print(my_str[-1])   # d
print(my_str[-2])   # l
'''

Useful when accessing last characters.

---

## 8. String Immutability

Strings are **immutable** in Python.

Meaning:
Once created, the string **cannot be changed directly**.

### Reassignment is allowed

'''python
greeting = "hi"

greeting = "hello"

print(greeting)
'''

The variable now points to a **new string object**.

---

### Direct modification is NOT allowed

'''python
greeting = "hi"

greeting[0] = "H"   # ERROR
'''

Error:
```
TypeError: 'str' object does not support item assignment
```

Because strings cannot be modified character by character.

---

## 9. Important Points to Remember

- Strings are **immutable**
- Use `' '` or `" "` for strings
- Multi-line strings use `''' '''` or `""" """`
- Indexing starts from **0**
- Negative indexing accesses characters from the end
- Use `len()` to get string length
- Use `in` operator to check substring

# String Concatenation & String Interpolation

## 1. String Concatenation

String concatenation means **joining multiple strings together**.

In Python, concatenation is done using the **+ operator**.

Important rule:
All values must be **strings**.

---

### Example: String + String

'''python
my_str_1 = "Hello"
my_str_2 = "World"

result = my_str_1 + " " + my_str_2
print(result)   # Hello World
'''

---

## 2. Concatenating String With Number

Python **does NOT automatically convert numbers to strings**.

Trying this will cause an error.

'''python
name = "John Doe"
age = 26

result = name + age
print(result)
# TypeError: can only concatenate str (not "int") to str
'''

To fix this, convert numbers to string using **str()**.

'''python
name = "John Doe"
age = 26

result = name + str(age)
print(result)   # John Doe26
'''

---

## 3. Augmented Concatenation (+=)

The **+= operator** allows concatenation and assignment in one step.

'''python
name = "John Doe"
age = 26

name_and_age = name
name_and_age += str(age)

print(name_and_age)   # John Doe26
'''

---

## 4. String Interpolation

String interpolation means **inserting variables or expressions inside a string**.

Python uses **f-strings (formatted strings)** for this.

Syntax:
Start string with **f** and use **{}** to insert variables.

---

### Example: f-string

'''python
name = "John Doe"
age = 26

message = f"My name is {name} and I am {age} years old"
print(message)
'''

Output:
My name is John Doe and I am 26 years old

---

### Example: Expressions Inside f-string

'''python
num1 = 5
num2 = 10

print(f"The sum of {num1} and {num2} is {num1 + num2}")
'''

Output:
The sum of 5 and 10 is 15

---

## 5. Advantages of f-strings

✔ Cleaner code  
✔ Easier to read  
✔ Automatic type conversion  
✔ Can evaluate expressions

---

## 6. Best Practice

Prefer **f-strings** over concatenation when working with variables.

Example:

❌ Less readable
'''python
print("My name is " + name + " and I am " + str(age))
'''

✔ Recommended
'''python
print(f"My name is {name} and I am {age}")
'''

---

## 7. Common Mistakes

- Concatenating string with integer without conversion
- Forgetting `f` before f-string
- Missing `{}` in interpolation

---

## 8. Key Point to Remember

Concatenation → Joining strings using **+**

Interpolation → Embedding variables inside string using **f-strings**



## String Slicing

### Key Points
- String slicing is used to extract a portion of a string.
- Each character in a string has an **index** (starting from 0).
- Negative indexing starts from the end of the string.
- Slicing does **not modify the original string** (strings are immutable).
- Basic slicing syntax:

string[start:stop]

- `start` → index where slicing begins.
- `stop` → index where slicing stops (NOT included).
- `step` → interval between characters (optional).

---

### Basic Index Access

'''python
my_str = "Hello world"

print(my_str[0])   # H
print(my_str[6])   # w
print(my_str[-1])  # d
'''

---

### Basic String Slicing

'''python
my_str = "Hello world"

print(my_str[1:4])   # ell
'''

Explanation:
- Starts at index **1**
- Stops before index **4**

---

### Omitting Start Index

If start is omitted → Python assumes **0**

'''python
my_str = "Hello world"

print(my_str[:7])   # Hello w
'''

---

### Omitting Stop Index

If stop is omitted → Python slices **until the end**

'''python
my_str = "Hello world"

print(my_str[8:])   # rld
'''

---

### Extract Entire String

'''python
my_str = "Hello world"

print(my_str[:])   # Hello world
'''

---

### Using Step in Slicing

Syntax:

string[start:stop:step]

'''python
my_str = "Hello world"

print(my_str[0:11:2])   # Hlowrd
'''

Explanation:
- Start → 0
- Stop → 11
- Step → 2 (every second character)

---

### Reverse a String (Common Trick)

Using step = -1

'''python
my_str = "Hello world"

print(my_str[::-1])   # dlrow olleH
'''

---

### Important Things to Remember

- `stop` index is **always excluded**.
- Slicing **does not change the original string**.
- Negative step (`-1`) can reverse the string.
- Default values:
  - start = 0
  - stop = end of string
  - step = 1

---

### Common Mistakes

- Forgetting that **stop index is excluded**.
- Confusing **indexing (`[]`) with slicing (`[start:stop]`)**.
- Assuming slicing modifies the original string (it does not).
