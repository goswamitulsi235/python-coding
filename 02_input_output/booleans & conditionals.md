# Conditional Statements & Logical Operators

Conditional statements allow a program to **make decisions** based on conditions that evaluate to **True or False**.

Python checks a condition and executes specific code depending on the result.

---

# Boolean Values

A **Boolean** is a data type that has only two values:

- `True`
- `False`

Many conditions in Python return Boolean values.

```python
print(5 > 3)   # True
print(2 > 10)  # False
```

---

# Comparison Operators

Comparison operators compare two values and return **True or False**.

| Operator | Meaning |
|--------|--------|
| `==` | Equal to |
| `!=` | Not equal to |
| `>` | Greater than |
| `<` | Less than |
| `>=` | Greater than or equal to |
| `<=` | Less than or equal to |

Example:

```python
print(3 > 4)   # False
print(3 < 4)   # True
print(4 == 4)  # True
print(3 != 4)  # True
print(3 >= 4)  # False
print(3 <= 4)  # True
```

---

# if Statement

The **if statement** runs code **only when a condition is True**.

Syntax:

```python
if condition:
    # code to run
```

Example:

```python
age = 18

if age >= 18:
    print("You are an adult")
```

Output:

```
You are an adult
```

---

# Indentation in Python

Python uses **indentation (spaces)** to define a block of code.

Standard practice → **4 spaces indentation**

Incorrect indentation causes an error.

```python
age = 18

if age >= 18:
print("You are an adult")   # IndentationError
```

Correct:

```python
if age >= 18:
    print("You are an adult")
```

---

# pass Statement

`pass` is used as a **placeholder** when a block is required but you don't want to write code yet.

```python
if 10 > 5:
    pass
```

---

# if – else Statement

`else` runs when the `if` condition is **False**.

Syntax:

```python
if condition:
    # code if True
else:
    # code if False
```

Example:

```python
age = 12

if age >= 18:
    print("You are an adult")
else:
    print("You are not an adult yet")
```

Output:

```
You are not an adult yet
```

---

# if – elif – else Statement

Used when there are **multiple conditions**.

Syntax:

```python
if condition1:
    # code
elif condition2:
    # code
else:
    # code
```

Example:

```python
age = 12

if age >= 18:
    print("You are an adult")
elif age >= 13:
    print("You are a teenager")
else:
    print("You are a child")
```

Output:

```
You are a child
```

---

# Multiple elif Conditions

You can use **multiple `elif` statements**.

```python
age = 2

if age >= 65:
    print("Senior citizen")
elif age >= 30:
    print("Adult in prime")
elif age >= 18:
    print("Young adult")
elif age >= 13:
    print("Teenager")
elif age >= 3:
    print("Young child")
else:
    print("Toddler or infant")
```

---

# Key Points

- Conditional statements control **program decision-making**
- Conditions evaluate to **True or False**
- `if` runs when condition is **True**
- `else` runs when condition is **False**
- `elif` checks **additional conditions**
- Python uses **indentation (4 spaces)** to define code blocks
- Comparison operators are used to **compare values**

---
