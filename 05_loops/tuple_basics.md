# Python Tuples — Important Notes

## What is a Tuple?

A **tuple** is an **ordered collection of elements**.

- Can contain **mixed data types**
- **Immutable** → values cannot be changed after creation
- Uses **zero-based indexing**

```python
developer = ('Alice', 34, 'Rust Developer')
```

---

# List vs Tuple

| Feature | List | Tuple |
|------|------|------|
| Mutability | Mutable | Immutable |
| Modification | Allowed | Not Allowed |
| Syntax | `[]` | `()` |

---

# Accessing Tuple Elements

Use **indexing**.

```python
developer = ('Alice', 34, 'Rust Developer')

print(developer[1])  # 34
```

### Negative Index

```python
numbers = (1,2,3,4,5)

print(numbers[-2])  # 4
```

Invalid index → **IndexError**

---

# Creating Tuple using tuple()

Convert an **iterable** into a tuple.

```python
name = "Jessica"

print(tuple(name))
# ('J','e','s','s','i','c','a')
```

---

# Checking Element in Tuple

Use `in`.

```python
languages = ('Python','Java','C++','Rust')

print('Rust' in languages)        # True
print('JavaScript' in languages)  # False
```

---

# Tuple Unpacking

Assign tuple values to variables.

```python
developer = ('Alice',34,'Rust Developer')

name, age, job = developer
```

Using `*` for remaining elements.

```python
name, *rest = developer

print(name)  # Alice
print(rest)  # [34,'Rust Developer']
```

---

# Tuple Slicing

Extract part of a tuple.

```python
desserts = ('cake','pie','cookies','ice cream')

print(desserts[1:3])
# ('pie','cookies')
```

Format:

```
tuple[start:end]
```

---

# Tuple Immutability

Tuples **cannot be modified or deleted**.

```python
languages = ('Python','Java','C++')

languages[0] = 'JavaScript'   # TypeError
```

```python
del languages[1]   # TypeError
```

---

# When to Use Tuple vs List

Use **List** when:
- Data needs to **change**
- Add/remove/update elements

Use **Tuple** when:
- Data should remain **fixed**
- **Immutable collection**


# Tuple Methods — Important Notes

## Tuples in Python

A **tuple** is an **ordered and immutable sequence** of elements.

- Uses **parentheses ()**
- Elements **cannot be modified after creation**
- Supports indexing and slicing like lists

```python
languages = ('Python', 'Java', 'Rust')
```

---

# 1. count() Method

Used to **count how many times an element appears** in a tuple.

```python
languages = ('Rust', 'Java', 'Python', 'C++', 'Rust')

print(languages.count('Rust'))  # 2
```

If element does not exist:

```python
print(languages.count('JavaScript'))  # 0
```

If no argument is given → **TypeError**

---

# 2. index() Method

Used to **find the index of an element** in a tuple.

```python
languages = ('Rust', 'Java', 'Python', 'C++')

print(languages.index('Java'))  # 1
```

If element does not exist → **ValueError**

---

## index() with Start Position

Search starting from a specific index.

```python
languages = ('Rust', 'Java', 'Python', 'C++', 'Rust', 'Python')

print(languages.index('Python', 3))  # 5
```

---

## index() with Start and Stop

Limit the search range.

```python
languages = ('Rust','Java','Python','C++','Rust','Python','JavaScript','Python')

print(languages.index('Python', 2, 5))  # 2
```

Format:

```
tuple.index(value, start, stop)
```

---

# 3. sorted() Function

Used to **sort elements of a tuple**.

- Returns a **new list**
- Does **not modify the tuple**

```python
numbers = (13,2,78,3,45,67,18,7)

print(sorted(numbers))
# [2,3,7,13,18,45,67,78]
```

---

# Sorting with key

Customize sorting logic.

Example: **sort by length**

```python
languages = ('Rust','Java','Python','C++')

print(sorted(languages, key=len))
# ['C++','Rust','Java','Python']
```

---

# Sorting in Reverse

```python
languages = ('Rust','Java','Python','C++')

print(sorted(languages, reverse=True))
```

---

# Key Points

- Tuples are **ordered and immutable**
- `count()` → counts occurrences of an element
- `index()` → finds position of element
- `index(value, start, stop)` → search in a range
- `sorted()` → returns a **new sorted list**
- `reverse=True` → sorts in descending order
- `key` → custom sorting logic
