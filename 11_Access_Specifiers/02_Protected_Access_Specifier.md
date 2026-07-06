# Protected Access Specifier in Python

## What is a Protected Access Specifier?

A **Protected Access Specifier** means that a variable or method is **mainly meant to be used inside the class and by its child classes**.

In Python, a protected variable is created by adding **one underscore (`_`)** before the variable name.

In simple words,

> **A protected variable should be used inside the class and by child classes. Although Python allows you to access it from outside the class, it is not recommended.**

Unlike some programming languages, Python does not completely block access to protected variables. The underscore is a convention that tells programmers:

> **"This variable is for internal use. Avoid using it directly from outside the class."**

---

# Real-World Example

Imagine a company.

Every employee has

- Name
- Employee ID
- Salary

The employee's **salary** should normally be used only by

- HR
- Payroll Department
- Manager

Other employees should not access it directly.

So, salary is a good example of a **Protected Variable**.

---

# Syntax

```python
class Employee:

    def __init__(self):
        self._salary = 50000
```

Notice

```python
self._salary
```

There is **one underscore (`_`)** before the variable name.

This makes it a **Protected Variable**.

---

# Intermediate Python Example

```python
class Employee:

    def __init__(self, name, salary):
        self.name = name
        self._salary = salary


class Manager(Employee):

    def show_salary(self):

        print(f"Employee Name : {self.name}")
        print(f"Salary        : ₹{self._salary}")

        if self._salary >= 70000:
            print("Senior Employee")
        else:
            print("Junior Employee")


employee1 = Manager("Gokul", 85000)
employee2 = Manager("Alice", 55000)

employees = [
    employee1,
    employee2
]

for employee in employees:

    employee.show_salary()

    print("-" * 35)
```

---

# Output

```
Employee Name : Gokul
Salary        : ₹85000
Senior Employee
-----------------------------------

Employee Name : Alice
Salary        : ₹55000
Junior Employee
-----------------------------------
```

---

# Step-by-Step Explanation

## Step 1

The parent class `Employee` is created.

```python
class Employee:
```

It stores

- Name
- Salary

The salary is stored as

```python
self._salary
```

Because salary should mainly be used inside the class and by child classes.

---

## Step 2

A child class named `Manager` is created.

```python
class Manager(Employee):
```

This class inherits everything from `Employee`.

So it automatically gets

- `name`
- `_salary`

---

## Step 3

The child class creates a new method.

```python
show_salary()
```

Inside this method,

the child class directly accesses

```python
self._salary
```

This is allowed because protected variables are intended to be used inside child classes.

---

## Step 4

Two objects are created.

```python
employee1 = Manager("Gokul", 85000)

employee2 = Manager("Alice", 55000)
```

Python stores

### employee1

```
Name = Gokul

Salary = 85000
```

### employee2

```
Name = Alice

Salary = 55000
```

---

## Step 5

Both objects are stored inside a list.

```python
employees = [
    employee1,
    employee2
]
```

---

## Step 6

The loop starts.

```python
for employee in employees:
```

First iteration

```
employee

↓

employee1
```

Second iteration

```
employee

↓

employee2
```

---

## Step 7

Python executes

```python
employee.show_salary()
```

During the first iteration,

Python executes

```python
employee1.show_salary()
```

Inside that method,

Python accesses

```python
self._salary
```

and checks

```python
if self._salary >= 70000
```

85000 is greater than 70000.

So the output is

```
Senior Employee
```

---

For the second object,

Python checks

```
55000 >= 70000
```

This is False.

So Python prints

```
Junior Employee
```

---

# Can We Access a Protected Variable Outside the Class?

Yes.

Python allows this.

Example

```python
print(employee1._salary)
```

Output

```
85000
```

Although this works,

it is **not recommended**.

The underscore (`_`) tells programmers

> "This variable is intended for internal use."

---

# How Python Executes the Program

When Python executes

```python
employee1 = Manager("Gokul", 85000)
```

It performs these steps.

### Step 1

Creates an empty object.

```
employee1

Empty Object
```

---

### Step 2

Calls the parent constructor.

```python
__init__()
```

---

### Step 3

Stores

```python
self.name = name

self._salary = salary
```

Now the object becomes

```
employee1

Name = Gokul

Salary = 85000
```

---

### Step 4

The loop starts.

Python takes one object from the list.

Calls

```python
employee.show_salary()
```

Inside this method,

the child class accesses

```python
self._salary
```

without any problem.

---

# Why Is Salary Protected?

Salary is not secret like a password,

but it should not be freely modified by every part of the program.

Only classes that work with employee information should use it.

That is why it is marked as **Protected**.

---

# Difference Between Public and Protected

| Public | Protected |
|---------|-----------|
| No underscore | One underscore (`_`) |
| Can be accessed anywhere | Intended for the class and child classes |
| Safe to use from outside | Python allows access, but it is not recommended |
| Example: Name | Example: Salary |

---

# Summary

- A Protected Variable uses one underscore (`_`).
- Protected variables are mainly intended for the class itself and its child classes.
- Python does not completely prevent outside access.
- The underscore is a convention that tells programmers not to access the variable directly.
- Protected variables are commonly used with inheritance because child classes can access them easily.
