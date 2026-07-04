# Classes and Objects in Python

## What is a Class?

A **class** is a **blueprint** or **template** used to create objects.

It tells Python:

> "Whenever someone creates an object, it should have these details and these actions."

A class itself is **not a real object**. It is only a design.

### Real-World Example

Imagine an engineer designing a house.

The blueprint contains:

- Number of rooms
- Number of windows
- Kitchen
- Bathroom

Can you live inside the blueprint?

**No.**

The blueprint is only a design.

Using that blueprint, many real houses can be built.

Here,

- **Blueprint = Class**
- **Actual House = Object**

---

## What is an Object?

An **object** is a real thing created using a class.

A single class can create many objects.

### Real-World Example

Suppose Samsung designs a mobile phone.

The design includes:

- Camera
- RAM
- Storage
- Battery
- Screen

This design is the **class**.

Now Samsung manufactures thousands of phones.

Every physical phone is an **object**.

Example:

- Phone 1
- Phone 2
- Phone 3

All of them are created from the same class.

---

## Visual Representation

```
               CLASS
        -----------------
             Student
        -----------------
        Name
        Age
        Department
        Roll Number
        -----------------

              │
              │
              ▼

        Student 1
        Student 2
        Student 3
        Student 4
```

One class can create many objects.

---

# Creating a Class

A class is created using the `class` keyword.

```python
class Student:
    pass
```

Here,

- `Student` is the class.
- `pass` means the class is currently empty.

---

# Creating an Object

```python
class Student:
    pass

student1 = Student()
student2 = Student()
```

Here,

- `student1` is an object.
- `student2` is another object.

Both are created from the same class.

---

# What is `__init__()`?

`__init__()` is a special method in Python.

It runs **automatically** whenever a new object is created.

Its purpose is to give initial values to the object.

### Real-World Example

Suppose you buy a new mobile phone.

When you open the box, the phone already has:

- Brand
- Model
- Storage
- Battery

Nobody adds these details after opening the box.

They are already there.

Similarly, when Python creates an object, `__init__()` gives that object its initial data.

---

# Understanding `__init__()`

```python
class Student:

    def __init__(self, name, age, department):
        self.name = name
        self.age = age
        self.department = department
```

Let's understand each line.

---

### Line 1

```python
def __init__(self, name, age, department):
```

This means:

Whenever a new student object is created, it should receive:

- Name
- Age
- Department

For example,

```python
student1 = Student("Gokul", 20, "AI & ML")
```

Python automatically matches the values.

| Parameter | Value |
|-----------|-------|
| self | student1 |
| name | Gokul |
| age | 20 |
| department | AI & ML |

Notice that **Python automatically passes `self`**.

You only provide the remaining values.

---

### Line 2

```python
self.name = name
```

Suppose,

```python
student1 = Student("Gokul", 20, "AI & ML")
```

Then,

```python
self.name = "Gokul"
```

This stores the name inside the object.

---

### Line 3

```python
self.age = age
```

Stores the age inside the object.

---

### Line 4

```python
self.department = department
```

Stores the department inside the object.

Now the object contains

```
student1

Name = Gokul
Age = 20
Department = AI & ML
```

---

# What is `self`?

This is the most confusing topic for beginners.

Actually, it is very simple.

`self` refers to **the current object**.

Suppose we create two objects.

```python
student1 = Student("Gokul", 20, "AI & ML")
student2 = Student("Alice", 21, "Computer Science")
```

When Python works with

```python
student1
```

then

```
self
│
▼
student1
```

When Python works with

```python
student2
```

then

```
self
│
▼
student2
```

So,

`self` simply means

> "This current object."

---

# Beginner Python Example

```python
class Student:

    def __init__(self, name):
        self.name = name

    def introduce(self):
        print("Hello, my name is", self.name)


student1 = Student("Gokul")
student2 = Student("Alice")

student1.introduce()
student2.introduce()
```

### Output

```
Hello, my name is Gokul
Hello, my name is Alice
```

---

# Intermediate Python Example

```python
class Student:

    def __init__(self, name, age, department):
        self.name = name
        self.age = age
        self.department = department

    def introduce(self):
        print(f"Hello, my name is {self.name}.")
        print(f"I am {self.age} years old.")
        print(f"I study {self.department}.")

    def study(self):
        print(f"{self.name} is studying Python.")


student1 = Student("Gokul", 20, "AI & ML")
student2 = Student("Alice", 22, "Computer Science")

student1.introduce()
student1.study()

print()

student2.introduce()
student2.study()
```

### Output

```
Hello, my name is Gokul.
I am 20 years old.
I study AI & ML.
Gokul is studying Python.

Hello, my name is Alice.
I am 22 years old.
I study Computer Science.
Alice is studying Python.
```

---

# Real-World Python Example

Suppose we want to represent cars.

Every car has

- Brand
- Color

Every car can

- Start
- Stop

```python
class Car:

    def __init__(self, brand, color):
        self.brand = brand
        self.color = color

    def start(self):
        print(f"{self.brand} is starting.")

    def stop(self):
        print(f"{self.brand} is stopping.")


car1 = Car("Audi", "Red")
car2 = Car("BMW", "Blue")

car1.start()
car2.stop()

print(car1.color)
print(car2.color)
```

### Output

```
Audi is starting.
BMW is stopping.
Red
Blue
```

---

# How Python Executes This Code

Suppose we write

```python
car1 = Car("Audi", "Red")
```

Python performs these steps automatically.

### Step 1

Creates an empty object.

```
car1

Empty Object
```

---

### Step 2

Automatically calls

```python
__init__(car1, "Audi", "Red")
```

---

### Step 3

Executes

```python
self.brand = brand
```

which becomes

```python
car1.brand = "Audi"
```

---

### Step 4

Executes

```python
self.color = color
```

which becomes

```python
car1.color = "Red"
```

Now the object looks like

```
car1

Brand = Audi
Color = Red
```

The object is now completely ready to use.

---

# Final Summary

- A **Class** is a blueprint or template.
- An **Object** is a real instance created from a class.
- `__init__()` automatically runs whenever an object is created.
- `self` refers to the current object.
- `self.variable = value` stores data inside the object.
- One class can create multiple objects, and each object stores its own data independently.
