# Constructors in Python

## What is a Constructor?

A **constructor** is a special method in Python that is **automatically called whenever an object is created**.

Its main purpose is to **initialize the object** by giving it initial values.

In Python, the constructor is written using the special method:

```python
__init__()
```

You do **not** call the constructor yourself.

Python automatically calls it whenever a new object is created.

---

# Real-World Example

Imagine you buy a new laptop.

When you open the box, it already has:

- Operating System
- RAM
- Storage
- Keyboard
- Screen

Nobody installs these basic components after you buy it.

The laptop is already prepared to use.

Similarly, when Python creates an object, the constructor prepares that object by storing its initial data.

---

# Constructor Syntax

```python
class Student:

    def __init__(self):
        print("Student object created")


student1 = Student()
```

### Output

```
Student object created
```

Here,

- `student1 = Student()` creates the object.
- Python automatically calls `__init__()`.
- The message is printed without calling `__init__()` manually.

---

# Constructor with Parameters

Most of the time, constructors are used to store information inside an object.

```python
class Student:

    def __init__(self, name, age):
        self.name = name
        self.age = age


student1 = Student("Gokul", 20)
```

Python automatically matches the values.

| Parameter | Value |
|-----------|-------|
| self | student1 |
| name | Gokul |
| age | 20 |

Now the object contains:

```
student1

Name = Gokul
Age = 20
```

---

# How the Constructor Works

Suppose we write

```python
student1 = Student("Gokul", 20)
```

Python performs the following steps automatically.

### Step 1

Creates an empty object.

```
student1

Empty Object
```

---

### Step 2

Automatically calls

```python
__init__(student1, "Gokul", 20)
```

---

### Step 3

Executes

```python
self.name = name
```

which becomes

```python
student1.name = "Gokul"
```

---

### Step 4

Executes

```python
self.age = age
```

which becomes

```python
student1.age = 20
```

Now the object looks like

```
student1

Name = Gokul
Age = 20
```

The object is now ready to use.

---

# Types of Constructors

Python mainly has two types of constructors.

## 1. Default Constructor

A default constructor does **not** take any extra values except `self`.

```python
class Car:

    def __init__(self):
        print("A new car object is created.")


car1 = Car()
```

### Output

```
A new car object is created.
```

---

## 2. Parameterized Constructor

A parameterized constructor accepts values while creating the object.

```python
class Car:

    def __init__(self, brand, color):
        self.brand = brand
        self.color = color


car1 = Car("Audi", "Red")
car2 = Car("BMW", "Blue")

print(car1.brand)
print(car2.color)
```

### Output

```
Audi
Blue
```

---

# Beginner Python Example

```python
class Student:

    def __init__(self, name):
        self.name = name

    def introduce(self):
        print(f"Hello, my name is {self.name}.")


student1 = Student("Gokul")
student2 = Student("Alice")

student1.introduce()
student2.introduce()
```

### Output

```
Hello, my name is Gokul.
Hello, my name is Alice.
```

---

# Intermediate Python Example

```python
class Laptop:

    def __init__(self, brand, ram, storage):
        self.brand = brand
        self.ram = ram
        self.storage = storage

    def show_details(self):
        print(f"Brand   : {self.brand}")
        print(f"RAM     : {self.ram} GB")
        print(f"Storage : {self.storage} GB")


laptop1 = Laptop("Dell", 16, 512)
laptop2 = Laptop("HP", 8, 256)

laptop1.show_details()

print()

laptop2.show_details()
```

### Output

```
Brand   : Dell
RAM     : 16 GB
Storage : 512 GB

Brand   : HP
RAM     : 8 GB
Storage : 256 GB
```

---

# Summary

- A **constructor** is a special method that runs automatically when an object is created.
- In Python, the constructor is written as `__init__()`.
- The constructor initializes an object by storing its initial data.
- Python automatically calls the constructor whenever a new object is created.
- Python has two common types of constructors:
  - **Default Constructor** – accepts only `self`.
  - **Parameterized Constructor** – accepts `self` and additional values.
