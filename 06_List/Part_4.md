---

# 🧩 Beginner Practice Problems

These problems will help you understand lists better.

---

# Problem 1 – Find the Largest Number

## 📖 Problem Statement

You are given a list of marks.

Find the highest mark.

### 💻 Python Code

```python
marks = [75, 85, 92, 68, 88]

highest = max(marks)

print("Highest Mark:", highest)
```

### Output

```
Highest Mark: 92
```

---

# Problem 2 – Find the Smallest Number

## 📖 Problem Statement

Find the lowest mark in the class.

### 💻 Python Code

```python
marks = [75, 85, 92, 68, 88]

lowest = min(marks)

print("Lowest Mark:", lowest)
```

### Output

```
Lowest Mark: 68
```

---

# Problem 3 – Find Total Marks

## 📖 Problem Statement

Calculate the total marks scored by all students.

### 💻 Python Code

```python
marks = [75, 85, 92, 68, 88]

total = sum(marks)

print("Total Marks:", total)
```

### Output

```
Total Marks: 408
```

---

# Problem 4 – Count the Number of Students

## 📖 Problem Statement

Find how many students are present in the class.

### 💻 Python Code

```python
students = ["Gokul", "Rahul", "Priya", "Arun"]

print("Total Students:", len(students))
```

### Output

```
Total Students: 4
```

---

# Problem 5 – Search for a Student

## 📖 Problem Statement

Check whether a student is present in the class.

### 💻 Python Code

```python
students = ["Gokul", "Rahul", "Priya", "Arun"]

name = input("Enter Student Name: ")

if name in students:
    print("Student Found")
else:
    print("Student Not Found")
```

### Sample Input

```
Priya
```

### Output

```
Student Found
```

---

# 💻 LeetCode Problem – Contains Duplicate

## 📖 Problem Statement

Given a list of numbers, check whether any number appears more than once.

If any duplicate number exists, return **True**.

Otherwise, return **False**.

### Example

Input

```
[1, 2, 3, 1]
```

Output

```
True
```

Because **1** appears two times.

---

### 🌍 Real-World Example

Imagine a college.

Each student should have a unique Register Number.

If the same Register Number appears twice, there is a mistake in the database.

Similarly, we check whether the list contains duplicate values.

---

## 💻 Solution

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

## 📖 How Does This Work?

Original List

```
[1, 2, 3, 1]
```

Length of List

```
4
```

Convert List into Set

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

there are duplicate values.

So the answer is

```
True
```

---

# 💻 LeetCode Problem – Running Sum of 1D Array

## 📖 Problem Statement

Given a list of numbers, return the running sum.

Each element becomes the sum of itself and all previous elements.

### Example

Input

```
[1,2,3,4]
```

Output

```
[1,3,6,10]
```

---

### 💻 Solution

```python
numbers = [1, 2, 3, 4]

running_sum = []

total = 0

for number in numbers:
    total = total + number
    running_sum.append(total)

print(running_sum)
```

### Output

```
[1, 3, 6, 10]
```

---
