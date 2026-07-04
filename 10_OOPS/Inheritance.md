# Inheritance in Python

## What is Inheritance?

**Inheritance** is a feature in Python that allows one class to **reuse the properties and methods of another class**.

Instead of writing the same code again and again, we can write it once in a parent class and allow other classes to use it.

In simple words,

> **Inheritance means one class using the code of another class.**

It helps us avoid writing duplicate code.

---

# Real-World Example

Imagine a company.

Every employee has:

- Name
- Employee ID

Now there are different types of employees.

### Manager

- Name
- Employee ID
- Team Size

### Developer

- Name
- Employee ID
- Programming Language

Instead of writing **Name** and **Employee ID** again for every employee type, we create one class called **Employee**.

Then **Manager** and **Developer** inherit from **Employee**.

```
              Employee
           (Parent Class)
          ----------------
          Name
          Employee ID
          ----------------
                 │
      -------------------------
      │                       │
      ▼                       ▼

    Manager             Developer
 (Child Class)        (Child Class)

 Team Size        Programming Language
```

Both child classes automatically get:

- Name
- Employee ID

from the parent class.

---

# Parent Class

The class that already exists and shares its code with other classes.

Example:

```python
class Employee:
    pass
```

---

# Child Class

The class that inherits the properties and methods from the parent class.

Example:

```python
class Manager(Employee):
    pass
```

Here,

`Manager` inherits from `Employee`.

---

# Syntax of Inheritance

```python
class Parent:
    pass


class Child(Parent):
    pass
```

Notice this line:

```python
class Child(Parent):
```

The class name inside the brackets tells Python:

> "The Child class should inherit everything from the Parent class."

---

# Beginner Python Example

## Step 1: Create the Parent Class

```python
class Animal:

    def __init__(self, name):
        self.name = name

    def eat(self):
        print(f"{self.name} is eating.")
```

The parent class contains:

- One attribute → `name`
- One method → `eat()`

---

## Step 2: Create the Child Class

```python
class Dog(Animal):
    pass
```

Here,

`Dog` inherits from `Animal`.

---

## Step 3: Create an Object

```python
dog1 = Dog("Tommy")
```

Even though `Dog` does not have its own constructor, it can still store the name because it inherited the constructor from `Animal`.

---

## Step 4: Call the Method

```python
dog1.eat()
```

### Output

```
Tommy is eating.
```

---

# Complete Beginner Example

```python
class Animal:

    def __init__(self, name):
        self.name = name

    def eat(self):
        print(f"{self.name} is eating.")


class Dog(Animal):
    pass


dog1 = Dog("Tommy")

dog1.eat()
```

### Output

```
Tommy is eating.
```

---

# How Python Executes This Program

Suppose we write

```python
dog1 = Dog("Tommy")
```

Python performs the following steps.

### Step 1

Creates an empty object.

```
dog1

Empty Object
```

---

### Step 2

Checks whether the `Dog` class has its own constructor.

```
Dog

__init__() ?

No
```

---

### Step 3

Python moves to the parent class.

```
Animal

__init__() ?

Yes
```

---

### Step 4

Python executes the parent constructor.

```python
self.name = name
```

Now the object becomes

```
dog1

Name = Tommy
```

---

### Step 5

When we write

```python
dog1.eat()
```

Python first checks

```
Does Dog have eat()?

No
```

Then Python checks

```
Does Animal have eat()?

Yes
```

So Python executes the parent's method.

Output

```
Tommy is eating.
```

---

# Child Class with Its Own Method

A child class can also have its own methods.

```python
class Animal:

    def __init__(self, name):
        self.name = name

    def eat(self):
        print(f"{self.name} is eating.")


class Dog(Animal):

    def bark(self):
        print(f"{self.name} is barking.")


dog1 = Dog("Tommy")

dog1.eat()
dog1.bark()
```

### Output

```
Tommy is eating.
Tommy is barking.
```

The child class now has

Inherited method

- `eat()`

Own method

- `bark()`

---

# What is `super()`?

Sometimes the child class needs its own constructor.

At the same time, it also wants to use the parent's constructor.

For this, Python provides

```python
super()
```

`super()` is used to call the parent class constructor.

---

# Syntax of `super()`

```python
super().__init__(arguments)
```

---

# Intermediate Python Example

```python
class Product:

    def __init__(self, product_name, price):
        self.product_name = product_name
        self.price = price

    def show_details(self):
        print(f"Product Name : {self.product_name}")
        print(f"Price        : ₹{self.price}")


class Electronics(Product):

    def __init__(self, product_name, price, warranty):

        super().__init__(product_name, price)

        self.warranty = warranty

    def show_warranty(self):
        print(f"{self.product_name} comes with {self.warranty} years of warranty.")


p1 = Electronics("Lenovo", 50000, 2)
p2 = Electronics("Dell", 60000, 3)

p1.show_details()
p1.show_warranty()

print()

p2.show_details()
p2.show_warranty()
```

### Output

```
Product Name : Lenovo
Price        : ₹50000
Lenovo comes with 2 years of warranty.

Product Name : Dell
Price        : ₹60000
Dell comes with 3 years of warranty.
```

---

# How `super()` Works

Suppose we create an object.

```python
p1 = Electronics("Lenovo", 50000, 2)
```

Python first executes

```python
Electronics.__init__()
```

Inside it,

```python
super().__init__(product_name, price)
```

calls the parent constructor.

The parent constructor stores

```python
self.product_name = product_name
self.price = price
```

Then the child constructor stores

```python
self.warranty = warranty
```

Now the object contains

```
p1

Product Name = Lenovo
Price = 50000
Warranty = 2
```

---

# Hard-Level Example

```python
class Person:

    def __init__(self, name, age):
        self.name = name
        self.age = age

    def show_details(self):
        print(f"Name : {self.name}")
        print(f"Age  : {self.age}")


class Doctor(Person):

    def __init__(self, name, age, specialization):
        super().__init__(name, age)
        self.specialization = specialization

    def treat_patient(self):
        print(f"Dr. {self.name} is treating a patient.")


doctor1 = Doctor("Gokul", 30, "Cardiologist")

doctor1.show_details()
print(f"Specialization : {doctor1.specialization}")
doctor1.treat_patient()
```

### Output

```
Name : Gokul
Age  : 30
Specialization : Cardiologist
Dr. Gokul is treating a patient.
```

---

# Program Flow of the Hard-Level Example

When we create

```python
doctor1 = Doctor("Gokul", 30, "Cardiologist")
```

Python performs these steps.

### Step 1

Creates an empty object.

---

### Step 2

Calls the child constructor.

```python
Doctor.__init__()
```

---

### Step 3

The child constructor executes

```python
super().__init__(name, age)
```

---

### Step 4

The parent constructor stores

```python
self.name = name
self.age = age
```

---

### Step 5

The child constructor stores

```python
self.specialization = specialization
```

Now the object becomes

```
doctor1

Name = Gokul
Age = 30
Specialization = Cardiologist
```

The object can now use

Inherited method

```python
show_details()
```

and its own method

```python
treat_patient()
```

---

# Summary

- **Inheritance** allows one class to reuse another class's code.
- The class that shares its code is called the **Parent Class**.
- The class that reuses the code is called the **Child Class**.
- A child class automatically gets the parent class's attributes and methods.
- Inheritance is created using:

```python
class Child(Parent):
```

- If the child class needs its own constructor but also wants the parent's constructor, use:

```python
super().__init__()
```

- A child class can:
  - Use the parent's methods.
  - Add its own methods.
  - Add its own attributes.
