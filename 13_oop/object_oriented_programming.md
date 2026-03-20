# OOP & Encapsulation (Very Short Notes)

## 🔑 OOP Basics
- OOP = programming using objects (real-world)
- Class = blueprint | Object = instance
- Attributes = data | Methods = behavior

## 🔒 Encapsulation
- Bundle data + methods in a class
- Hide internal data, control via methods

## ⚡ Access Levels
- `_var` → protected (convention)
- `__var` → private (restricted)

## 🚀 Key Idea
- ❌ Direct access → avoid
- ✅ Use methods → safe control

## ✅ Example
```python
class Wallet:
    def __init__(self, balance):
        self.__balance = balance

    def deposit(self, amt):
        if amt > 0:
            self.__balance += amt

    def get_balance(self):
        return self.__balance

w = Wallet(100)
w.deposit(50)
print(w.get_balance())  # 150
