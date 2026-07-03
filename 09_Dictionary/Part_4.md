# 🧩 Beginner Practice Problems

Practice these problems to improve your understanding of dictionaries.

---

## Problem 1 – Store Student Details

### 📖 Problem Statement

Create a dictionary to store a student's:

- Name
- Age
- Department

Print all the details.

### 💻 Python Code

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

## Problem 2 – Add a New Key

### 📖 Problem Statement

Add the student's CGPA to the dictionary.

### 💻 Python Code

```python
student = {
    "Name": "Gokul",
    "Age": 20
}

student["CGPA"] = 8.65

print(student)
```

### Output

```
{'Name': 'Gokul', 'Age': 20, 'CGPA': 8.65}
```

---

## Problem 3 – Update Salary

### 📖 Problem Statement

Update the salary of an employee.

### 💻 Python Code

```python
employee = {
    "Name": "Rahul",
    "Salary": 40000
}

employee["Salary"] = 50000

print(employee)
```

### Output

```
{'Name': 'Rahul', 'Salary': 50000}
```

---

## Problem 4 – Remove a Key

### 📖 Problem Statement

Remove the "Age" key from the dictionary.

### 💻 Python Code

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

## Problem 5 – Search for a Student

### 📖 Problem Statement

Check whether a student's marks are available.

### 💻 Python Code

```python
marks = {
    "Gokul": 95,
    "Rahul": 88,
    "Priya": 91
}

student = input("Enter Student Name: ")

if student in marks:
    print("Marks:", marks[student])
else:
    print("Student Not Found")
```

### Sample Input

```
Priya
```

### Output

```
Marks: 91
```

---

# 💻 LeetCode Problem – Two Sum

## 📖 Problem Statement

You are given a list of numbers and a target value.

Find the positions of two numbers whose sum is equal to the target.

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

Imagine you are shopping.

You have different gift cards with different values.

You want to find two gift cards whose total value is exactly ₹500.

The same idea is used in this problem.

---

## 💻 Python Solution (Using Dictionary)

```python
numbers = [2, 7, 11, 15]
target = 9

seen = {}

for i in range(len(numbers)):
    difference = target - numbers[i]

    if difference in seen:
        print([seen[difference], i])
        break

    seen[numbers[i]] = i
```

### Output

```
[0, 1]
```

---

## 📖 How Does It Work?

Initially:

```
seen = {}
```

### Step 1

Current Number = 2

Difference = 9 - 2 = 7

7 is not found.

Store:

```
{
2:0
}
```

---

### Step 2

Current Number = 7

Difference = 9 - 7 = 2

2 is already present.

So the answer is:

```
[0,1]
```

---

# 💻 Interview Coding Problem – Word Counter

## 📖 Problem Statement

Count how many times each word appears in a sentence.

### 💻 Python Code

```python
sentence = "python java python ai java python"

words = sentence.split()

count = {}

for word in words:
    if word in count:
        count[word] += 1
    else:
        count[word] = 1

print(count)
```

### Output

```
{
'python': 3,
'java': 2,
'ai': 1
}
```

---

# 💻 Interview Coding Problem – Student Marks Lookup

## 📖 Problem Statement

Store marks for students and display the marks of a given student.

### 💻 Python Code

```python
marks = {
    "Gokul": 95,
    "Rahul": 88,
    "Priya": 91
}

student = "Rahul"

print(marks[student])
```

### Output

```
88
```

---

# 🌍 Real-Life Uses of Dictionaries

Dictionaries are one of the most widely used data types in Python.

They are used in:

- 🎓 Student Management Systems
- 👨‍💼 Employee Databases
- 🏦 Banking Applications
- 🏥 Hospital Management Systems
- 🛒 Online Shopping Websites
- 🔐 User Login Systems
- 📱 Mobile Applications
- 🌐 Websites
- 🤖 Artificial Intelligence
- 📊 Data Analysis
- 🛡️ Cybersecurity Tools
- 🎮 Game Development

---

# 📌 Key Points

- A dictionary stores data as key-value pairs.
- Keys must be unique.
- Values can be duplicated.
- Dictionaries are mutable.
- Access values using keys.
- Use `keys()` to get all keys.
- Use `values()` to get all values.
- Use `items()` to get both keys and values.
- Use `get()` to safely access a value.
- Use `update()` to add or modify data.
- Use `pop()` to remove a key.
- Use `clear()` to remove all data.
- Dictionaries are best for storing related information.
