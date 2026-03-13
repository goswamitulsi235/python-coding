## What is a Dictionary?

A **dictionary** is a built-in Python data structure used to store **key–value pairs**.

- Each **key maps to a value**
- Keys must be **unique**
- Keys must be **immutable**
- Values can be **any data type**
- Used for **fast lookup using keys**

### Basic Syntax

```python
dictionary = {
    key1: value1,
    key2: value2
}
```

### Example

```python
pizza = {
    "name": "Margherita Pizza",
    "price": 8.9,
    "calories_per_slice": 250,
    "toppings": ["mozzarella", "basil"]
}
```

---

# Creating Dictionary using dict()

```python
pizza = dict([
    ("name","Margherita Pizza"),
    ("price",8.9),
    ("calories_per_slice",250)
])
```

---

# Accessing Values

Use **bracket notation** with the key.

```python
pizza["name"]
# 'Margherita Pizza'
```

---

# Updating Values

```python
pizza["name"] = "Margherita"

print(pizza["name"])
# Margherita
```

If the key **does not exist**, Python creates a **new key-value pair**.

---

# get() Method

Used to access values **without causing an error** if key is missing.

```python
pizza.get("toppings", [])
```

---

# Dictionary Methods

### keys()

Returns all keys.

```python
pizza.keys()
```

### values()

Returns all values.

```python
pizza.values()
```

### items()

Returns key-value pairs.

```python
pizza.items()
```

---

# Removing Elements

### clear()

Removes all items.

```python
pizza.clear()
```

### pop()

Removes a specific key.

```python
pizza.pop("price",10)
```

### popitem()

Removes **last inserted item**.

```python
pizza.popitem()
```

---

# Updating Dictionary

Use `.update()` to merge dictionaries.

```python
pizza.update({
    "price": 15,
    "total_time": 25
})
```

---

# Key Points

- Dictionaries store **key-value pairs**
- Keys must be **unique & immutable**
- Values can be **any type**
- Use **[] or .get()** to access values
- `.keys()`, `.values()`, `.items()` for viewing data
- `.pop()`, `.popitem()`, `.clear()` for deletion
- `.update()` for modifying dictionaries
