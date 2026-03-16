# Exception Handling — Key Points

- **Exception Handling** prevents program crashes by handling errors gracefully.

- Python uses **try, except, else, and finally** blocks.

---

## try
Code where an **error might occur**.

```python
try:
    x = 10 / 0
```

---

## except
Runs when a **specific error occurs**.

```python
except ZeroDivisionError:
    print("You can't divide by zero!")
```

---

## else
Runs **only if no exception occurs**.

```python
else:
    print("Division successful")
```

---

## finally
Runs **always**, whether error occurs or not.

Used for **cleanup tasks** (closing files, releasing resources).

```python
finally:
    print("This always runs")
```

---

## Multiple Exceptions

You can handle different errors separately.

```python
try:
    number = int("abc")
except ValueError:
    print("Invalid number")
except ZeroDivisionError:
    print("Cannot divide by zero")
```

---

## Exception Object

Use `as e` to access the **error message**.

```python
try:
    x = 1 / 0
except ZeroDivisionError as e:
    print(e)
```

---

## Catch Multiple Exceptions Together

```python
try:
    number = int(input())
    result = 10 / number
except (ValueError, ZeroDivisionError) as e:
    print(e)
```

---

# Quick Summary

- `try` → code that may cause error  
- `except` → handles the error  
- `else` → runs if no error  
- `finally` → always runs  
- Use `as e` to access error details


# Python Notes — Raise Statement

## What is `raise`?
The `raise` statement is used to **manually trigger an exception** in Python.  
It allows you to control **when an error should occur** and define **custom error conditions**.

Used for:
- Input validation
- Enforcing rules
- Creating custom errors
- Propagating exceptions

---

## Basic Syntax

```python
raise ExceptionType("error message")
```

Example:

```python
def check_age(age):
    if age < 0:
        raise ValueError("Age cannot be negative")
    return age
```

Usage:

```python
try:
    check_age(-5)
except ValueError as e:
    print(f"Error: {e}")
```

---

## Re-raising an Exception

Using `raise` without arguments re-raises the **current exception**.

```python
def process_data(data):
    try:
        result = int(data)
        return result * 2
    except ValueError:
        print("Logging: Invalid data received")
        raise
```

```python
try:
    process_data("abc")
except ValueError:
    print("Handled at higher level")
```

---

## Creating Custom Exceptions

Custom exceptions are created by inheriting from `Exception`.

```python
class InsufficientFundsError(Exception):
    def __init__(self, balance, amount):
        self.balance = balance
        self.amount = amount
        super().__init__(f"Insufficient funds: ${balance} available, ${amount} requested")
```

Example usage:

```python
def withdraw(balance, amount):
    if amount > balance:
        raise InsufficientFundsError(balance, amount)
    return balance - amount
```

```python
try:
    withdraw(100, 150)
except InsufficientFundsError as e:
    print(f"Transaction failed: {e}")
```

---

## Exception Chaining (`raise ... from`)

Shows the relationship between exceptions.

Suppress original exception:

```python
raise ValueError("Configuration file is missing") from None
```

Chain with original exception:

```python
raise ValueError("Invalid configuration format") from e
```

Example:

```python
def parse_config(filename):
    try:
        with open(filename, "r") as file:
            data = file.read()
            return int(data)
    except FileNotFoundError:
        raise ValueError("Configuration file is missing") from None
    except ValueError as e:
        raise ValueError("Invalid configuration format") from e
```

---

## Using `assert`

`assert` is shorthand for raising `AssertionError` when a condition fails.

```python
assert condition, "error message"
```

Example:

```python
def calculate_square_root(number):
    assert number >= 0, "Cannot calculate square root of negative number"
    return number ** 0.5
```

```python
try:
    calculate_square_root(-4)
except AssertionError as e:
    print(f"Assertion failed: {e}")
```

---

## Key Points

- `raise` manually triggers exceptions.
- Helps enforce rules and validate inputs.
- `raise Exception("message")` creates a custom error.
- `raise` alone re-raises the current exception.
- Custom exceptions inherit from `Exception`.
- `raise ... from e` chains exceptions.
- `raise ... from None` hides original exception.
- `assert` is a shortcut for raising `AssertionError`.
