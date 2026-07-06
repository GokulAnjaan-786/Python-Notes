# Private Access Specifier in Python

## What is a Private Access Specifier?

A **Private Access Specifier** means that a variable or method is **meant to be used only inside the class where it is created**.

In Python, a private variable is created by adding **two underscores (`__`)** before the variable name.

In simple words,

> **A private variable should not be accessed directly from outside the class.**

Private variables are usually used to store **important or sensitive information**.

Examples:

- Password
- ATM PIN
- Bank Balance
- OTP
- Security Code

---

# Real-World Example

Imagine your bank account.

Your bank account contains

- Name
- Account Number
- Balance
- ATM PIN

Should everyone know your ATM PIN?

**No.**

Should everyone change your ATM PIN directly?

**No.**

Only the bank system should access it.

Similarly,

in Python,

private variables protect important information.

---

# Syntax

```python
class BankAccount:

    def __init__(self):
        self.__pin = "1234"
```

Notice

```python
self.__pin
```

There are **two underscores (`__`)** before `pin`.

This makes it a **Private Variable**.

---

# Intermediate Python Example

```python
class BankAccount:

    def __init__(self, account_holder, balance, pin):
        self.account_holder = account_holder
        self._balance = balance
        self.__pin = pin

    def show_details(self):
        print(f"Account Holder : {self.account_holder}")
        print(f"Balance        : ₹{self._balance}")

    def check_pin(self, entered_pin):

        if entered_pin == self.__pin:
            print("PIN Verified")
            print("Access Granted")

        else:
            print("Incorrect PIN")
            print("Access Denied")


account1 = BankAccount("Gokul", 50000, "1234")
account2 = BankAccount("Alice", 75000, "5678")

accounts = [
    account1,
    account2
]

for account in accounts:

    account.show_details()

    pin = input(f"Enter PIN for {account.account_holder}: ")

    account.check_pin(pin)

    print("-" * 40)
```

---

# Sample Output

```
Account Holder : Gokul
Balance        : ₹50000
Enter PIN for Gokul: 1234
PIN Verified
Access Granted
----------------------------------------

Account Holder : Alice
Balance        : ₹75000
Enter PIN for Alice: 1111
Incorrect PIN
Access Denied
----------------------------------------
```

---

# Step-by-Step Explanation

## Step 1

A class named

```python
BankAccount
```

is created.

The constructor stores three variables.

```python
self.account_holder
```

Public Variable

```python
self._balance
```

Protected Variable

```python
self.__pin
```

Private Variable

---

## Step 2

Two BankAccount objects are created.

```python
account1 = BankAccount("Gokul", 50000, "1234")

account2 = BankAccount("Alice", 75000, "5678")
```

Python stores

### account1

```
Account Holder = Gokul

Balance = 50000

PIN = 1234
```

### account2

```
Account Holder = Alice

Balance = 75000

PIN = 5678
```

---

## Step 3

Both objects are stored inside one list.

```python
accounts = [
    account1,
    account2
]
```

---

## Step 4

Python starts the loop.

```python
for account in accounts:
```

During every iteration,

the variable

```python
account
```

points to one object.

First iteration

```
account

↓

account1
```

Second iteration

```
account

↓

account2
```

---

## Step 5

Python executes

```python
account.show_details()
```

This displays

- Account Holder
- Balance

Notice

The PIN is **not displayed**.

---

## Step 6

Python asks the user

```python
Enter PIN
```

The entered PIN is stored inside

```python
pin
```

---

## Step 7

Python executes

```python
account.check_pin(pin)
```

Inside the method,

Python compares

```python
entered_pin
```

with

```python
self.__pin
```

If both are equal,

Python prints

```
PIN Verified

Access Granted
```

Otherwise,

Python prints

```
Incorrect PIN

Access Denied
```

---

# Can We Access a Private Variable Directly?

Suppose we write

```python
print(account1.__pin)
```

Python gives an error.

```
AttributeError
```

Why?

Because

```python
__pin
```

is a **Private Variable**.

It cannot be accessed directly outside the class.

---

# The Correct Way

The correct way is to create a method inside the class.

Example

```python
class BankAccount:

    def __init__(self):
        self.__pin = "1234"

    def show_pin(self):
        print(self.__pin)


account = BankAccount()

account.show_pin()
```

Output

```
1234
```

The method belongs to the class,

so it can access the private variable.

---

# Important Concept: Name Mangling

Many beginners think

```python
self.__pin
```

is completely hidden.

Actually,

Python changes its name internally.

Suppose we write

```python
class BankAccount:

    def __init__(self):
        self.__pin = "1234"
```

Python internally changes it to

```python
_BankAccount__pin
```

This process is called

> **Name Mangling**

The purpose of Name Mangling is to reduce accidental access or accidental name conflicts.

As a beginner,

you should **not** access private variables using the mangled name.

Always use methods inside the class.

---

# Private Variable with Inheritance

```python
class Parent:

    def __init__(self):
        self.__salary = 50000


class Child(Parent):

    def show_salary(self):
        print(self.__salary)
```

This program gives an error.

Why?

Because

```python
__salary
```

belongs only to the `Parent` class.

The child class cannot access it directly.

If you want child classes to access a variable,

use a **Protected Variable (`_salary`)** instead of a Private Variable.

---

# How Python Executes the Program

When Python executes

```python
account1 = BankAccount("Gokul", 50000, "1234")
```

Python performs these steps.

### Step 1

Creates an empty object.

```
account1

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
self.account_holder = account_holder

self._balance = balance

self.__pin = pin
```

Now the object becomes

```
account1

Account Holder = Gokul

Balance = 50000

PIN = 1234
```

(The PIN is stored internally using name mangling.)

---

### Step 4

The loop starts.

Python takes one object from the list.

Calls

```python
account.show_details()
```

Displays

- Account Holder
- Balance

---

### Step 5

Python asks the user for the PIN.

Then executes

```python
account.check_pin(pin)
```

Inside this method,

Python compares

```python
entered_pin
```

with

```python
self.__pin
```

If both are equal,

access is granted.

Otherwise,

access is denied.

---

# Public vs Protected vs Private

| Feature | Public | Protected | Private |
|---------|---------|-----------|----------|
| Symbol | `variable` | `_variable` | `__variable` |
| Access inside class | ✅ Yes | ✅ Yes | ✅ Yes |
| Access in child class | ✅ Yes | ✅ Yes | ❌ No (directly) |
| Access outside class | ✅ Yes | ✅ Yes (Not Recommended) | ❌ No |
| Common Example | Name | Salary | Password, PIN |

---

# Easy Way to Remember

Imagine your house.

### Public

```
Living Room
```

Everyone can enter.

---

### Protected

```
Family Room
```

Mainly for family members.

Guests should avoid entering.

---

### Private

```
Locker
```

Only you can open it.

No one else should access it directly.

---

# Summary

- A Private Variable uses **two underscores (`__`)**.
- Private variables are meant to be used only inside the class.
- Private variables cannot be accessed directly from outside the class.
- The correct way to use a private variable is through methods inside the class.
- Python internally changes the variable name. This is called **Name Mangling**.
- Child classes cannot directly access private variables.
- Private variables are commonly used for passwords, ATM PINs, OTPs, security codes, and other sensitive information.
