# 🐍 Lists in Python

---

# 📖 What is a List?

A **List** is a collection of multiple values stored in a single variable.

A list can store:

- Numbers
- Strings
- Boolean values
- Other lists
- Different data types together

Lists are one of the most commonly used data types in Python because they allow us to store many values in one place.

---

# 🌍 Real-World Example

Imagine you are a teacher.

Instead of creating a separate variable for every student's name,

```python
student1 = "Gokul"
student2 = "Rahul"
student3 = "Priya"
student4 = "Arun"
```

you can store all student names in one list.

```python
students = ["Gokul", "Rahul", "Priya", "Arun"]
```

Now, all the student names are stored in one variable.

This makes the program simple and easy to manage.

---

# ❓ Why Do We Need Lists?

Lists help us to:

- Store multiple values in one variable.
- Easily add new values.
- Remove unwanted values.
- Update existing values.
- Access any value whenever needed.
- Loop through all values easily.

Without lists, we would have to create many variables, making programs difficult to manage.

---

# 📝 Syntax

```python
list_name = [value1, value2, value3]
```

---

# 💻 Example 1 – Student Names

```python
students = ["Gokul", "Rahul", "Priya", "Arun"]

print(students)
```

### Output

```
['Gokul', 'Rahul', 'Priya', 'Arun']
```

---

# 💻 Example 2 – Product Prices

```python
prices = [250, 500, 150, 1000]

print(prices)
```

### Output

```
[250, 500, 150, 1000]
```

---

# 💻 Example 3 – Different Data Types

A list can store different types of values together.

```python
details = ["Gokul", 20, 8.65, True]

print(details)
```

### Output

```
['Gokul', 20, 8.65, True]
```

---

# 📌 List Indexing

Every element in a list has a position called an **index**.

Python starts counting from **0**.

Example

```python
students = ["Gokul", "Rahul", "Priya", "Arun"]
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
students = ["Gokul", "Rahul", "Priya", "Arun"]

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

Python also allows negative indexing.

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
students = ["Gokul", "Rahul", "Priya", "Arun"]

print(students[-1])
```

### Output

```
Arun
```

---

# ✂️ List Slicing

Slicing is used to access multiple elements from a list.

## Syntax

```python
list_name[start:end]
```

The **start index is included**.

The **end index is not included**.

---

### Example

```python
students = ["Gokul", "Rahul", "Priya", "Arun"]

print(students[0:2])
```

### Output

```
['Gokul', 'Rahul']
```

---

```python
print(students[1:4])
```

### Output

```
['Rahul', 'Priya', 'Arun']
```

---

```python
print(students[:3])
```

### Output

```
['Gokul', 'Rahul', 'Priya']
```

---

```python
print(students[2:])
```

### Output

```
['Priya', 'Arun']
```

---

# 🔁 Looping Through a List

A list can be accessed one element at a time using a **for loop**.

### Example

```python
students = ["Gokul", "Rahul", "Priya", "Arun"]

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

# 📏 Length of a List

The `len()` function returns the total number of elements in a list.

### Example

```python
students = ["Gokul", "Rahul", "Priya", "Arun"]

print(len(students))
```

### Output

```
4
```

---

# ✏️ Updating an Element

Lists are **mutable**, which means we can change their values.

### Example

```python
students = ["Gokul", "Rahul", "Priya"]

students[1] = "Arun"

print(students)
```

### Output

```
['Gokul', 'Arun', 'Priya']
```

---

# 🌍 Where Are Lists Used?

Lists are used in almost every software application.

Examples include:

- 🎓 Student Management System
- 🛒 Shopping Cart
- 🏦 Banking Application
- 🏥 Hospital Management System
- 📚 Library Management System
- 📱 Mobile Applications
- 🌐 Websites
- 🤖 Artificial Intelligence Projects
- 🔐 Cybersecurity Tools
- 📊 Data Analysis Projects

---

# 📌 Key Points

- A list stores multiple values in one variable.
- Lists are created using square brackets `[]`.
- Lists can store different data types.
- Indexing starts from **0**.
- Negative indexing starts from **-1**.
- Lists are mutable, so elements can be updated.
- Slicing helps us access multiple elements.
- A `for` loop can be used to read all elements.
- `len()` returns the number of elements in a list.
