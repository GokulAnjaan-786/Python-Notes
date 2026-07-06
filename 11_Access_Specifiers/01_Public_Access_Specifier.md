# Public Access Specifier in Python

## What is a Public Access Specifier?

A **Public Access Specifier** means that a variable or method can be accessed from **anywhere** in the program.

This is the **default access level** in Python.

If you create a variable without using `_` or `__`, Python treats it as **Public**.

In simple words,

> **A Public variable or method can be used both inside and outside the class.**

---

# Real-World Example

Imagine a college.

Every student has

- Name
- Department

These details are not secret.

Teachers, students, and the college office can see them.

So these details can be **Public**.

---

# Syntax

```python
class Student:

    def __init__(self):
        self.name = "Gokul"
```

Notice

```python
self.name
```

There is **no underscore** before `name`.

This means it is a **Public Variable**.

---

# Intermediate Python Example

```python
class Student:

    def __init__(self, name, department, cgpa):
        self.name = name
        self.department = department
        self.cgpa = cgpa

    def show_details(self):
        print(f"Name       : {self.name}")
        print(f"Department : {self.department}")
        print(f"CGPA       : {self.cgpa}")


student1 = Student("Gokul", "AIML", 8.65)
student2 = Student("Alice", "CSE", 9.10)

students = [
    student1,
    student2
]

for student in students:

    student.show_details()

    if student.cgpa >= 9:
        print("Excellent Performance")

    elif student.cgpa >= 8:
        print("Very Good Performance")

    else:
        print("Good Performance")

    print("-" * 30)
```

---

# Output

```
Name       : Gokul
Department : AIML
CGPA       : 8.65
Very Good Performance
------------------------------

Name       : Alice
Department : CSE
CGPA       : 9.1
Excellent Performance
------------------------------
```

---

# Step-by-Step Explanation

## Step 1

A class named `Student` is created.

```python
class Student:
```

This class represents every student.

---

## Step 2

The constructor stores three public variables.

```python
self.name
self.department
self.cgpa
```

Since there is **no underscore**, all three are **Public Variables**.

---

## Step 3

Two student objects are created.

```python
student1 = Student("Gokul", "AIML", 8.65)

student2 = Student("Alice", "CSE", 9.10)
```

Now Python stores

### student1

```
Name       = Gokul
Department = AIML
CGPA       = 8.65
```

### student2

```
Name       = Alice
Department = CSE
CGPA       = 9.10
```

---

## Step 4

Both objects are stored inside a list.

```python
students = [
    student1,
    student2
]
```

Python allows us to store objects inside a list.

---

## Step 5

The loop starts.

```python
for student in students:
```

During every iteration,

the variable `student` points to one object.

First iteration

```
student

↓

student1
```

Second iteration

```
student

↓

student2
```

---

## Step 6

Python executes

```python
student.show_details()
```

For the first iteration,

Python executes

```python
student1.show_details()
```

For the second iteration,

Python executes

```python
student2.show_details()
```

---

## Step 7

Python checks

```python
if student.cgpa >= 9
```

For student1

```
8.65 >= 9

False
```

Next condition

```
8.65 >= 8

True
```

Output

```
Very Good Performance
```

---

For student2

```
9.10 >= 9

True
```

Output

```
Excellent Performance
```

---

# How Python Executes the Program

When we create

```python
student1 = Student("Gokul", "AIML", 8.65)
```

Python performs the following steps.

### Step 1

Creates an empty object.

```
student1

Empty Object
```

---

### Step 2

Calls the constructor.

```python
__init__()
```

---

### Step 3

Stores

```python
self.name = name
self.department = department
self.cgpa = cgpa
```

Now the object becomes

```
student1

Name = Gokul

Department = AIML

CGPA = 8.65
```

---

### Step 4

The loop starts.

Python takes one object from the list.

Calls

```python
student.show_details()
```

Prints the details.

---

### Step 5

Python checks the CGPA.

Depending on the condition,

it prints the correct performance message.

---

# Why Are These Variables Public?

Because

```python
name
department
cgpa
```

are not secret information.

Other parts of the program can safely use them.

For example,

outside the class,

we can write

```python
print(student1.name)

print(student1.department)

print(student1.cgpa)
```

This works because they are **Public Variables**.

---

# Summary

- Public is the default access specifier in Python.
- A public variable does not use `_` or `__`.
- Public variables can be accessed both inside and outside the class.
- Public variables are generally used for information that is safe to share.
- Examples include a student's name, department, or CGPA.
