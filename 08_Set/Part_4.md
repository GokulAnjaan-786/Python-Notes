# 🧩 Beginner Practice Problems

Practice these problems to improve your understanding of Sets.

---

## Problem 1 – Remove Duplicate Student Names

### 📖 Problem Statement

A teacher has a list of student names.

Some names appear more than once.

Store them in a set and print the unique names.

### 💻 Python Code

```python
students = {
    "Gokul",
    "Rahul",
    "Priya",
    "Gokul",
    "Arun",
    "Rahul"
}

print(students)
```

### Sample Output

```
{'Gokul', 'Rahul', 'Priya', 'Arun'}
```

---

## Problem 2 – Add a New Student

### 📖 Problem Statement

A new student joins the workshop.

Add the student's name to the set.

### 💻 Python Code

```python
students = {
    "Gokul",
    "Rahul",
    "Priya"
}

students.add("Arun")

print(students)
```

### Sample Output

```
{'Gokul', 'Rahul', 'Priya', 'Arun'}
```

---

## Problem 3 – Find Common Students

### 📖 Problem Statement

Find the students who are members of both the Coding Club and the AI Club.

### 💻 Python Code

```python
coding_club = {
    "Gokul",
    "Rahul",
    "Priya"
}

ai_club = {
    "Rahul",
    "Priya",
    "Arun"
}

common_students = coding_club.intersection(ai_club)

print(common_students)
```

### Output

```
{'Rahul', 'Priya'}
```

---

## Problem 4 – Combine Two Sets

### 📖 Problem Statement

Two colleges are conducting a joint workshop.

Combine both student lists.

### 💻 Python Code

```python
college_a = {
    "Gokul",
    "Rahul"
}

college_b = {
    "Priya",
    "Arun"
}

all_students = college_a.union(college_b)

print(all_students)
```

### Sample Output

```
{'Gokul', 'Rahul', 'Priya', 'Arun'}
```

---

## Problem 5 – Remove a Student

### 📖 Problem Statement

A student cancels their workshop registration.

Remove the student's name from the set.

### 💻 Python Code

```python
students = {
    "Gokul",
    "Rahul",
    "Priya"
}

students.remove("Rahul")

print(students)
```

### Output

```
{'Gokul', 'Priya'}
```

---

# 💻 LeetCode Problem – Contains Duplicate

## 📖 Problem Statement

Given a list of numbers, check whether any number appears more than once.

Return **True** if there is at least one duplicate value.

Otherwise, return **False**.

### Example

**Input**

```
[1, 2, 3, 1]
```

**Output**

```
True
```

---

## 🌍 Real-World Example

Imagine a college.

Each student should have a unique Register Number.

If the same Register Number appears more than once, there is a mistake in the database.

A Set helps us quickly identify duplicate values.

---

## 💻 Python Solution

```python
numbers = [1, 2, 3, 1]

if len(numbers) != len(set(numbers)):
    print(True)
else:
    print(False)
```

### Output

```
True
```

---

## 📖 How Does It Work?

Original List

```
[1, 2, 3, 1]
```

Length of List

```
4
```

Convert the List into a Set

```
{1, 2, 3}
```

Length of Set

```
3
```

Since

```
4 != 3
```

duplicate values exist.

So the answer is

```
True
```

---

# 💻 Interview Coding Problem – Find Unique Numbers

## 📖 Problem Statement

Given a list of numbers, print only the unique values.

### 💻 Python Code

```python
numbers = [10, 20, 10, 30, 20, 40]

unique_numbers = set(numbers)

print(unique_numbers)
```

### Output

```
{40, 10, 20, 30}
```

---

# 💻 Interview Coding Problem – Find Different Subjects

## 📖 Problem Statement

Two students have chosen different subjects.

Find the subjects that are selected by only one student.

### 💻 Python Code

```python
student1 = {
    "Python",
    "Java",
    "SQL"
}

student2 = {
    "Python",
    "C++",
    "SQL"
}

print(student1.symmetric_difference(student2))
```

### Output

```
{'Java', 'C++'}
```

---

# 🌍 Real-Life Uses of Sets

Sets are widely used in real-world software.

Examples include:

- 🎓 Student Registration Systems
- 📧 Email Subscription Lists
- 🌐 Website Unique Visitors
- 🔐 Cybersecurity Blacklisted IP Addresses
- 🛒 Product Categories
- 🏥 Hospital Blood Group Records
- 📊 Data Analysis
- 🤖 Artificial Intelligence
- ☁️ Cloud Computing
- 📱 Mobile Applications

---

# 📌 Key Points

- A Set stores only unique values.
- Duplicate values are removed automatically.
- Sets are unordered.
- Sets do not support indexing.
- Sets do not support slicing.
- Sets are mutable.
- Use `add()` to add one value.
- Use `update()` to add multiple values.
- Use `remove()` or `discard()` to delete values.
- Use `union()` to combine sets.
- Use `intersection()` to find common values.
- Use `difference()` to find different values.
- Use `symmetric_difference()` to find values present in only one set.
