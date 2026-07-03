# 🐍 Sets in Python

## 📖 What is a Set?

A **Set** is a collection of **unique values** stored in a single variable.

Unlike a list, a set **does not allow duplicate values**.

A set is mainly used when we want to store unique data.

Sets are created using **curly braces `{}`**.

---

# 🌍 Real-World Example

Imagine a college is organizing a Python workshop.

Many students register for the workshop.

Some students accidentally register more than once.

Student List:

- Gokul
- Rahul
- Priya
- Gokul
- Arun
- Rahul

The college does not want duplicate registrations.

Using a **Set**, Python automatically removes duplicate names.

Result:

- Gokul
- Rahul
- Priya
- Arun

This is why Sets are useful.

---

# ❓ Why Do We Need Sets?

Sets help us to:

- Store only unique values.
- Remove duplicate data automatically.
- Perform mathematical operations like Union and Intersection.
- Search values quickly.
- Compare two collections of data.

---

# 📝 Syntax

```python
set_name = {value1, value2, value3}
```

---

# 💻 Example 1 – Student Names

```python
students = {"Gokul", "Rahul", "Priya"}

print(students)
```

### Output

```
{'Gokul', 'Rahul', 'Priya'}
```

---

# 💻 Example 2 – Duplicate Values

```python
students = {"Gokul", "Rahul", "Priya", "Gokul", "Rahul"}

print(students)
```

### Output

```
{'Gokul', 'Rahul', 'Priya'}
```

Notice that duplicate values are removed automatically.

---

# 💻 Example 3 – Different Data Types

A set can store different types of values.

```python
details = {"Gokul", 20, True, 8.65}

print(details)
```

### Output

```
{20, True, 8.65, 'Gokul'}
```

**Note:** The order may be different because sets do not maintain the order of elements.

---

# 📌 Important Properties of a Set

A Set:

- Stores only unique values.
- Does not allow duplicate values.
- Does not support indexing.
- Does not support slicing.
- Is mutable, so we can add or remove elements.
- Does not maintain insertion order.

---

# 💻 Accessing Elements

Unlike Lists and Tuples, Sets do not support indexing.

❌ Wrong

```python
students = {"Gokul", "Rahul", "Priya"}

print(students[0])
```

### Output

```
TypeError
```

Since Sets have no index, we cannot access elements using position.

---

# 🔁 Looping Through a Set

We can access all elements using a **for loop**.

### Example

```python
students = {"Gokul", "Rahul", "Priya"}

for student in students:
    print(student)
```

### Sample Output

```
Rahul
Priya
Gokul
```

The order may change every time the program runs.

---

# 📏 Length of a Set

The `len()` function returns the total number of elements.

### Example

```python
students = {"Gokul", "Rahul", "Priya"}

print(len(students))
```

### Output

```
3
```

---

# 🌍 Where Are Sets Used?

Sets are commonly used in:

- 🎓 Student Registration Systems
- 🏥 Hospital Patient Records
- 🛒 Online Shopping Websites
- 📧 Email Subscriber Lists
- 🌐 Website Visitor Tracking
- 🔐 Cybersecurity Blacklisted IP Addresses
- 📊 Data Analysis
- 🤖 Artificial Intelligence Projects

---

# 💡 When Should You Use a Set?

Use a Set when:

- Duplicate values should not be allowed.
- You need only unique data.
- You want to compare two collections.
- You want to remove duplicate values easily.

Example:

- Unique Student IDs
- Unique Email Addresses
- Unique Mobile Numbers
- Unique Product IDs

---

# 📌 Key Points

- A Set stores unique values.
- Duplicate values are removed automatically.
- Sets are created using curly braces `{}`.
- Sets do not support indexing.
- Sets do not support slicing.
- Sets are mutable, so elements can be added or removed.
- A `for` loop can be used to access all elements.
- `len()` returns the total number of elements.
