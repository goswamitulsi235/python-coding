## enumerate()

- Used to **get index and value while looping**
- Removes the need for manually creating an index variable
- Returns **(index, value) tuples**

```python
languages = ['Spanish', 'English', 'Russian']

for index, language in enumerate(languages):
    print(index, language)
```

### Start Index Option

- Default index starts from **0**
- Can change starting index

```python
for index, language in enumerate(languages, 1):
    print(index, language)
```

---

# zip()

- Used to **iterate over multiple lists together**
- Combines elements into **tuples**
- Stops when the **shortest iterable ends**

```python
developers = ['Naomi','Dario','Jessica']
ids = [1,2,3]

for name, id in zip(developers, ids):
    print(name, id)
```

---

# Key Takeaways

- `enumerate()` → loop with **index + value**
- `zip()` → loop through **multiple lists simultaneously**
- Both functions make loops **cleaner and more readable**
