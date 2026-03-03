# Variables & Naming Conventions in Python

## 1. What is a Variable?

A variable is a named container used to store data.

In Python, variables are created using the assignment operator (=).

No special keyword like `let` or `const` is required.

---

## 2. Basic Syntax

variable_name = value

Example:

name = "John Doe"
age = 25

- Left side → variable name
- = → assignment operator
- Right side → value stored

---

## 3. Strings in Variables

Strings are text values written inside quotes.

Single quotes:
'Hello'

Double quotes:
"Hello"

Example:

name = "Tulsi"
city = 'Indore'

---

## 4. Rules for Naming Variables

✔ Must start with:
- A letter (a-z, A-Z)
- Or underscore (_)

❌ Cannot start with a number:
5name = "Tulsi"   # SyntaxError

✔ Can contain:
- Letters
- Numbers
- Underscores

❌ Cannot use Python reserved keywords:
if, class, def, etc.

✔ Case-sensitive:
age = 23
Age = 30
These are different variables.

---

## 5. Naming Conventions (Best Practices)

1. Use snake_case (lowercase + underscores)
user_name = "Tulsi"

2. Use descriptive names
user_age = 23     # Good
ua = 23           # Avoid

3. Avoid single-letter names
x = 10   # Not meaningful

Exception:
In loops, i, j, k are acceptable.

---

## 6. Comments in Python

Comments start with #

Example:
# This is a comment
```python
Multi-line comment:
# Line 1
# Line 2
# Line 3
```

Python ignores everything after # on that line.

Use comments to:
- Explain logic
- Add reminders
- Clarify complex code

Do NOT use comments to explain bad variable names.
Instead, use better variable names.

---

## 7. Common Mistakes

- Starting variable with number
- Using reserved keywords
- Using unclear names (x, a1, temp1)
- Confusing uppercase and lowercase

---

## 8. Key Points to Remember

- Variables store data.
- No keyword needed to declare variables.
- Use snake_case naming.
- Variable names must follow rules.
- Python is case-sensitive.

