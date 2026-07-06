# Python Module: Public, Protected and Private Access Specifiers

## Problem Statement

Create a **Student Management System** that demonstrates all three access specifiers in a single program.

The program should contain:

- Public Variable
- Protected Variable
- Private Variable
- Methods
- Objects
- List of Objects
- Loop
- Conditional Statements
- User Input

---

# Python Program

```python
class Student:

    def __init__(self, name, department, password):
        # Public Variable
        self.name = name

        # Protected Variable
        self._department = department

        # Private Variable
        self.__password = password

    # Public Method
    def show_details(self):
        print(f"Name       : {self.name}")
        print(f"Department : {self._department}")

    # Public Method
    def check_password(self, entered_password):

        if entered_password == self.__password:
            print("Login Successful")
        else:
            print("Incorrect Password")

    # Public Method
    def change_password(self, old_password, new_password):

        if old_password == self.__password:
            self.__password = new_password
            print("Password Changed Successfully")
        else:
            print("Old Password is Incorrect")


# Create Objects

student1 = Student("Gokul", "AIML", "python123")
student2 = Student("Alice", "Computer Science", "abc123")


# Store Objects Inside a List

students = [
    student1,
    student2
]


# Loop Through Every Student

for student in students:

    print("-" * 40)

    student.show_details()

    entered_password = input("Enter Password : ")

    student.check_password(entered_password)

    choice = input("Do you want to change password? (yes/no): ")

    if choice.lower() == "yes":

        old_password = input("Enter Old Password : ")

        new_password = input("Enter New Password : ")

        student.change_password(old_password, new_password)

    else:

        print("Password Not Changed")

print("-" * 40)
```

---

# Sample Output

```
----------------------------------------

Name       : Gokul
Department : AIML

Enter Password : python123

Login Successful

Do you want to change password? (yes/no): yes

Enter Old Password : python123

Enter New Password : welcome123

Password Changed Successfully

----------------------------------------

Name       : Alice
Department : Computer Science

Enter Password : hello

Incorrect Password

Do you want to change password? (yes/no): no

Password Not Changed

----------------------------------------
```

---

# Understanding the Program

## Step 1

A class named `Student` is created.

```python
class Student:
```

This class represents every student.

---

## Step 2

The constructor stores three variables.

```python
self.name
```

This is a **Public Variable**.

It can be accessed from anywhere.

Example

```python
print(student1.name)
```

---

```python
self._department
```

This is a **Protected Variable**.

It is mainly meant to be used

- Inside the class
- Inside child classes

Python still allows access outside the class,

but it is not recommended.

Example

```python
print(student1._department)
```

---

```python
self.__password
```

This is a **Private Variable**.

It should only be used inside the class.

Trying to access it directly

```python
print(student1.__password)
```

will give

```
AttributeError
```

---

# Step 3

Two student objects are created.

```python
student1 = Student("Gokul", "AIML", "python123")

student2 = Student("Alice", "Computer Science", "abc123")
```

Python stores

Student 1

```
Name = Gokul

Department = AIML

Password = python123
```

Student 2

```
Name = Alice

Department = Computer Science

Password = abc123
```

---

# Step 4

Both objects are stored inside one list.

```python
students = [
    student1,
    student2
]
```

Python allows objects to be stored inside lists.

---

# Step 5

Python starts the loop.

```python
for student in students:
```

During every iteration,

the variable

```python
student
```

points to one object.

Iteration 1

```
student

↓

student1
```

Iteration 2

```
student

↓

student2
```

---

# Step 6

Python executes

```python
student.show_details()
```

This method prints

- Public Variable (`name`)
- Protected Variable (`department`)

Notice

The password is **not printed**.

---

# Step 7

Python asks

```
Enter Password
```

The entered value is passed to

```python
student.check_password()
```

Inside this method,

Python compares

```python
entered_password
```

with

```python
self.__password
```

If both are equal

```
Login Successful
```

Otherwise

```
Incorrect Password
```

---

# Step 8

Python asks

```
Do you want to change password?
```

If the answer is

```
yes
```

Python asks

- Old Password
- New Password

Then executes

```python
student.change_password()
```

Inside this method,

Python again checks the old password.

If it matches,

the password is updated.

Otherwise,

Python displays

```
Old Password is Incorrect
```

---

# How This Program Uses All Three Access Specifiers

## Public

```python
self.name
```

Reason

The student's name is not secret.

It can be accessed from anywhere.

---

## Protected

```python
self._department
```

Reason

The department is mainly used inside the class or by child classes.

Python allows outside access,

but it is not recommended.

---

## Private

```python
self.__password
```

Reason

The password is sensitive information.

It should only be used inside the class.

It cannot be accessed directly outside the class.

---

# Summary

| Access Specifier | Symbol | Example | Access Outside Class |
|------------------|--------|---------|----------------------|
| Public | `variable` | `name` | ✅ Yes |
| Protected | `_variable` | `_department` | ✅ Yes (Not Recommended) |
| Private | `__variable` | `__password` | ❌ No |

---

# Key Points

- Public variables are open to everyone.
- Protected variables are mainly for the class and child classes.
- Private variables are only for the class itself.
- Public variables use **no underscore**.
- Protected variables use **one underscore (`_`)**.
- Private variables use **two underscores (`__`)**.
- Private variables are commonly used for passwords, PINs, OTPs, and other sensitive information.
