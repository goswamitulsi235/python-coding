# Lambda Functions — Key Points

- **Lambda functions** are **anonymous (nameless) functions**.
- Used for **short, one-line functions**.
- Defined using the **`lambda` keyword**.
- Syntax:

```python
lambda arguments: expression
```

Example:

```python
square = lambda x: x**2
print(square(4))  # 16
```

---

# Common Use

Mostly used with **higher-order functions** like:

- `map()`
- `filter()`
- `sorted()`

Example:

```python
numbers = [1,2,3,4,5]

even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
```

---

# Important Rules

- Lambda functions contain **only one expression**.
- They **automatically return the result**.
- Best used for **small temporary operations**.

---

# Best Practices

✔ Use lambda for **simple inline logic**
Avoid assigning lambda to variables (use `def` instead)
Avoid complex lambda expressions (hard to read)

---

# When to Use Lambda

Use lambda when:

- Function is **very small**
- Used **only once**
- Used inside functions like `map()` or `filter()`

Otherwise → use **regular functions (`def`)**
