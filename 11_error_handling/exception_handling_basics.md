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
