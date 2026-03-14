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

  # Looping Over Dictionaries — Important Notes

## Dictionary Example

```python
products = {
    'Laptop': 990,
    'Smartphone': 600,
    'Tablet': 250,
    'Headphones': 70
}
```

---

# 1. Loop Over Values

Use `.values()` to iterate through **all values**.

```python
for price in products.values():
    print(price)
```

Output

```
990
600
250
70
```

---

# 2. Loop Over Keys

Use `.keys()` or directly iterate over dictionary.

```python
for product in products.keys():
    print(product)

# OR

for product in products:
    print(product)
```

Output

```
Laptop
Smartphone
Tablet
Headphones
```

---

# 3. Loop Over Key-Value Pairs

Use `.items()` to get **key and value together**.

```python
for product in products.items():
    print(product)
```

Output

```
('Laptop', 990)
('Smartphone', 600)
('Tablet', 250)
('Headphones', 70)
```

---

# 4. Store Key and Value in Separate Variables

```python
for product, price in products.items():
    print(product, price)
```

Output

```
Laptop 990
Smartphone 600
Tablet 250
Headphones 70
```

---

# 5. Updating Dictionary Values While Looping

Example: **20% discount**

```python
for product, price in products.items():
    products[product] = round(price * 0.8)

print(products)
```

Output

```
{
 'Laptop': 792,
 'Smartphone': 480,
 'Tablet': 200,
 'Headphones': 56
}
```

---

# 6. Using enumerate() With Dictionary

`enumerate()` adds a **counter (index)** to each iteration.

```python
for index, product in enumerate(products):
    print(index, product)
```

Output

```
0 Laptop
1 Smartphone
2 Tablet
3 Headphones
```

---

# 7. enumerate() With Values

```python
for index, price in enumerate(products.values()):
    print(index, price)
```

Output

```
0 990
1 600
2 250
3 70
```

---

# 8. enumerate() With Key-Value Pairs

```python
for index, item in enumerate(products.items()):
    print(index, item)
```

Output

```
0 ('Laptop', 990)
1 ('Smartphone', 600)
2 ('Tablet', 250)
3 ('Headphones', 70)
```

---

# 9. Custom Start Index in enumerate()

```python
for index, item in enumerate(products.items(), 1):
    print(index, item)
```

Output

```
1 ('Laptop', 990)
2 ('Smartphone', 600)
3 ('Tablet', 250)
4 ('Headphones', 70)
```

---

# Key Points

- `.keys()` → iterate over **keys**
- `.values()` → iterate over **values**
- `.items()` → iterate over **key-value pairs**
- `enumerate()` → adds **counter/index**
- Can **update dictionary values inside loop**
