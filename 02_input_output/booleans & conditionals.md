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


# Truthy & Falsy Values and Boolean Operators

## 1. Truthy and Falsy Values

In Python, every value has a **boolean meaning** when used in conditions.

- **Truthy values → treated as True**
- **Falsy values → treated as False**

### Common Falsy Values

- `False`
- `None`
- `0`
- `0.0`
- `""` (empty string)

### Common Truthy Values

- Non-zero numbers
- Non-empty strings
- Most objects

### Checking Truthy or Falsy

Use the `bool()` function to convert a value into `True` or `False`.

```python
print(bool(False))   # False
print(bool(0))       # False
print(bool(""))      # False

print(bool(True))    # True
print(bool(1))       # True
print(bool("Hello")) # True
```

---

# Boolean Operators

Boolean operators allow you to **combine multiple conditions**.

Python has **three logical operators**:

1. `and`
2. `or`
3. `not`

---

# 1. AND Operator

The `and` operator returns **True only if both conditions are True**.

### Example

```python
is_citizen = True
age = 25

if is_citizen and age >= 18:
    print("You are eligible to vote")
else:
    print("You are not eligible to vote")
```

### How AND Works

- If the **first operand is falsy → Python stops and returns it**
- If the **first operand is truthy → Python evaluates the second operand**

```python
print(True and 25)   # 25
print(False and 25)  # False
```

---

# 2. OR Operator

The `or` operator returns **True if at least one condition is True**.

### Example

```python
age = 19
is_student = True

if age < 18 or is_student:
    print("You are eligible for a student discount")
else:
    print("You are not eligible for a student discount")
```

### How OR Works

- If the **first operand is truthy → Python returns it**
- If the **first operand is falsy → Python evaluates the second operand**

```python
age = 19
is_employed = False

print(age or is_employed)  # 19
```

---

# 3. NOT Operator

The `not` operator **reverses the boolean value**.

- True → False  
- False → True

### Examples

```python
print(not "")      # True
print(not "Hello") # False
print(not 0)       # True
print(not 1)       # False
print(not False)   # True
print(not True)    # False
```

### Using NOT in Conditions

```python
is_admin = False

if not is_admin:
    print("Access denied for non-administrators.")
else:
    print("Welcome, Administrator!")
```

---

# Short-Circuit Evaluation

Python evaluates conditions **from left to right** and **stops as soon as the result is determined**.  
This behavior is called **short-circuiting**.

### AND Short-Circuit

If the first value is **False**, Python stops immediately.

```python
False and print("This will not run")
```

### OR Short-Circuit

If the first value is **True**, Python stops immediately.

```python
True or print("This will not run")
```

---

# Key Points

- Every Python value is **truthy or falsy**
- `bool()` converts values to **True or False**
- `and` → True only if **both conditions are True**
- `or` → True if **at least one condition is True**
- `not` → **reverses** the boolean value
- `and` and `or` use **short-circuit evaluation**
