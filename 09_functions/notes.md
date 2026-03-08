# Functions in Python

## 1. What is a Function?

A **function** is a reusable block of code that runs when it is **called**.

Functions help:
- Reuse code
- Organize programs
- Avoid repetition

Python has **built-in functions** and allows you to create **custom functions**.

---

# 2. Built-in Functions

Built-in functions are functions already available in Python.

Examples:
- `print()`
- `input()`
- `int()`

### Example: input()

The `input()` function allows users to enter data.

```python
name = input("What is your name?")
print("Hello", name)
```

Example output:

```
Hello Kolade
```

---

### Example: int()

The `int()` function converts values to integers.

```python
print(int(3.14))   # 3
print(int("42"))   # 42
print(int(True))   # 1
print(int(False))  # 0
```

---

# 3. Creating Custom Functions

You can create your own function using the **def keyword**.

### Syntax

```python
def function_name():
    # function body
```

- `def` → defines a function
- `function_name` → name of the function
- `()` → parentheses required
- `:` → starts the function body
- Indented code → function body

---

# 4. Example of a Simple Function

```python
def hello():
    print("Hello World")
```

### Calling the Function

```python
hello()
```

Output:

```
Hello World
```

---

# 5. Parameters and Arguments

Functions can accept inputs called **parameters**.

- **Parameter** → variable inside the function
- **Argument** → value passed when calling the function

### Example

```python
def calculate_sum(a, b):
    print(a + b)
```

Here:
- `a` and `b` are **parameters**

### Calling the Function

```python
calculate_sum(3, 1)
```

Output

```
4
```

Here:
- `3` and `1` are **arguments**

---

# 6. Error When Arguments Are Missing

If the correct number of arguments is not provided, Python raises an error.

```python
calculate_sum()
```

Error:

```
TypeError: calculate_sum() missing 2 required positional arguments: 'a' and 'b'
```

---

# 7. Return Statement

Functions use the **return keyword** to send a value back.

### Example Without Return

```python
def calculate_sum(a, b):
    print(a + b)

my_sum = calculate_sum(3, 1)
print(my_sum)
```

Output

```
4
None
```

Explanation:
- Function prints the sum
- But does not return a value
- Python returns **None by default**

---

# 8. Using Return Properly

```python
def calculate_sum(a, b):
    return a + b

my_sum = calculate_sum(3, 1)
print(my_sum)
```

Output

```
4
```

Now:
- The function **returns the result**
- The value is stored in `my_sum`

---

# Key Points

- Functions are **reusable blocks of code**
- Built-in functions include `print()`, `input()`, and `int()`
- Custom functions are created using `def`
- **Parameters** receive values inside the function
- **Arguments** are values passed when calling the function
- `return` sends a value back from the function
- If no return is used, Python returns **None**

# Scope in Python (LEGB Rule)

## What is Scope?

**Scope** determines **where a variable can be accessed in a program**.  
It controls the **visibility and lifetime of variables**.

Python resolves variable names using the **LEGB rule**.

---

# LEGB Rule

Python searches for variables in the following order:

1. **L – Local Scope**
2. **E – Enclosing Scope**
3. **G – Global Scope**
4. **B – Built-in Scope**

---

# 1. Local Scope (L)

Variables created **inside a function or class** belong to the **local scope**.

They can **only be accessed inside that function**.

### Example

```python
def my_func():
    my_var = 10
    print(my_var)

my_func()      # 10
print(my_var)  # NameError
```

Explanation:
- `my_var` exists only inside `my_func`
- Accessing it outside causes **NameError**

---

# 2. Enclosing Scope (E)

Occurs when **a function is inside another function**.

The **inner function can access variables from the outer function**.

### Example

```python
def outer_func():
    msg = "Hello there!"

    def inner_func():
        print(msg)

    inner_func()

outer_func()
```

Output

```
Hello there!
```

### Important Rule

Outer functions **cannot access variables defined in inner functions**.

```python
def outer_func():
    msg = "Hello there!"
    print(res)

    def inner_func():
        res = "How are you?"
        print(msg)

    inner_func()

outer_func()
```

Output

```
NameError: name 'res' is not defined
```

Because `res` belongs to the **local scope of `inner_func`**.

---

# Using `nonlocal` Keyword

`nonlocal` allows a nested function to **modify variables from the enclosing scope**.

```python
def outer_func():
    msg = "Hello there!"
    res = ""

    def inner_func():
        nonlocal res
        res = "How are you?"
        print(msg)

    inner_func()
    print(res)

outer_func()
```

Output

```
Hello there!
How are you?
```

---

# 3. Global Scope (G)

Variables defined **outside all functions** belong to the **global scope**.

They can be accessed **anywhere in the program**.

### Example

```python
my_var = 100

def show_var():
    print(my_var)

show_var()
print(my_var)
```

Output

```
100
100
```

---

# Using `global` Keyword

The `global` keyword allows a function to **create or modify global variables**.

### Creating a Global Variable

```python
my_var_1 = 7

def show_vars():
    global my_var_2
    my_var_2 = 10
    print(my_var_1)
    print(my_var_2)

show_vars()

print(my_var_2)
```

Output

```
7
10
10
```

---

### Modifying a Global Variable

```python
my_var = 10

def change_var():
    global my_var
    my_var = 20

change_var()

print(my_var)
```

Output

```
20
```

---

# 4. Built-in Scope (B)

Built-in scope contains **Python's predefined functions, objects, and keywords**.

These are **available everywhere in Python**.

Examples of built-in functions:
- `print()`
- `type()`
- `str()`
- `len()`
- `isinstance()`

### Example

```python
print(str(45))
print(type(3.14))
print(isinstance(3, str))
```

Output

```
'45'
<class 'float'>
False
```

---

# Summary

| Scope | Description |
|-----|-----|
| Local | Variables inside a function |
| Enclosing | Variables in outer (nested) functions |
| Global | Variables defined outside functions |
| Built-in | Python's predefined functions and objects |

### Variable Lookup Order

Python searches variables in this order:

```
Local → Enclosing → Global → Built-in
```
