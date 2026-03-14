# Python Standard Library & Importing Modules

## Python Standard Library

The **Python Standard Library** is a collection of **built-in modules** that provide ready-to-use functions, classes, and tools.

It helps developers **avoid writing code from scratch**.

### Common Uses
- Working with **files**
- Interacting with **operating system**
- **Networking**
- **Date and time operations**
- **Mathematical calculations**
- **Regular expressions**
- **Testing and debugging**

### Popular Built-in Modules

- `math` → mathematical operations  
- `random` → random number generation  
- `re` → regular expressions  
- `datetime` → working with dates and time  

---

# Importing Modules

To use a module, we use the **import statement**.

### Basic Syntax

```python
import module_name
```

Example:

```python
import math

print(math.sqrt(36))  # 6.0
```

Use **dot notation** to access module functions.

```
module_name.function_name()
```

---

# Import with Alias

Use `as` to give a module a **short name**.

```python
import math as m

print(m.sqrt(36))
```

Useful for:
- Shortening long module names
- Avoiding name conflicts

---

# Import Specific Functions

Instead of importing the whole module, you can import **specific functions**.

```python
from module_name import function1, function2
```

Example:

```python
from math import radians, sin, cos

angle = 40
angle_radians = radians(angle)

print(sin(angle_radians))
print(cos(angle_radians))
```

Now functions can be used **without module prefix**.

---

# Import with Alias for Functions

```python
from module_name import function as alias
```

Example:

```python
from math import sqrt as s

print(s(36))
```

---

# Import Everything (Not Recommended)

```python
from module_name import *
```

Example:

```python
from math import *

print(sqrt(36))
print(pow(5,2))
```

⚠ Generally **not recommended** because it can cause **name conflicts**.

---

# Importing Constants

Modules may also contain **constants**.

Example:

```python
import math

print(math.pi)
```

---

# Importing Classes

Modules may contain **classes**.

Example:

```python
import datetime

birthday = datetime.date(1959,7,15)

print(birthday.day)
print(birthday.month)
print(birthday.year)
```

---

# Special Variable: `__name__`

`__name__` is a **built-in variable**.

- If file runs directly → `__name__ = "__main__"`
- If file imported → `__name__ = module_name`

### Example

```python
if __name__ == "__main__":
    print("This runs only when script is executed directly")
```

This prevents code from running when the file is **imported as a module**.

---

# Key Points

- Python provides many **built-in modules** in the Standard Library.
- Modules contain **functions, classes, constants, variables**.
- `import module` → import entire module.
- `import module as alias` → give module a short name.
- `from module import name` → import specific elements.
- `from module import *` → imports everything (not recommended).
- `__name__ == "__main__"` ensures code runs only when the file is executed directly.
