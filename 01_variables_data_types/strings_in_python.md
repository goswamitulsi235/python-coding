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

'''python
my_str_3 = """Multiline
string"""

my_str_4 = '''Another
multiline
string'''
'''

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
