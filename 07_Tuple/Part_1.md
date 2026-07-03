# 🐍 Tuples in Python

---

# 📖 What is a Tuple?

A **Tuple** is a collection of multiple values stored in a single variable.

A tuple can store:

- Numbers
- Strings
- Boolean values
- Different data types together

A tuple is similar to a list, but there is one important difference.

✅ **A Tuple cannot be changed after it is created.**

This means we **cannot add, remove, or update** elements in a tuple.

---

# 🌍 Real-World Example

Imagine your **Date of Birth**.

Example:

```
15 August 2005
```

Your Date of Birth never changes.

Similarly,

- Passport Number
- Aadhaar Number
- GPS Location
- Latitude and Longitude

These values usually remain the same.

So, instead of using a List, we use a **Tuple** because its values should not change.

---

# ❓ Why Do We Need Tuples?

Tuples are useful when the data should remain fixed.

They help us to:

- Store multiple values together.
- Protect data from accidental changes.
- Improve program reliability.
- Store fixed information.

---

# 📝 Syntax

```python
tuple_name = (value1, value2, value3)
```

---

# 💻 Example 1 – Student Details

```python
student = ("Gokul", 20, "AIML")

print(student)
```

### Output

```
('Gokul', 20, 'AIML')
```

---

# 💻 Example 2 – Months of the Year

The names of the months never change.

```python
months = (
    "January",
    "February",
    "March",
    "April"
)

print(months)
```

### Output

```
('January', 'February', 'March', 'April')
```

---

# 💻 Example 3 – GPS Location

A GPS location contains Latitude and Longitude.

```python
location = (11.0168, 76.9558)

print(location)
```

### Output

```
(11.0168, 76.9558)
```

---

# 📌 Tuple Indexing

Every element inside a tuple has an index.

Python starts indexing from **0**.

Example

```python
students = ("Gokul", "Rahul", "Priya", "Arun")
```

| Index | Value |
|------:|-------|
| 0 | Gokul |
| 1 | Rahul |
| 2 | Priya |
| 3 | Arun |

---

# 💻 Accessing Elements

```python
students = ("Gokul", "Rahul", "Priya", "Arun")

print(students[0])
```

### Output

```
Gokul
```

---

```python
print(students[2])
```

### Output

```
Priya
```

---

# 📌 Negative Indexing

Negative indexing starts from the last element.

| Index | Value |
|------:|-------|
| -4 | Gokul |
| -3 | Rahul |
| -2 | Priya |
| -1 | Arun |

---

### Example

```python
students = ("Gokul", "Rahul", "Priya", "Arun")

print(students[-1])
```

### Output

```
Arun
```

---

# ✂️ Tuple Slicing

Slicing is used to access multiple elements.

## Syntax

```python
tuple_name[start:end]
```

The start index is included.

The end index is not included.

---

### Example

```python
students = ("Gokul", "Rahul", "Priya", "Arun")

print(students[1:3])
```

### Output

```
('Rahul', 'Priya')
```

---

```python
print(students[:2])
```

### Output

```
('Gokul', 'Rahul')
```

---

```python
print(students[2:])
```

### Output

```
('Priya', 'Arun')
```

---

# 🔁 Looping Through a Tuple

A tuple can be accessed one element at a time using a **for loop**.

### Example

```python
students = ("Gokul", "Rahul", "Priya", "Arun")

for student in students:
    print(student)
```

### Output

```
Gokul
Rahul
Priya
Arun
```

---

# 📏 Length of a Tuple

The `len()` function returns the total number of elements.

### Example

```python
students = ("Gokul", "Rahul", "Priya", "Arun")

print(len(students))
```

### Output

```
4
```

---

# ⚠️ Can We Update a Tuple?

No.

Tuples are **immutable**.

This means their values cannot be changed after creation.

### Example

```python
students = ("Gokul", "Rahul", "Priya")

students[1] = "Arun"
```

### Output

```
TypeError: 'tuple' object does not support item assignment
```

---

# 🌍 Where Are Tuples Used?

Tuples are commonly used in:

- 📍 GPS Coordinates
- 🪪 Aadhaar Information
- 🛂 Passport Details
- 📅 Date of Birth
- 🌈 RGB Color Values
- 🛰️ Latitude and Longitude
- 🏥 Patient ID
- 🎓 Student Register Number

These values usually remain unchanged.

---

# 📌 Key Points

- A tuple stores multiple values in one variable.
- Tuples are created using **parentheses `()`**.
- Tuples can store different data types.
- Tuples are immutable.
- Indexing starts from **0**.
- Negative indexing starts from **-1**.
- Slicing works in tuples.
- A `for` loop can be used to access all elements.
- `len()` returns the number of elements.
