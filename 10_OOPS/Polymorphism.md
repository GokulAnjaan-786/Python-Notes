# Polymorphism in Python

## What is Polymorphism?

The word **Polymorphism** is made up of two words.

- **Poly** = Many
- **Morph** = Forms

So,

> **Polymorphism means one thing can have many forms.**

In Python,

> **The same method can behave differently for different objects.**

The method name remains the same, but the output changes depending on the object that calls it.

---

# Real-World Example

Imagine a remote control.

It has a **Power** button.

When you press the Power button,

On a TV

```
TV turns ON
```

On an Air Conditioner

```
AC turns ON
```

On a Projector

```
Projector turns ON
```

The button is the same.

The action is the same.

But the result is different.

This is called **Polymorphism**.

---

# Another Real-World Example

Think about different animals.

Every animal can make a sound.

But,

Dog

```
Bark
```

Cat

```
Meow
```

Cow

```
Moo
```

The method is always

```python
sound()
```

But every animal gives a different output.

This is Polymorphism.

---

# Syntax

```python
class Parent:

    def method(self):
        print("Parent Method")


class Child(Parent):

    def method(self):
        print("Child Method")
```

Here,

The child class has the same method as the parent class.

But the child class changes the behavior of that method.

This is called **Method Overriding**, which is the most common way to achieve polymorphism in Python.

---

# Beginner Python Example

```python
class Animal:

    def sound(self):
        print("Animal makes a sound.")


class Dog(Animal):

    def sound(self):
        print("Dog barks.")


class Cat(Animal):

    def sound(self):
        print("Cat meows.")


dog = Dog()
cat = Cat()

dog.sound()
cat.sound()
```

### Output

```
Dog barks.
Cat meows.
```

---

# How This Program Works

Suppose we write

```python
dog.sound()
```

Python checks

```
Does Dog have sound()?

Yes
```

So Python executes

```python
Dog.sound()
```

Now,

```python
cat.sound()
```

Python checks

```
Does Cat have sound()?

Yes
```

So Python executes

```python
Cat.sound()
```

The method name is the same.

The output is different.

This is Polymorphism.

---

# Intermediate Python Example

```python
class Vehicle:

    def start(self):
        print("Vehicle is starting.")


class Car(Vehicle):

    def start(self):
        print("Car starts using a key.")


class Bike(Vehicle):

    def start(self):
        print("Bike starts using the self-start button.")


class ElectricCar(Vehicle):

    def start(self):
        print("Electric car starts silently.")


car = Car()
bike = Bike()
electric = ElectricCar()

car.start()
bike.start()
electric.start()
```

### Output

```
Car starts using a key.
Bike starts using the self-start button.
Electric car starts silently.
```

---

# Practical Python Example

This example combines

- Classes
- Objects
- Constructors
- Inheritance
- Polymorphism
- Method Overriding
- Lists
- Loops
- Conditional Statements
- User Input

```python
class User:

    def __init__(self, name):
        self.name = name

    def login(self):
        print(f"{self.name} logged in.")

    def get_dashboard(self):
        print("Opening Dashboard...")


class Student(User):

    def login(self):
        print(f"{self.name} logged in as Student.")

    def get_dashboard(self):
        print("Opening Student Dashboard...")


class Teacher(User):

    def login(self):
        print(f"{self.name} logged in as Teacher.")

    def get_dashboard(self):
        print("Opening Teacher Dashboard...")


class Admin(User):

    def login(self):
        print(f"{self.name} logged in as Admin.")

    def get_dashboard(self):
        print("Opening Admin Dashboard...")


student = Student("Gokul")
teacher = Teacher("Alice")
admin = Admin("Rahul")


users = [
    student,
    teacher,
    admin
]


password = input("Enter Password: ")

if password == "python123":

    print("\nLogin Successful\n")

    for user in users:

        user.login()
        user.get_dashboard()

        choice = input("Do you want to logout? (yes/no): ")

        if choice.lower() == "yes":
            print("Logged out successfully.")
        else:
            print("You are still logged in.")

        print("-" * 40)

else:

    print("\nInvalid Password.")
    print("Access Denied.")
```

---

# Sample Output (Correct Password)

```
Enter Password: python123

Login Successful

Gokul logged in as Student.
Opening Student Dashboard...
Do you want to logout? (yes/no): yes
Logged out successfully.
----------------------------------------

Alice logged in as Teacher.
Opening Teacher Dashboard...
Do you want to logout? (yes/no): no
You are still logged in.
----------------------------------------

Rahul logged in as Admin.
Opening Admin Dashboard...
Do you want to logout? (yes/no): yes
Logged out successfully.
----------------------------------------
```

---

# How This Program Works

### Step 1

Three child classes are created.

- Student
- Teacher
- Admin

All of them inherit from the **User** class.

---

### Step 2

Each child class overrides the same methods.

```python
login()

get_dashboard()
```

Although the method names are the same, each class gives a different output.

This is Polymorphism.

---

### Step 3

Three objects are created.

```python
student = Student("Gokul")
teacher = Teacher("Alice")
admin = Admin("Rahul")
```

---

### Step 4

All objects are stored inside one list.

```python
users = [
    student,
    teacher,
    admin
]
```

Python allows us to store objects inside a list.

---

### Step 5

The user enters a password.

```python
password = input("Enter Password: ")
```

If the password is correct,

Python enters the loop.

Otherwise,

the program stops.

---

### Step 6

Python starts the loop.

```python
for user in users:
```

During every iteration,

the variable `user` points to one object.

First iteration

```
user

↓

Student Object
```

Second iteration

```
user

↓

Teacher Object
```

Third iteration

```
user

↓

Admin Object
```

---

### Step 7

Inside the loop,

Python executes

```python
user.login()
```

For the Student object,

Python runs

```python
Student.login()
```

For the Teacher object,

Python runs

```python
Teacher.login()
```

For the Admin object,

Python runs

```python
Admin.login()
```

Notice that the code is exactly the same.

```python
user.login()
```

Only the object changes.

Python automatically executes the correct method.

This is Polymorphism.

---

### Step 8

Python executes

```python
user.get_dashboard()
```

Again,

every object displays a different dashboard.

Student

```
Opening Student Dashboard...
```

Teacher

```
Opening Teacher Dashboard...
```

Admin

```
Opening Admin Dashboard...
```

The method name is the same.

Only the output changes.

---

### Step 9

The program asks

```python
Do you want to logout?
```

If the answer is

```
yes
```

Output

```
Logged out successfully.
```

Otherwise

```
You are still logged in.
```

This is done using an `if-else` statement.

---

# Summary

- **Polymorphism** means one method can have different behaviors.
- The method name remains the same.
- Different objects execute different versions of the same method.
- Polymorphism is commonly achieved using **Inheritance** and **Method Overriding**.
- Python automatically calls the correct method depending on the object.
- Polymorphism works very well with loops because one loop can process many different objects using the same method name.
