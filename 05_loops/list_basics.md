# Python Lists — Important Notes

## What is a List?

A **list** is an **ordered collection of elements**.

- Can store **strings, numbers, or other lists**
- **Mutable** → values can be changed
- Uses **zero-based indexing**

```python
cities = ['Los Angeles', 'London', 'Tokyo']
```

---

# Accessing Elements

### Positive Index

```python
cities = ['Los Angeles', 'London', 'Tokyo']

print(cities[0])  # Los Angeles
```

### Negative Index

Access elements from the **end of the list**.

```python
print(cities[-1])  # Tokyo
```

---

# Creating Lists with list()

Convert an **iterable** into a list.

```python
developer = "Jessica"

print(list(developer))
# ['J','e','s','s','i','c','a']
```

---

# Length of List

Use `len()` to count elements.

```python
numbers = [1,2,3,4,5]

print(len(numbers))  # 5
```

---

# Updating Elements (Mutable)

Lists allow modification.

```python
languages = ['Python','Java','C++']

languages[0] = 'JavaScript'

print(languages)
# ['JavaScript','Java','C++']
```

If index is invalid → **IndexError**

---

# Deleting Elements

Use `del`.

```python
developer = ['Jane Doe',23,'Python Developer']

del developer[1]

print(developer)
# ['Jane Doe','Python Developer']
```

---

# Checking if Element Exists

Use `in`.

```python
languages = ['Python','Java','Rust']

print('Rust' in languages)        # True
print('JavaScript' in languages)  # False
```

---

# Nested Lists

Lists can contain **other lists**.

```python
developer = ['Alice',25,['Python','Rust','C++']]

print(developer[2])     # ['Python','Rust','C++']
print(developer[2][1])  # Rust
```

---

# List Unpacking

Assign list values to variables.

```python
developer = ['Alice',34,'Rust Developer']

name, age, job = developer
```

Using `*` to collect remaining values:

```python
name, *rest = developer

print(name)  # Alice
print(rest)  # [34,'Rust Developer']
```

---

# List Slicing

Extract part of a list.

```python
desserts = ['Cake','Cookies','Ice Cream','Pie','Brownies']

print(desserts[1:4])
# ['Cookies','Ice Cream','Pie']
```

Format:

```
list[start:end]
```

---

# Slicing with Step

```python
numbers = [1,2,3,4,5,6]

print(numbers[1::2])
# [2,4,6]
```

Format:

```
list[start:end:step]
```

---

# Key Points

- Lists are **ordered and mutable**
- Use **indexing** to access elements
- Use **negative index** for reverse access
- `len()` → number of elements
- `del` → remove element
- `in` → check membership
- Lists support **nesting**
- **Unpacking** assigns list values to variables
- **Slicing** extracts portions of lists

# Python List Methods — Important Notes

## 1. append()

Adds an element **to the end of the list**.

```python
numbers = [1,2,3,4,5]
numbers.append(6)

print(numbers)
# [1,2,3,4,5,6]
```

If you append another list → it becomes a **nested list**.

```python
numbers = [1,2,3]
even = [4,6]

numbers.append(even)

print(numbers)
# [1,2,3,[4,6]]
```

---

# 2. extend()

Adds **each element of another list** to the end.

```python
numbers = [1,2,3]
even = [4,6]

numbers.extend(even)

print(numbers)
# [1,2,3,4,6]
```

Difference:

- `append()` → adds list as **single element**
- `extend()` → adds **elements individually**

---

# 3. insert()

Insert an element at a **specific index**.

```python
numbers = [1,2,3,4]

numbers.insert(2,2.5)

print(numbers)
# [1,2,2.5,3,4]
```

Format:

```
list.insert(index, value)
```

---

# 4. remove()

Removes **first occurrence of a value**.

```python
numbers = [10,20,30,40,50,50]

numbers.remove(50)

print(numbers)
# [10,20,30,40,50]
```

Only removes **first match**, not all.

---

# 5. pop()

Removes element **by index** and **returns it**.

```python
numbers = [1,2,3,4,5]

numbers.pop(1)

print(numbers)
# [1,3,4,5]
```

Without index → removes **last element**.

```python
numbers.pop()
# removes 5
```

---

# 6. clear()

Removes **all elements from the list**.

```python
numbers = [1,2,3]

numbers.clear()

print(numbers)
# []
```

---

# 7. sort()

Sorts the list **in place** (modifies original list).

```python
numbers = [19,2,35,1,67]

numbers.sort()

print(numbers)
# [1,2,19,35,67]
```

---

# 8. sorted()

Returns a **new sorted list** without changing the original.

```python
numbers = [19,2,35,1,67]

sorted_numbers = sorted(numbers)

print(numbers)
# [19,2,35,1,67]

print(sorted_numbers)
# [1,2,19,35,67]
```

Difference:

- `sort()` → modifies original list
- `sorted()` → creates new list

---

# 9. reverse()

Reverses list **in place**.

```python
numbers = [6,5,4,3,2,1]

numbers.reverse()

print(numbers)
# [1,2,3,4,5,6]
```

---

# 10. index()

Finds the **first index of an element**.

```python
languages = ['Rust','Java','Python','C++']

print(languages.index('Java'))
# 1
```

If element not found → **ValueError**

---

# Key Points

- `append()` → add single element
- `extend()` → add multiple elements
- `insert()` → add element at index
- `remove()` → remove by value
- `pop()` → remove by index
- `clear()` → remove all elements
- `sort()` → sort original list
- `sorted()` → returns new sorted list
- `reverse()` → reverse list
- `index()` → find position of element
