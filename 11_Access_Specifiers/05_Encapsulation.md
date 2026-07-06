# Encapsulation in Python

## What is Encapsulation?

**Encapsulation** means **keeping the data and the methods that work on that data together inside one class and protecting the data from being changed directly.**

In simple words,

> **Encapsulation means protecting important data and allowing it to be accessed or changed only through methods.**

The user should not directly change important data.

Instead, the user should use the methods provided by the class.

---

# Real-World Example

## ATM Machine

Imagine an ATM.

You can

- Check Balance
- Deposit Money
- Withdraw Money

Can you directly type

```
Balance = ₹10,00,000
```

No.

You must use

```
Deposit Money

or

Withdraw Money
```

The balance is protected.

Only the ATM system can change it.

This is **Encapsulation**.

---

# Another Real-World Example

Imagine your Instagram account.

You have

- Username
- Password

Can someone directly change your password?

No.

They must follow the correct process.

```
Enter Current Password

↓

Verify Password

↓

Enter New Password

↓

Password Updated
```

The password is protected.

This is Encapsulation.

---

# Why Do We Need Encapsulation?

Suppose a bank account has

```
Balance = ₹50000
```

Without Encapsulation,

someone could write

```python
account.balance = -5000
```

or

```python
account.balance = 100000000
```

Both are wrong.

Instead,

the balance should only be changed through methods like

```python
deposit()
```

or

```python
withdraw()
```

These methods first check whether the operation is valid.

This keeps the data safe.

---

# How Do We Achieve Encapsulation?

Encapsulation is achieved using

- Private Variables
- Getter Methods
- Setter Methods

The data is stored as a private variable.

The user cannot directly access it.

The user must use methods provided by the class.

---

# Private Variable

A private variable starts with **two underscores (`__`)**.

Example

```python
self.__balance
```

A private variable cannot be accessed directly from outside the class.

---

# Getter Method

A Getter Method is used to **read** the value of a private variable.

Example

```python
def get_balance(self):
    return self.__balance
```

The Getter only returns the value.

It does not change it.

---

# Setter Method

A Setter Method is used to **update** the value of a private variable.

Before updating,

it can check whether the new value is valid.

Example

```python
def set_balance(self, amount):

    if amount >= 0:
        self.__balance = amount
    else:
        print("Invalid Balance")
```

This prevents incorrect data from being stored.

---

# Syntax

```python
class ClassName:

    def __init__(self):
        self.__variable = value

    def get_variable(self):
        return self.__variable

    def set_variable(self, value):
        self.__variable = value
```

---

# Beginner Python Example

```python
class Student:

    def __init__(self, name, marks):
        self.name = name
        self.__marks = marks

    def get_marks(self):
        return self.__marks


student = Student("Gokul", 95)

print(student.get_marks())
```

### Output

```
95
```

---

# How This Program Works

The marks are stored inside

```python
self.__marks
```

This makes the marks private.

The user cannot directly write

```python
student.__marks
```

Instead,

the user uses

```python
student.get_marks()
```

The Getter Method safely returns the marks.

---

# Intermediate Python Example

```python
class BankAccount:

    def __init__(self, account_holder, balance):
        self.account_holder = account_holder
        self.__balance = balance

    def get_balance(self):
        return self.__balance

    def deposit(self, amount):

        if amount > 0:
            self.__balance += amount
            print(f"₹{amount} Deposited Successfully")
        else:
            print("Invalid Amount")

    def withdraw(self, amount):

        if amount <= self.__balance:
            self.__balance -= amount
            print(f"₹{amount} Withdrawn Successfully")
        else:
            print("Insufficient Balance")


account = BankAccount("Gokul", 10000)

print(f"Current Balance : ₹{account.get_balance()}")

account.deposit(5000)

print(f"Current Balance : ₹{account.get_balance()}")

account.withdraw(3000)

print(f"Current Balance : ₹{account.get_balance()}")
```

### Output

```
Current Balance : ₹10000

₹5000 Deposited Successfully

Current Balance : ₹15000

₹3000 Withdrawn Successfully

Current Balance : ₹12000
```

---

# Step-by-Step Explanation

## Step 1

The class stores

```python
self.__balance
```

The balance is private.

No one can change it directly.

---

## Step 2

The Getter Method

```python
get_balance()
```

returns the current balance.

---

## Step 3

The Deposit Method

```python
deposit()
```

checks

```python
if amount > 0
```

If the amount is valid,

the balance increases.

Otherwise,

Python prints

```
Invalid Amount
```

---

## Step 4

The Withdraw Method

```python
withdraw()
```

checks

```python
if amount <= self.__balance
```

If enough balance is available,

Python deducts the amount.

Otherwise,

Python prints

```
Insufficient Balance
```

---

# Hard-Level Python Example

This example combines

- Classes
- Objects
- Constructors
- Encapsulation
- Private Variables
- Getter Methods
- Setter Methods
- Lists
- Loops
- Conditional Statements
- User Input

```python
class Employee:

    def __init__(self, name, salary):
        self.name = name
        self.__salary = salary

    def get_salary(self):
        return self.__salary

    def set_salary(self, new_salary):

        if new_salary >= 15000:
            self.__salary = new_salary
            print("Salary Updated Successfully")
        else:
            print("Salary Cannot Be Less Than ₹15000")


employees = [
    Employee("Gokul", 60000),
    Employee("Alice", 45000)
]


for employee in employees:

    print("-" * 35)

    print(f"Employee Name : {employee.name}")

    print(f"Current Salary : ₹{employee.get_salary()}")

    choice = input("Do you want to update salary? (yes/no): ")

    if choice.lower() == "yes":

        new_salary = int(input("Enter New Salary : "))

        employee.set_salary(new_salary)

        print(f"Updated Salary : ₹{employee.get_salary()}")

    else:

        print("Salary Not Updated")
```

### Sample Output

```
-----------------------------------

Employee Name : Gokul

Current Salary : ₹60000

Do you want to update salary? (yes/no): yes

Enter New Salary : 70000

Salary Updated Successfully

Updated Salary : ₹70000
```

---

# How This Program Works

## Step 1

Every employee stores

```python
self.__salary
```

The salary is private.

---

## Step 2

The program cannot directly access

```python
employee.__salary
```

Instead,

it uses

```python
employee.get_salary()
```

---

## Step 3

If the user wants to update the salary,

the program calls

```python
employee.set_salary(new_salary)
```

---

## Step 4

Before updating,

Python checks

```python
if new_salary >= 15000
```

If the salary is valid,

Python updates it.

Otherwise,

Python displays

```
Salary Cannot Be Less Than ₹15000
```

This prevents incorrect data from being stored.

---

# Difference Between Access Specifiers and Encapsulation

| Access Specifiers | Encapsulation |
|-------------------|---------------|
| Decide who can access the data | Protects the data and controls how it is accessed or updated |
| Uses Public, Protected and Private | Uses Private Variables together with Getter and Setter Methods |
| Focuses on access | Focuses on safe data handling |

---

# Summary

- **Encapsulation** means protecting important data and allowing it to be accessed or changed only through methods.
- Private variables are commonly used for encapsulation.
- A **Getter Method** is used to read a private variable.
- A **Setter Method** is used to update a private variable safely.
- A Setter Method can validate the input before updating the value.
- Encapsulation helps prevent invalid or incorrect data from being stored.
- Real-world examples include ATM machines, bank accounts, online payment systems, and social media accounts where sensitive information is protected.
