# Getters & Setters (Python)

## 🔑 Key Points
- Getter → get value
- Setter → set/update value (with validation)
- Property → use methods like attributes (`obj.attr`)
- Use `@property`, `@x.setter`, `@x.deleter`

## ⚡ Example
```python
class Circle:
    def __init__(self, radius):
        self.radius = radius   # calls setter

    # Getter
    @property
    def radius(self):
        return self._radius

    # Setter
    @radius.setter
    def radius(self, value):
        if value <= 0:
            raise ValueError("Must be positive")
        self._radius = value

    # Deleter
    @radius.deleter
    def radius(self):
        print("Deleted")
        del self._radius


c = Circle(5)

# Getter
print(c.radius)      # 5

# Setter
c.radius = 10

# Deleter
del c.radius
