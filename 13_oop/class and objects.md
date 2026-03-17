# Python Notes — Classes & Objects

## What is a Class?
A **class** is a blueprint/template used to create objects.  
It defines:
- **Attributes (data)**
- **Methods (functions/behavior)**

---

## Basic Syntax

```python
class ClassName:
    def __init__(self, attr1, attr2):
        self.attr1 = attr1
        self.attr2 = attr2

    def method_name(self):
        # action
        pass
```

---

## Key Concepts

### 1. `__init__` Method
- Special method (constructor)
- Automatically called when object is created
- Used to initialize attributes

```python
def __init__(self, name, age):
    self.name = name
    self.age = age
```

---

### 2. `self`
- Refers to the **current object**
- Used to access attributes & methods inside class

---

### 3. Attributes
- Variables inside a class
- Store object data

```python
self.name = name
self.age = age
```

---

### 4. Methods
- Functions inside a class
- Define object behavior

```python
def sample_method(self):
    print(self.name.upper())
```

---

## Example: Class

```python
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def bark(self):
        print(f"{self.name.upper()} says woof woof!")
```

---

## Creating Objects

```python
dog_1 = Dog("Jack", 3)
dog_2 = Dog("Thatcher", 5)
```

---

## Calling Methods

```python
dog_1.bark()
dog_2.bark()
```

Full Example:

```python
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def bark(self):
        print(f"{self.name.upper()} says woof woof! I'm {self.age} years old!")

dog_1 = Dog("Jack", 3)
dog_2 = Dog("Thatcher", 5)

dog_1.bark()
dog_2.bark()
```

---

## Output

```
JACK says woof woof! I'm 3 years old!
THATCHER says woof woof! I'm 5 years old!
```

---

## Class vs Object

| Class | Object |
|------|--------|
| Blueprint/template | Actual instance |
| Defines structure | Holds real data |
| Written once | Created many times |
| No real values | Has actual values |

---

## Key Points

- Class = blueprint, Object = instance
- `__init__` initializes object data
- `self` refers to current object
- Attributes store data, methods define behavior
- One class → multiple objects with different values
