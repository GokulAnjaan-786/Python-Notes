# 🔧 Common Dictionary Methods in Python

Python provides many built-in methods to work with dictionaries. These methods help us access, update, remove, and manage data easily.

---

# 1️⃣ keys()

## 📖 What is keys()?

The `keys()` method returns all the keys present in a dictionary.

---

## 🌍 Real-World Example

Imagine a student database.

If you want to know what information is stored about a student, such as Name, Age, and Department, you can use the `keys()` method.

---

## 📝 Syntax

```python
dictionary_name.keys()
```

---

## 💻 Example

```python
student = {
    "Name": "Gokul",
    "Age": 20,
    "Department": "AIML"
}

print(student.keys())
```

### Output

```
dict_keys(['Name', 'Age', 'Department'])
```

---

# 2️⃣ values()

## 📖 What is values()?

The `values()` method returns all the values stored in a dictionary.

---

## 🌍 Real-World Example

A teacher wants to view only the student details without seeing the field names.

---

## 📝 Syntax

```python
dictionary_name.values()
```

---

## 💻 Example

```python
student = {
    "Name": "Gokul",
    "Age": 20,
    "Department": "AIML"
}

print(student.values())
```

### Output

```
dict_values(['Gokul', 20, 'AIML'])
```

---

# 3️⃣ items()

## 📖 What is items()?

The `items()` method returns both keys and values together.

---

## 🌍 Real-World Example

A school wants to print complete student information.

---

## 📝 Syntax

```python
dictionary_name.items()
```

---

## 💻 Example

```python
student = {
    "Name": "Gokul",
    "Age": 20,
    "Department": "AIML"
}

print(student.items())
```

### Output

```
dict_items([('Name', 'Gokul'), ('Age', 20), ('Department', 'AIML')])
```

---

# 4️⃣ get()

## 📖 What is get()?

The `get()` method returns the value of a given key.

If the key is not present, it returns `None` instead of giving an error.

---

## 🌍 Real-World Example

Suppose a company wants to check whether an employee's phone number is stored.

If it is not available, the program should continue without crashing.

---

## 📝 Syntax

```python
dictionary_name.get(key)
```

---

## 💻 Example

```python
student = {
    "Name": "Gokul",
    "Age": 20
}

print(student.get("Name"))
print(student.get("Department"))
```

### Output

```
Gokul
None
```

---

# 5️⃣ update()

## 📖 What is update()?

The `update()` method adds new key-value pairs or updates existing values.

---

## 🌍 Real-World Example

A student changes their phone number.

The school updates the record.

---

## 📝 Syntax

```python
dictionary_name.update({"key": value})
```

---

## 💻 Example

```python
student = {
    "Name": "Gokul",
    "Age": 20
}

student.update({"Age": 21})

print(student)
```

### Output

```
{'Name': 'Gokul', 'Age': 21}
```

---

# 6️⃣ pop()

## 📖 What is pop()?

The `pop()` method removes a key and returns its value.

---

## 🌍 Real-World Example

A company removes an employee's old phone number from the database.

---

## 📝 Syntax

```python
dictionary_name.pop(key)
```

---

## 💻 Example

```python
student = {
    "Name": "Gokul",
    "Age": 20,
    "Department": "AIML"
}

student.pop("Age")

print(student)
```

### Output

```
{'Name': 'Gokul', 'Department': 'AIML'}
```

---

# 7️⃣ popitem()

## 📖 What is popitem()?

The `popitem()` method removes the last inserted key-value pair.

---

## 🌍 Real-World Example

Suppose the last record entered into a system was added by mistake.

It can be removed using `popitem()`.

---

## 📝 Syntax

```python
dictionary_name.popitem()
```

---

## 💻 Example

```python
student = {
    "Name": "Gokul",
    "Age": 20,
    "Department": "AIML"
}

student.popitem()

print(student)
```

### Output

```
{'Name': 'Gokul', 'Age': 20}
```

---

# 8️⃣ clear()

## 📖 What is clear()?

The `clear()` method removes all key-value pairs from a dictionary.

---

## 🌍 Real-World Example

At the end of an academic year, the student records are cleared before creating records for the next batch.

---

## 📝 Syntax

```python
dictionary_name.clear()
```

---

## 💻 Example

```python
student = {
    "Name": "Gokul",
    "Age": 20
}

student.clear()

print(student)
```

### Output

```
{}
```

---

# 9️⃣ copy()

## 📖 What is copy()?

The `copy()` method creates a duplicate copy of a dictionary.

---

## 🌍 Real-World Example

Before updating important records, a company creates a backup.

---

## 📝 Syntax

```python
new_dictionary = old_dictionary.copy()
```

---

## 💻 Example

```python
student = {
    "Name": "Gokul",
    "Age": 20
}

backup = student.copy()

print(backup)
```

### Output

```
{'Name': 'Gokul', 'Age': 20}
```

---

# 🔟 fromkeys()

## 📖 What is fromkeys()?

The `fromkeys()` method creates a new dictionary using a list of keys and assigns the same value to all of them.

---

## 🌍 Real-World Example

Suppose a teacher creates attendance for three students.

Initially, everyone is marked as "Absent".

---

## 📝 Syntax

```python
dict.fromkeys(keys, value)
```

---

## 💻 Example

```python
students = ["Gokul", "Rahul", "Priya"]

attendance = dict.fromkeys(students, "Absent")

print(attendance)
```

### Output

```
{
    'Gokul': 'Absent',
    'Rahul': 'Absent',
    'Priya': 'Absent'
}
```

---

# 📊 Quick Reference Table

| Method | Purpose |
|---------|---------|
| `keys()` | Returns all keys |
| `values()` | Returns all values |
| `items()` | Returns keys and values |
| `get()` | Returns the value of a key |
| `update()` | Adds or updates values |
| `pop()` | Removes a key |
| `popitem()` | Removes the last inserted key-value pair |
| `clear()` | Removes all data |
| `copy()` | Creates a duplicate dictionary |
| `fromkeys()` | Creates a new dictionary with default values |

---

# 📌 Key Points

- `keys()` returns all keys.
- `values()` returns all values.
- `items()` returns both keys and values.
- `get()` safely accesses a value without giving an error if the key is missing.
- `update()` adds or updates key-value pairs.
- `pop()` removes a specific key.
- `popitem()` removes the last inserted key-value pair.
- `clear()` removes everything from the dictionary.
- `copy()` creates a duplicate dictionary.
- `fromkeys()` creates a new dictionary with the same default value for all keys.
