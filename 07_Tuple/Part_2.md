# 🔧 Common Tuple Methods in Python

Unlike lists, tuples have only **two built-in methods** because tuples are **immutable** (their values cannot be changed).

The two methods are:

1. `count()`
2. `index()`

---

# 1️⃣ count()

## 📖 What is count()?

The `count()` method counts how many times a particular value appears in a tuple.

---

## 🌍 Real-World Example

Imagine a teacher wants to know how many students selected **Python** as their favorite programming language.

Instead of counting manually, Python can count it automatically.

---

## 📝 Syntax

```python
tuple_name.count(value)
```

---

## 💻 Example

```python
languages = ("Python", "Java", "Python", "C++", "Python")

print(languages.count("Python"))
```

### Output

```
3
```

---

# 2️⃣ index()

## 📖 What is index()?

The `index()` method returns the position of a value inside a tuple.

---

## 🌍 Real-World Example

Suppose you want to know the position of a student's name in the attendance list.

---

## 📝 Syntax

```python
tuple_name.index(value)
```

---

## 💻 Example

```python
students = ("Gokul", "Rahul", "Priya", "Arun")

print(students.index("Priya"))
```

### Output

```
2
```

---

# 📦 Tuple Packing

## 📖 What is Tuple Packing?

Tuple Packing means storing multiple values into one tuple.

Python automatically packs all the values into a tuple.

---

## 💻 Example

```python
student = "Gokul", 20, "AIML"

print(student)
```

### Output

```
('Gokul', 20, 'AIML')
```

Python automatically creates the tuple.

---

# 📦 Tuple Unpacking

## 📖 What is Tuple Unpacking?

Tuple Unpacking means assigning each value of a tuple to a separate variable.

---

## 🌍 Real-World Example

Imagine a student registration form.

The system stores:

- Name
- Age
- Department

Later, we need to use each value separately.

Tuple unpacking makes this easy.

---

## 💻 Example

```python
student = ("Gokul", 20, "AIML")

name, age, department = student

print(name)
print(age)
print(department)
```

### Output

```
Gokul
20
AIML
```

---

# 📦 Nested Tuple

## 📖 What is a Nested Tuple?

A Nested Tuple is a tuple inside another tuple.

---

## 🌍 Real-World Example

Suppose a college stores details of multiple students.

Each student's information is stored as one tuple.

All student tuples are stored inside another tuple.

---

## 💻 Example

```python
students = (
    ("Gokul", 20),
    ("Rahul", 21),
    ("Priya", 19)
)

print(students)
```

### Output

```
(('Gokul', 20), ('Rahul', 21), ('Priya', 19))
```

---

## 💻 Accessing Nested Tuple Elements

```python
students = (
    ("Gokul", 20),
    ("Rahul", 21),
    ("Priya", 19)
)

print(students[1][0])
```

### Output

```
Rahul
```

---

# 📊 Difference Between List and Tuple

| List | Tuple |
|------|-------|
| Uses square brackets `[]` | Uses parentheses `()` |
| Mutable (can be changed) | Immutable (cannot be changed) |
| Can add or remove elements | Cannot add or remove elements |
| More flexible | More secure for fixed data |
| Has many methods | Has only two methods |

---

# 🌍 When Should You Use a List?

Use a List when:

- Data changes frequently.
- You need to add new elements.
- You need to remove elements.
- You need to update values.

### Example

Shopping Cart

```
Laptop
Mouse
Keyboard
```

Customers can add or remove products at any time.

So, List is the correct choice.

---

# 🌍 When Should You Use a Tuple?

Use a Tuple when:

- Data should never change.
- The values are fixed.
- You want to protect important information.

### Example

- Date of Birth
- Aadhaar Number
- Passport Number
- GPS Coordinates
- RGB Color Values

These values usually remain the same.

So, Tuple is the correct choice.

---

# 📌 Key Points

- Tuples have only two built-in methods.
- `count()` counts how many times a value appears.
- `index()` returns the position of a value.
- Tuple Packing stores multiple values into one tuple.
- Tuple Unpacking stores tuple values into separate variables.
- Nested Tuples allow tuples inside tuples.
- Use Lists for changing data.
- Use Tuples for fixed data.
