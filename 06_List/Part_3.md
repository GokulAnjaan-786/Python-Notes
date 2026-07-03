---

# 🌍 Real-World Project 1 – Student Management System

## 📖 Problem Statement

Suppose you are developing a simple application for a school.

The school wants to:

- Add a new student
- Remove a student
- Display all students

A Python list is perfect for storing the student names.

---

## 💻 Python Program

```python
students = ["Gokul", "Rahul", "Priya"]

print("Current Students:")
print(students)

students.append("Arun")

print("\nAfter Adding Arun:")
print(students)

students.remove("Rahul")

print("\nAfter Removing Rahul:")
print(students)
```

### Output

```
Current Students:
['Gokul', 'Rahul', 'Priya']

After Adding Arun:
['Gokul', 'Rahul', 'Priya', 'Arun']

After Removing Rahul:
['Gokul', 'Priya', 'Arun']
```

---

# 🌍 Real-World Project 2 – Shopping Cart System

## 📖 Problem Statement

Suppose you are creating an online shopping application.

A customer can:

- Add products
- Remove products
- View all products

---

## 💻 Python Program

```python
cart = []

cart.append("Laptop")
cart.append("Mouse")
cart.append("Keyboard")

print("Shopping Cart:")
print(cart)

cart.remove("Mouse")

print("\nAfter Removing Mouse:")
print(cart)
```

### Output

```
Shopping Cart:
['Laptop', 'Mouse', 'Keyboard']

After Removing Mouse:
['Laptop', 'Keyboard']
```

---

# 🌍 Real-World Project 3 – Student Marks System

## 📖 Problem Statement

A teacher wants to calculate the total marks of students.

---

## 💻 Python Program

```python
marks = [85, 90, 78, 95, 88]

total = sum(marks)

average = total / len(marks)

print("Total Marks:", total)

print("Average Marks:", average)
```

### Output

```
Total Marks: 436

Average Marks: 87.2
```

---

# 🌍 Real-World Project 4 – Attendance System

## 📖 Problem Statement

A teacher wants to check whether a student is present in today's attendance list.

---

## 💻 Python Program

```python
attendance = ["Gokul", "Rahul", "Priya", "Arun"]

student = input("Enter Student Name: ")

if student in attendance:
    print("Student is Present")
else:
    print("Student is Absent")
```

### Sample Input

```
Priya
```

### Output

```
Student is Present
```

---

# 🌍 Real-World Project 5 – Highest Marks Finder

## 📖 Problem Statement

A teacher wants to find the highest mark scored in the class.

---

## 💻 Python Program

```python
marks = [75, 80, 98, 65, 91]

highest = max(marks)

print("Highest Marks:", highest)
```

### Output

```
Highest Marks: 98
```

---

# 🌍 Real-World Applications of Lists

Lists are one of the most commonly used data structures in Python.

They are used in:

- 🎓 Student Management Systems
- 🏥 Hospital Management Systems
- 🛒 Shopping Cart Applications
- 🏦 Banking Applications
- 📚 Library Management Systems
- 🎬 Movie Recommendation Systems
- 📱 Mobile Applications
- 🌐 Websites
- 🤖 Artificial Intelligence Projects
- 📊 Data Analysis
- 🔐 Cybersecurity Tools
- 🎮 Games

---

# 💡 When Should You Use a List?

Use a list when:

- You want to store multiple values.
- The values may change later.
- You need to add or remove elements.
- You want to loop through all values.
- You need to sort or search data.

Lists are one of the most useful data types in Python and are used in almost every real-world Python project.
