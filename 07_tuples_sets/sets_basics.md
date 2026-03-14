## What is a Set?

A **set** is a built-in Python data structure used to store **unique elements**.

Features:
- **No duplicate values**
- **Unordered** (no indexing)
- **Mutable**
- Stores **immutable values** (numbers, strings, tuples)

```python
my_set = {1, 2, 3, 4, 5}
```

---

# Creating an Empty Set

Use `set()` to create an empty set.

```python
s = set()   # empty set
d = {}      # dictionary
```

---

# Adding Elements

Use `.add()` method.

```python
my_set = {1,2,3}

my_set.add(4)

print(my_set)   # {1,2,3,4}
```

Duplicate values are ignored.

```python
my_set.add(3)   # no change
```

---

# Removing Elements

### remove()

Raises error if element not found.

```python
my_set.remove(2)
```

### discard()

No error if element not found.

```python
my_set.discard(2)
```

---

# Clearing a Set

Remove all elements.

```python
my_set.clear()
```

---

# Membership Check

Use `in`.

```python
my_set = {1,2,3,4}

print(3 in my_set)  # True
print(6 in my_set)  # False
```

---

# Set Operations

```python
my_set = {1,2,3,4,5}
your_set = {2,3,4,6}
```

### Union (all elements)

```python
my_set | your_set
# {1,2,3,4,5,6}
```

---

### Intersection (common elements)

```python
my_set & your_set
# {2,3,4}
```

---

### Difference (elements in first but not second)

```python
my_set - your_set
# {1,5}
```

---

### Symmetric Difference

Elements in **either set but not both**.

```python
my_set ^ your_set
# {1,5,6}
```

---

# Compound Assignment Operators

Update the first set.

```python
my_set |= your_set
my_set &= your_set
my_set -= your_set
my_set ^= your_set
```

Example:

```python
my_set -= your_set

print(my_set)  # {1,5}
```

---

# Subset and Superset

### Subset

```python
your_set.issubset(my_set)
```

### Superset

```python
my_set.issuperset(your_set)
```

---

# Disjoint Sets

Check if sets have **no common elements**.

```python
my_set.isdisjoint(your_set)
```

---

# Key Points

- Sets store **unique values**
- **Unordered → no indexing**
- Created using `{}` or `set()`
- Use `.add()` to insert elements
- Use `.remove()` or `.discard()` to delete
- Support **mathematical operations** like union, intersection, difference
- Useful when working with **unique data**
