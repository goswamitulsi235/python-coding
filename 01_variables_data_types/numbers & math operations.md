# Integers and Floats in Python

## 1. Numeric Data Types

Python has two main numeric types:

- **int (Integer)** → Whole numbers without decimal points
- **float (Floating Point)** → Numbers with decimal points

Examples:

```python
my_int_1 = 56
my_int_2 = -4

my_float_1 = -12.0
my_float_2 = 4.9

print(type(my_int_1))   # <class 'int'>
print(type(my_float_1)) # <class 'float'>
```

---

# 2. Basic Arithmetic Operations

Python supports common mathematical operations.

| Operation | Symbol |
|--------|--------|
| Addition | `+` |
| Subtraction | `-` |
| Multiplication | `*` |
| Division | `/` |

Example:

```python
a = 56
b = 12

print(a + b)  # Addition
print(a - b)  # Subtraction
print(a * b)  # Multiplication
print(a / b)  # Division
```

⚠️ **Important:**  
Division `/` always returns a **float**.

---

# 3. Float Arithmetic

All arithmetic operations also work with floats.

```python
x = 5.4
y = 12.0

print(x + y)  # Addition
print(y - x)  # Subtraction
print(x * y)  # Multiplication
print(y / x)  # Division
```

---

# 4. Mixing Integers and Floats

When **int and float are used together**, Python automatically converts the result to **float**.

```python
my_int = 56
my_float = 5.4

result = my_int + my_float

print(result)        # 61.4
print(type(result))  # <class 'float'>
```

This applies to:
- Addition
- Subtraction
- Multiplication
- Division

---

# 5. Advanced Arithmetic Operators

### Modulo Operator `%`
Returns **remainder of division**.

```python
a = 56
b = 12

print(a % b)  # 8
```

---

### Floor Division `//`
Returns the **largest integer less than or equal to division result**.

```python
a = 56
b = 12

print(a // b)  # 4
```

---

### Exponentiation `**`
Raises number to the power of another.

```python
print(2 ** 3)  # 8
```

---

# 6. Float Precision Issue

Some decimal numbers cannot be represented exactly in binary.

Example:

```python
print(0.1 + 0.2)
```

Output:

```
0.30000000000000004
```

Reason:
- Floating-point numbers are stored in **binary approximation**
- Small **rounding errors** occur

---

# 7. Type Conversion

Python provides functions to convert data types.

### Convert to Float

```python
num = 56
float_num = float(num)

print(float_num)       # 56.0
print(type(float_num)) # float
```

---

### Convert to Integer

```python
num = 12.92563
int_num = int(num)

print(int_num)  # 12
```

⚠️ `int()` **removes the decimal part**, it does not round.

---

### Convert String to Number

```python
str_int = "45"
str_float = "7.8"

num1 = int(str_int)
num2 = float(str_float)

print(num1, type(num1))
print(num2, type(num2))
```

---

# 8. Useful Built-in Numeric Functions

### round()

Rounds number to specified decimal places.

```python
print(round(4.798))     # 5
print(round(4.253, 1))  # 4.3
```

---

### abs()

Returns **absolute value** (distance from zero).

```python
print(abs(-15))  # 15
```

---

### pow()

Raises a number to a power.

```python
print(pow(2, 3))  # 8
```

Also supports **modular exponentiation**:

```python
print(pow(2, 3, 5))  # (2**3) % 5 = 3
```

---

# Key Points to Remember

- `int` → whole numbers  
- `float` → decimal numbers  
- `/` division always returns **float**
- `//` → floor division
- `%` → remainder
- `**` → exponent
- Mixing `int` and `float` → result is **float**
- Floating numbers may have **precision errors**
- `int()` removes decimal part
- `round()` rounds number
- `abs()` returns positive value
```




# Augmented Assignment in Python

## Concept
Augmented assignment combines an **operation + assignment** in one step.

General Syntax:

```python
variable <operator>= value
```

Equivalent to:

```python
variable = variable <operator> value
```

Advantage:
- Shorter and cleaner code
- Avoids repeating variable names
- Reduces chances of typing errors

---

# Common Augmented Assignment Operators

## 1. Addition Assignment (`+=`)
Adds value to the variable and stores result.

```python
my_var = 10
my_var += 5

print(my_var)  # 15
```

Equivalent:

```python
my_var = my_var + 5
```

---

## 2. Subtraction Assignment (`-=`)
Subtracts value from variable.

```python
count = 14
count -= 3

print(count)  # 11
```

---

## 3. Multiplication Assignment (`*=`)
Multiplies variable by value.

```python
product = 65
product *= 7

print(product)  # 455
```

---

## 4. Division Assignment (`/=`)
Divides variable by value.

```python
price = 100
price /= 4

print(price)  # 25.0
```

Note:
- Result becomes **float**.

---

## 5. Floor Division Assignment (`//=`)
Divides and keeps **integer part only**.

```python
total_pages = 23
total_pages //= 5

print(total_pages)  # 4
```

---

## 6. Modulo Assignment (`%=`)
Stores the **remainder** after division.

```python
bits = 35
bits %= 2

print(bits)  # 1
```

---

## 7. Exponentiation Assignment (`**=`)
Raises variable to the power of value.

```python
power = 2
power **= 3

print(power)  # 8
```

---

# Augmented Assignment with Strings

## String Concatenation (`+=`)

```python
greet = "Hello"
greet += " World"

print(greet)  # Hello World
```

---

## String Repetition (`*=`)

```python
greet = "Hello"
greet *= 3

print(greet)  # HelloHelloHello
```

---

# Invalid Operations with Strings

These operators **do NOT work with strings**:

- `-=`
- `/=`

Example:

```python
greet = "Hello"
greet -= " World"   # TypeError
```

```python
greet = "Hello"
greet /= "World"    # TypeError
```

---

# Increment & Decrement in Python

Python **does NOT support**:

```
x++
x--
```

Instead use:

```python
x += 1
```

Example:

```python
my_var = 5
my_var += 1

print(my_var)  # 6
```

---

# Important Note About `++`

`++x` does NOT increment in Python.

It only applies unary plus multiple times.

```python
my_var = 5

print(+my_var)   # 5
print(++my_var)  # 5
print(+++my_var) # 5
```

No change occurs.

---

# Key Points to Remember

- Augmented assignment = **operation + assignment**
- Makes code **shorter and cleaner**
- Works with numbers and some strings
- Python **does not support ++ or -- operators**
- Use `+= 1` to increment values
