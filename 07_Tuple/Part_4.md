# 🧩 Beginner Practice Problems

Practice these problems to improve your understanding of tuples.

---

## Problem 1 – Display Student Details

### 📖 Problem Statement

Create a tuple to store a student's:

- Name
- Age
- Department

Print each value separately.

### 💻 Python Code

```python
student = ("Gokul", 20, "AIML")

print("Name:", student[0])
print("Age:", student[1])
print("Department:", student[2])
```

### Output

```
Name: Gokul
Age: 20
Department: AIML
```

---

## Problem 2 – Find the Length of a Tuple

### 📖 Problem Statement

Find the total number of subjects.

### 💻 Python Code

```python
subjects = ("Python", "Java", "C", "SQL")

print("Total Subjects:", len(subjects))
```

### Output

```
Total Subjects: 4
```

---

## Problem 3 – Count a Value

### 📖 Problem Statement

Find how many times "Python" appears in the tuple.

### 💻 Python Code

```python
languages = ("Python", "Java", "Python", "C++", "Python")

print(languages.count("Python"))
```

### Output

```
3
```

---

## Problem 4 – Find the Position of an Element

### 📖 Problem Statement

Find the position of "Priya" in the tuple.

### 💻 Python Code

```python
students = ("Gokul", "Rahul", "Priya", "Arun")

print(students.index("Priya"))
```

### Output

```
2
```

---

## Problem 5 – Tuple Unpacking

### 📖 Problem Statement

Store employee details in a tuple and print them using tuple unpacking.

### 💻 Python Code

```python
employee = ("Rahul", "Developer", 50000)

name, role, salary = employee

print("Name:", name)
print("Role:", role)
print("Salary:", salary)
```

### Output

```
Name: Rahul
Role: Developer
Salary: 50000
```

---

# 💻 LeetCode Problem – Two Sum

## 📖 Problem Statement

You are given a list of numbers and a target value.

Find the positions of the two numbers whose sum is equal to the target.

### Example

**Input**

```
numbers = [2, 7, 11, 15]
target = 9
```

**Output**

```
[0, 1]
```

Because:

```
2 + 7 = 9
```

---

## 🌍 Real-World Example

Imagine you have different currency notes in your wallet.

You want to find two notes that together make ₹500.

The same idea is used here.

---

## 💻 Python Code

```python
numbers = [2, 7, 11, 15]
target = 9

for i in range(len(numbers)):
    for j in range(i + 1, len(numbers)):
        if numbers[i] + numbers[j] == target:
            print([i, j])
```

### Output

```
[0, 1]
```

---

## 📖 How Does It Work?

The program checks every possible pair of numbers.

- First, it checks `2 + 7`.
- Since the sum is `9`, it prints their positions.
- Then the program stops because it found the required pair.

This solution is easy to understand and is suitable for beginners.

---

# 🌍 Where Are Tuples Used in Real Life?

Tuples are used in many real-world applications where data should remain unchanged.

Examples include:

- 📍 GPS Coordinates
- 🛰️ Latitude and Longitude
- 🌈 RGB Color Values
- 🎓 Student Register Numbers
- 🏥 Patient IDs
- 🛂 Passport Numbers
- 🪪 Aadhaar Numbers
- ✈️ Flight Numbers
- 🚆 Train Numbers
- 📦 Product IDs

---

# 📌 Key Points

- Tuples store multiple values in one variable.
- Tuples are created using parentheses `()`.
- Tuples are immutable, so their values cannot be changed.
- Tuples support indexing, slicing, and looping.
- `count()` counts how many times a value appears.
- `index()` returns the position of a value.
- Tuple packing stores multiple values into one tuple.
- Tuple unpacking stores tuple values into separate variables.
- Tuples are best for storing fixed data.
