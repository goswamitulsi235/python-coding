# Common Python Errors — Key Notes

## 1. SyntaxError
Occurs when Python code **breaks syntax rules**.

```python
print("Hello"
# SyntaxError
```

Missing brackets, quotes, or incorrect structure.

---

## 2. NameError
Occurs when using a **variable that is not defined**.

```python
print(name)
# NameError
```

---

## 3. TypeError
Occurs when performing an operation on **incompatible data types**.

```python
5 + "5"
# TypeError
```

---

## 4. IndexError
Occurs when accessing a **list index that doesn't exist**.

```python
nums = [1,2,3]

print(nums[5])
# IndexError
```

---

## 5. AttributeError
Occurs when calling a **method that an object doesn't support**.

```python
num = 42

num.append(5)
# AttributeError
```

---

# Key Points

- **SyntaxError** → invalid Python syntax  
- **NameError** → variable not defined  
- **TypeError** → incompatible data types  
- **IndexError** → index out of range  
- **AttributeError** → method doesn't exist for object

  # Python Debugging — Key Points

## What is Debugging
Debugging means **finding and fixing errors (bugs) in code**.

---

# Common Debugging Techniques

### 1. Using `print()` Statements
- Print variable values to check program flow.
- Helps understand what the program is doing.

```python
def add(a, b):
    result = a + b
    print(f"Adding {a} and {b} = {result}")
    return result
```

---

### 2. Using `pdb` (Python Debugger)
- Python’s **built-in debugging tool**.
- Allows **step-by-step execution**.
- Inspect variables during runtime.

```python
import pdb

def divide(a, b):
    pdb.set_trace()
    return a / b
```

Common commands:
- `n` → next line  
- `c` → continue  
- `p` → print variable  
- `q` → quit debugger

---

### 3. IDE Debugging Tools (VS Code etc.)

Features:
- **Breakpoints**
- **Step execution**
- **Variable inspection**

Useful commands:

- **F5** → start debugging  
- **F10** → step over  
- **F11** → step into  
- **Shift+F11** → step out  

---

# Key Points

- Debugging = **finding & fixing bugs**
- `print()` → quick debugging
- `pdb` → interactive debugging
- IDE tools → **visual debugging with breakpoints**
