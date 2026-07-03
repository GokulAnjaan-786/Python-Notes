# 🐍 Dictionaries in Python

## 📖 What is a Dictionary?

A **Dictionary** is a collection of data stored as **key-value pairs**.

Each value is connected to a unique key.

Instead of accessing data using an index like a List or Tuple, we access data using its **key**.

Dictionaries are created using **curly braces `{}`**.

---

# 🌍 Real-World Example

Imagine a student ID card.

It contains information like:

- Name → Gokul
- Age → 20
- Department → AIML
- CGPA → 8.65

Each piece of information has a name.

Here,

- **Name**, **Age**, **Department**, and **CGPA** are **Keys**.
- **Gokul**, **20**, **AIML**, and **8.65** are **Values**.

This is exactly how a dictionary works.

---

# ❓ Why Do We Need Dictionaries?

We use dictionaries when we want to store related information together.

Dictionaries help us to:

- Store data as key-value pairs.
- Access data quickly using keys.
- Update information easily.
- Add new information whenever needed.
- Store real-world records like employee details, student details, bank accounts, etc.

---

# 📝 Syntax

```python
dictionary_name = {
    "key1": value1,
    "key2": value2,
    "key3": value3
}
```

---

# 💻 Example 1 – Student Details

```python
student = {
    "Name": "Gokul",
    "Age": 20,
    "Department": "AIML"
}

print(student)
```

### Output

```
{'Name': 'Gokul', 'Age': 20, 'Department': 'AIML'}
```

---

# 💻 Example 2 – Employee Details

```python
employee = {
    "ID": 101,
    "Name": "Rahul",
    "Salary": 45000
}

print(employee)
```

### Output

```
{'ID': 101, 'Name': 'Rahul', 'Salary': 45000}
```

---

# 💻 Example 3 – Product Details

```python
product = {
    "Product Name": "Laptop",
    "Brand": "Dell",
    "Price": 65000
}

print(product)
```

### Output

```
{'Product Name': 'Laptop', 'Brand': 'Dell', 'Price': 65000}
```

---

# 📌 Accessing Values

Dictionary values are accessed using their **keys**.

## Syntax

```python
dictionary_name["key"]
```

---

## 💻 Example

```python
student = {
    "Name": "Gokul",
    "Age": 20,
    "Department": "AIML"
}

print(student["Name"])
print(student["Department"])
```

### Output

```
Gokul
AIML
```

---

# ➕ Adding a New Key-Value Pair

We can add a new key and value to a dictionary.

## 💻 Example

```python
student = {
    "Name": "Gokul",
    "Age": 20
}

student["Department"] = "AIML"

print(student)
```

### Output

```
{'Name': 'Gokul', 'Age': 20, 'Department': 'AIML'}
```

---

# ✏️ Updating a Value

We can update the value of an existing key.

## 💻 Example

```python
student = {
    "Name": "Gokul",
    "Age": 20
}

student["Age"] = 21

print(student)
```

### Output

```
{'Name': 'Gokul', 'Age': 21}
```

---

# 🔁 Looping Through a Dictionary

We can use a **for loop** to access all the keys.

## 💻 Example

```python
student = {
    "Name": "Gokul",
    "Age": 20,
    "Department": "AIML"
}

for key in student:
    print(key)
```

### Output

```
Name
Age
Department
```

---

# 🔁 Looping Through Keys and Values

We can print both keys and values together.

## 💻 Example

```python
student = {
    "Name": "Gokul",
    "Age": 20,
    "Department": "AIML"
}

for key, value in student.items():
    print(key, ":", value)
```

### Output

```
Name : Gokul
Age : 20
Department : AIML
```

---

# 📏 Length of a Dictionary

The `len()` function returns the total number of key-value pairs.

## 💻 Example

```python
student = {
    "Name": "Gokul",
    "Age": 20,
    "Department": "AIML"
}

print(len(student))
```

### Output

```
3
```

---

# 🌍 Where Are Dictionaries Used?

Dictionaries are widely used in:

- 🎓 Student Management Systems
- 👨‍💼 Employee Databases
- 🏦 Banking Applications
- 🏥 Hospital Management Systems
- 🛒 Online Shopping Websites
- 📱 Mobile Applications
- 🌐 Websites
- 🤖 Artificial Intelligence Projects
- 🔐 Cybersecurity Tools
- 📊 Data Analysis

---

# 💡 When Should You Use a Dictionary?

Use a Dictionary when:

- Every value has a name.
- You need to access data using keys.
- You want to store related information together.
- You need to update values easily.

### Examples

- Student Details
- Employee Details
- Product Information
- Bank Account Details
- Hospital Patient Records
- User Login Information

---

# 📊 Dictionary vs List

| List | Dictionary |
|------|------------|
| Stores only values | Stores key-value pairs |
| Access using index | Access using key |
| Uses `[]` | Uses `{}` |
| Good for ordered data | Good for related information |

---

# 📌 Key Points

- A Dictionary stores data as key-value pairs.
- Dictionaries are created using curly braces `{}`.
- Keys must be unique.
- Values can be duplicated.
- Dictionary values are accessed using keys.
- Dictionaries are mutable, so values can be added, updated, or removed.
- `len()` returns the number of key-value pairs.
- Dictionaries are one of the most commonly used data types in Python.
