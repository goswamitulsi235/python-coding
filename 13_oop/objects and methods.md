# Python Notes — Attributes & Methods

## Attributes
- Variables that store data in a class/object
- Types:
  - **Instance attributes** → unique per object (`self.variable`)
  - **Class attributes** → shared by all objects

```python
class Dog:
    species = "French Bulldog"  # Class attribute

    def __init__(self, name):
        self.name = name  # Instance attribute
```

Access:
```python
dog = Dog("Jack")
print(dog.name)     # Instance
print(dog.species)  # Class
print(Dog.species)  # Direct class access
```

---

## Methods
- Functions inside a class
- Used to **perform actions on object data**
- Accessed using dot notation

```python
class Dog:
    def __init__(self, name):
        self.name = name

    def bark(self):
        return f"{self.name} says woof!"
```

```python
dog = Dog("Jack")
print(dog.bark())
```

---

## Key Points
- Attributes = data, Methods = behavior
- `self` refers to the current object
- Instance attributes → different for each object
- Class attributes → same for all objects
- Methods operate on object’s data
- Use dot (`.`) to access both
