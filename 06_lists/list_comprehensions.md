# List Comprehension and Useful List Functions

## List Comprehension

**List comprehension** is a shorter way to create lists using a **loop and condition in one line**.

### Basic Syntax

```python
[expression for item in iterable if condition]
```

### Example (Traditional Loop)

```python
even_numbers = []

for num in range(21):
    if num % 2 == 0:
        even_numbers.append(num)

print(even_numbers)
```

### Same Using List Comprehension

```python
even_numbers = [num for num in range(21) if num % 2 == 0]

print(even_numbers)
```

Advantages:
- Shorter code
- More readable
- Faster in many cases

---

# Conditional List Comprehension

You can also use **if-else expressions** inside list comprehensions.

```python
numbers = [1,2,3,4,5]

result = [(num,'Even') if num % 2 == 0 else (num,'Odd') for num in numbers]

print(result)

# [(1,'Odd'), (2,'Even'), (3,'Odd'), (4,'Even'), (5,'Odd')]
```

---

# filter() Function

`filter()` selects elements from an iterable based on a **condition function**.

### Syntax

```python
filter(function, iterable)
```

### Example

```python
words = ['tree','sky','mountain','river','cloud','sun']

def is_long_word(word):
    return len(word) > 4

long_words = list(filter(is_long_word, words))

print(long_words)
# ['mountain','river','cloud']
```

Purpose:
- Extract elements that satisfy a condition

---

# map() Function

`map()` applies a function to **every element in an iterable**.

### Syntax

```python
map(function, iterable)
```

### Example

```python
celsius = [0,10,20,30,40]

def to_fahrenheit(temp):
    return (temp * 9/5) + 32

fahrenheit = list(map(to_fahrenheit, celsius))

print(fahrenheit)
# [32.0, 50.0, 68.0, 86.0, 104.0]
```

Purpose:
- Transform data in a list

---

# sum() Function

`sum()` returns the **total of all elements in an iterable**.

### Basic Example

```python
numbers = [5,10,15,20]

total = sum(numbers)

print(total)  # 50
```

### With Start Value

```python
numbers = [5,10,15,20]

total = sum(numbers, 10)

print(total)  # 60
```

---

# Key Points

- **List comprehension** creates lists in one line using loops.
- **filter()** selects elements based on a condition.
- **map()** applies a function to each element.
- **sum()** calculates the total of numbers in an iterable.
