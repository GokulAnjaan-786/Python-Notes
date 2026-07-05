# Abstraction in Python

## What is Abstraction?

**Abstraction** means **showing only the necessary details to the user and hiding the internal working**.

In simple words,

> **The user knows what to do, but does not need to know how it works inside.**

The user only uses the feature.

The internal process remains hidden.

---

# Real-World Example

## ATM Machine

Suppose you go to an ATM.

You

- Insert your ATM card
- Enter your PIN
- Select **Withdraw Money**
- Receive cash

Do you know

- How the ATM checks your account?
- How the bank verifies your PIN?
- How the money is deducted?
- How the cash comes out?

No.

You only know how to use the ATM.

The internal working is hidden.

This is called **Abstraction**.

---

# Another Real-World Example

## Car

When you drive a car, you use

- Steering
- Brake
- Accelerator

You do not need to know

- How the engine works
- How fuel burns
- How the gearbox changes speed

You simply drive the car.

The complicated working is hidden.

This is Abstraction.

---

# How Abstraction is Implemented in Python

Python provides a module called

```python
abc
```

which stands for

```
Abstract Base Class
```

Using this module, we can create an **Abstract Class**.

---

# What is an Abstract Class?

An **Abstract Class** is a class that is used only as a blueprint.

It cannot be used to create objects directly.

Instead,

other classes inherit from it and complete the missing methods.

---

# What is an Abstract Method?

An **Abstract Method** is a method that has **only the method name**.

It does not contain any implementation.

The child class must write its own implementation.

---

# Syntax

```python
from abc import ABC, abstractmethod


class Parent(ABC):

    @abstractmethod
    def method(self):
        pass


class Child(Parent):

    def method(self):
        print("Method Implementation")
```

---

# Understanding the Syntax

## Step 1

```python
from abc import ABC, abstractmethod
```

This imports

- `ABC` → Used to create an abstract class.
- `abstractmethod` → Used to create an abstract method.

---

## Step 2

```python
class Parent(ABC):
```

Instead of writing

```python
class Parent:
```

we write

```python
class Parent(ABC):
```

This tells Python that

`Parent` is an abstract class.

---

## Step 3

```python
@abstractmethod
```

This tells Python

> Every child class **must** write this method.

---

## Step 4

```python
def method(self):
    pass
```

Notice that there is no code inside the method.

Only

```python
pass
```

This means

The parent class is only creating a rule.

The child class will write the actual code.

---

# Beginner Python Example

```python
from abc import ABC, abstractmethod


class Animal(ABC):

    @abstractmethod
    def sound(self):
        pass


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

The parent class says

```
Every animal must have a sound() method.
```

The parent class does not know

what sound every animal makes.

The child classes decide.

Dog

```
Dog barks.
```

Cat

```
Cat meows.
```

The parent creates the rule.

The child classes complete the rule.

This is Abstraction.

---

# What Happens if a Child Class Does Not Implement the Method?

Suppose we write

```python
from abc import ABC, abstractmethod


class Animal(ABC):

    @abstractmethod
    def sound(self):
        pass


class Dog(Animal):
    pass


dog = Dog()
```

Python gives an error.

```
TypeError

Can't instantiate abstract class Dog
with abstract method sound
```

This happens because

`Dog` did not implement the required method.

---

# Intermediate Python Example

Suppose every payment method must have a

```python
pay()
```

method.

Different payment methods complete the payment differently.

```python
from abc import ABC, abstractmethod


class Payment(ABC):

    @abstractmethod
    def pay(self):
        pass


class CreditCard(Payment):

    def pay(self):
        print("Payment completed using Credit Card.")


class UPI(Payment):

    def pay(self):
        print("Payment completed using UPI.")


class NetBanking(Payment):

    def pay(self):
        print("Payment completed using Net Banking.")


payments = [
    CreditCard(),
    UPI(),
    NetBanking()
]

for payment in payments:
    payment.pay()
```

### Output

```
Payment completed using Credit Card.
Payment completed using UPI.
Payment completed using Net Banking.
```

---

# How This Program Works

The parent class creates one rule.

```
Every payment method must have pay().
```

The parent does not know how payment happens.

Each child class writes its own implementation.

Then,

all objects are stored inside one list.

```python
payments = [
    CreditCard(),
    UPI(),
    NetBanking()
]
```

A loop is used.

```python
for payment in payments:
```

Python automatically executes the correct `pay()` method for every object.

---

# Hard-Level Python Example

This example combines

- Classes
- Objects
- Constructors
- Inheritance
- Abstraction
- Lists
- Loops
- Conditional Statements

```python
from abc import ABC, abstractmethod


class Employee(ABC):

    def __init__(self, name):
        self.name = name

    @abstractmethod
    def calculate_salary(self):
        pass


class Manager(Employee):

    def calculate_salary(self):
        return 80000


class Developer(Employee):

    def calculate_salary(self):
        return 60000


class Intern(Employee):

    def calculate_salary(self):
        return 15000


employees = [
    Manager("Gokul"),
    Developer("Alice"),
    Intern("Rahul")
]


for employee in employees:

    salary = employee.calculate_salary()

    print(f"Employee : {employee.name}")
    print(f"Salary   : ₹{salary}")

    if salary >= 50000:
        print("Senior Employee")
    else:
        print("Junior Employee")

    print("-" * 30)
```

### Output

```
Employee : Gokul
Salary   : ₹80000
Senior Employee
------------------------------

Employee : Alice
Salary   : ₹60000
Senior Employee
------------------------------

Employee : Rahul
Salary   : ₹15000
Junior Employee
------------------------------
```

---

# How This Program Works

## Step 1

The `Employee` class becomes an abstract class.

It creates one rule.

```
Every employee must calculate salary.
```

But it does not explain how.

---

## Step 2

Each child class implements the rule.

Manager

```python
calculate_salary()
```

returns

```
80000
```

Developer

returns

```
60000
```

Intern

returns

```
15000
```

---

## Step 3

Three objects are created.

```python
Manager("Gokul")
Developer("Alice")
Intern("Rahul")
```

---

## Step 4

All objects are stored inside one list.

```python
employees = [
    Manager("Gokul"),
    Developer("Alice"),
    Intern("Rahul")
]
```

---

## Step 5

Python starts the loop.

```python
for employee in employees:
```

During every iteration,

Python calls

```python
employee.calculate_salary()
```

Python automatically executes the correct method depending on the object.

---

## Step 6

The salary is stored inside the variable

```python
salary
```

Then

```python
if salary >= 50000:
```

checks whether the employee is a Senior Employee.

If the condition is true,

```
Senior Employee
```

is printed.

Otherwise,

```
Junior Employee
```

is printed.

---

# Summary

- **Abstraction** means hiding the internal working and showing only the necessary part.
- Python uses the `abc` module to create abstract classes.
- An abstract class is created using `ABC`.
- An abstract method is created using `@abstractmethod`.
- An abstract class cannot be used to create objects directly.
- Every child class must implement all abstract methods.
- The parent class creates the rule.
- The child classes complete the rule.
- Abstraction is useful when every child class must provide its own implementation of the same method.
