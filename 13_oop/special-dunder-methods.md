# Special Methods (Magic / Dunder Methods)

## 🔑 Key Points
- Special methods = methods with `__name__` (dunder)
- Python automatically calls them (you don’t call directly)
- Used to **customize behavior of objects**

## ⚙️ Common Examples
- `__init__()` → constructor
- `__add__()` → +
- `__len__()` → len()
- `__str__()` → print()
- `__eq__()` → ==
- `__iter__()` → loops
- `__next__()` → next item

## 🧠 Why Needed?
- Default objects:
  - ❌ no len()
  - ❌ ugly print
  - ❌ compares memory, not values
- Special methods fix this

## ✅ Example (Book Class)

```python
class Book:
    def __init__(self, title, pages):
        self.title = title
        self.pages = pages

    def __len__(self):
        return self.pages

    def __str__(self):
        return f"{self.title} - {self.pages} pages"

    def __eq__(self, other):
        return self.pages == other.pages
