# Python Loops — Important Key Points

## What are Loops?

Loops are used to **repeat a block of code multiple times**.

Python mainly has two loops:

- `for` loop
- `while` loop

---

# 1. For Loop

Used to **iterate over an iterable** (list, string, tuple, etc).

```python
languages = ['Rust', 'Java', 'Python']

for lang in languages:
    print(lang)
```

### Iterate Through String

```python
for char in "code":
    print(char)
```

### Important
- Loop body **must be indented**
- Otherwise → `IndentationError`

---

# 2. Nested For Loop

A loop **inside another loop**.

```python
categories = ['Fruit', 'Vegetable']
foods = ['Apple', 'Carrot']

for category in categories:
    for food in foods:
        print(category, food)
```

Outer loop runs first, inner loop runs completely each time.

---

# 3. While Loop

Runs **until the condition becomes False**.

```python
secret_number = 3
guess = 0

while guess != secret_number:
    guess = int(input("Guess number: "))
```

Used when **number of iterations is unknown**.

---

# 4. Break Statement

`break` **stops the loop immediately**.

```python
names = ['Jess', 'Naomi', 'Tom']

for name in names:
    if name == 'Naomi':
        break
    print(name)
```

---

# 5. Continue Statement

`continue` **skips the current iteration** and moves to the next.

```python
names = ['Jess', 'Naomi', 'Tom']

for name in names:
    if name == 'Naomi':
        continue
    print(name)
```

---

# 6. Loop with Else

`else` runs **only if the loop finishes normally (no break)**.

```python
for i in range(3):
    print(i)
else:
    print("Loop finished")
```

---

# Key Points

- Loops repeat code execution
- `for` → iterate through sequences
- `while` → runs until condition becomes False
- `break` → stops loop
- `continue` → skips current iteration
- Loops can be **nested**
- `else` runs if loop **does not break**

  # Python range() — Important Notes

## What is range()

`range()` is used to **generate a sequence of integers**, mainly used in **loops**.

Basic syntax:

```python
range(start, stop, step)
```

- **start** → starting number (optional, default = 0)
- **stop** → ending number (**not included**)
- **step** → increment/decrement value (optional, default = 1)

---

# Basic Example

```python
for num in range(3):
    print(num)
```

Output

```
0
1
2
```

`3` is **not included** because the stop value is **exclusive**.

---

# Using Start and Stop

```python
for num in range(1,5):
    print(num)
```

Output

```
1
2
3
4
```

---

# Using Step

Step controls how much the number increases.

```python
for num in range(2,11,2):
    print(num)
```

Output

```
2
4
6
8
10
```

---

# Negative Step (Reverse Loop)

Use a **negative step** to count backwards.

```python
for num in range(40,0,-10):
    print(num)
```

Output

```
40
30
20
10
```

---

# Creating a List Using range()

`range()` can be converted into a list.

```python
numbers = list(range(2,11,2))

print(numbers)
```

Output

```
[2,4,6,8,10]
```

---

# Important Rules

- `range()` requires **at least one argument**
- Arguments must be **integers**
- **Stop value is always excluded**

Example Errors:

```python
range()      # TypeError (no argument)

range(1.5)   # TypeError (float not allowed)
```

---

# Key Points

- `range()` generates **integer sequences**
- Mostly used with **for loops**
- Default values → `start=0`, `step=1`
- Stop value is **not included**
- Can generate **ascending or descending sequences**
- Can convert to list using `list(range())`
