# Exception Handling in Python

## What is Exception Handling?

**Exception Handling** is a way to handle errors that happen while a program is running.

In simple words,

> **Exception Handling prevents the program from stopping when an error occurs.**

Instead of crashing,

Python handles the error and continues running the program.

---

# Real-World Example

## ATM Machine

Suppose you have **₹5000** in your bank account.

You try to withdraw

```
₹10000
```

Should the ATM stop working?

No.

It should display

```
Insufficient Balance
```

and continue working.

This is exactly what Exception Handling does.

---

# Another Real-World Example

Imagine you are logging into your email account.

You enter a wrong password.

Should the website crash?

No.

It simply displays

```
Invalid Password
```

and asks you to try again.

This is Exception Handling.

---

# Why Do We Need Exception Handling?

Suppose we write

```python
number = int(input("Enter a Number: "))
```

If the user enters

```
hello
```

Python cannot convert it into an integer.

Without Exception Handling,

the program stops immediately.

With Exception Handling,

the program displays a proper message and continues running.

---

# Syntax

```python
try:

    # Code that may cause an error

except:

    # Code that runs if an error occurs
```

---

# How Exception Handling Works

Python first executes the code inside

```python
try
```

If no error occurs,

Python skips the `except` block.

If an error occurs,

Python immediately jumps to

```python
except
```

and executes the code inside it.

---

# Flow of Execution

```
Program Starts

↓

try Block

↓

Did an Error Occur?

↓

No ------------------> Continue Program

↓

Yes

↓

except Block

↓

Continue Program
```

---

# Beginner Python Example

```python
try:

    number = int(input("Enter a Number: "))

    print(f"You entered: {number}")

except:

    print("Please enter numbers only.")
```

### Output (Valid Input)

```
Enter a Number:
25

You entered: 25
```

### Output (Invalid Input)

```
Enter a Number:
hello

Please enter numbers only.
```

---

# How This Program Works

Python starts with

```python
try
```

If the user enters

```
25
```

Python converts it into an integer.

No error occurs.

The number is printed.

If the user enters

```
hello
```

Python cannot convert it into an integer.

Instead of stopping the program,

Python jumps to

```python
except
```

and prints

```
Please enter numbers only.
```

---

# Common Exceptions

| Exception | Meaning |
|-----------|---------|
| ValueError | Wrong value entered |
| ZeroDivisionError | Division by zero |
| TypeError | Wrong data type |
| IndexError | Invalid list index |
| KeyError | Invalid dictionary key |
| FileNotFoundError | File does not exist |

---

# Handling Different Exceptions

```python
try:

    number = int(input("Enter a Number: "))

    result = 100 / number

    print(result)

except ValueError:

    print("Please enter numbers only.")

except ZeroDivisionError:

    print("Cannot divide by zero.")
```

### Output 1

```
Enter a Number:
hello

Please enter numbers only.
```

### Output 2

```
Enter a Number:
0

Cannot divide by zero.
```

---

# else Block

The `else` block runs **only if there is no error**.

```python
try:

    number = int(input("Enter Number: "))

except ValueError:

    print("Invalid Input")

else:

    print("Number Entered Successfully")
```

### Output

```
Enter Number:
50

Number Entered Successfully
```

---

# finally Block

The `finally` block always runs.

Whether an error happens or not,

Python executes the code inside `finally`.

```python
try:

    number = int(input("Enter Number: "))

except ValueError:

    print("Invalid Input")

finally:

    print("Program Finished")
```

### Output (Invalid Input)

```
Enter Number:
hello

Invalid Input

Program Finished
```

### Output (Valid Input)

```
Enter Number:
20

Program Finished
```

---

# Complete Syntax

```python
try:

    # Code that may cause an error

except:

    # Runs if an error occurs

else:

    # Runs if no error occurs

finally:

    # Always runs
```

---

# Intermediate Python Example

```python
students = ["Gokul", "Alice", "Rahul"]

try:

    index = int(input("Enter Student Index: "))

    print(f"Student Name: {students[index]}")

except IndexError:

    print("Student Not Found.")

except ValueError:

    print("Please enter numbers only.")

finally:

    print("Program Finished.")
```

### Output 1

```
Enter Student Index:
1

Student Name: Alice

Program Finished.
```

### Output 2

```
Enter Student Index:
5

Student Not Found.

Program Finished.
```

### Output 3

```
Enter Student Index:
abc

Please enter numbers only.

Program Finished.
```

---

# How This Program Works

## Step 1

A list of students is created.

```python
students = ["Gokul", "Alice", "Rahul"]
```

---

## Step 2

Python asks the user to enter a student index.

---

## Step 3

Python enters the `try` block.

If the user enters

```
1
```

Python prints

```
Alice
```

---

## Step 4

If the user enters

```
5
```

there is no student at index 5.

Python raises

```
IndexError
```

The program jumps to

```python
except IndexError
```

and prints

```
Student Not Found.
```

---

## Step 5

If the user enters

```
abc
```

Python cannot convert it into an integer.

Python raises

```
ValueError
```

The program jumps to

```python
except ValueError
```

and prints

```
Please enter numbers only.
```

---

## Step 6

Finally,

Python executes

```python
finally
```

which prints

```
Program Finished.
```

This block runs every time.

---

# Practical Python Example

This example combines

- Classes
- Objects
- Constructors
- Encapsulation
- Exception Handling
- Loops
- Conditional Statements
- User Input

```python
class BankAccount:

    def __init__(self, name, balance):
        self.name = name
        self.__balance = balance

    def show_balance(self):
        print(f"Current Balance : ₹{self.__balance}")

    def withdraw(self):

        try:

            amount = int(input("Enter Withdrawal Amount: "))

            if amount <= 0:
                print("Amount must be greater than zero.")

            elif amount > self.__balance:
                print("Insufficient Balance.")

            else:
                self.__balance -= amount
                print("Withdrawal Successful.")

        except ValueError:

            print("Please enter numbers only.")


accounts = [
    BankAccount("Gokul", 10000),
    BankAccount("Alice", 5000)
]

for account in accounts:

    print("-" * 35)

    print(f"Account Holder : {account.name}")

    account.show_balance()

    account.withdraw()

    account.show_balance()
```

### Sample Output

```
-----------------------------------

Account Holder : Gokul

Current Balance : ₹10000

Enter Withdrawal Amount:
abc

Please enter numbers only.

Current Balance : ₹10000
```

### Another Output

```
-----------------------------------

Account Holder : Alice

Current Balance : ₹5000

Enter Withdrawal Amount:
3000

Withdrawal Successful.

Current Balance : ₹2000
```

---

# How This Program Works

## Step 1

The balance is stored as a private variable.

```python
self.__balance
```

---

## Step 2

Python asks the user to enter a withdrawal amount.

---

## Step 3

The program enters the `try` block.

Python tries to convert the input into an integer.

---

## Step 4

If the amount is less than or equal to zero,

Python displays

```
Amount must be greater than zero.
```

---

## Step 5

If the amount is greater than the current balance,

Python displays

```
Insufficient Balance.
```

---

## Step 6

If the amount is valid,

Python subtracts it from the balance and displays

```
Withdrawal Successful.
```

---

## Step 7

If the user enters

```
abc
```

Python raises a `ValueError`.

Instead of stopping,

Python jumps to

```python
except ValueError
```

and prints

```
Please enter numbers only.
```

The program continues running normally.

---

# Difference Between Error and Exception

| Error | Exception |
|--------|-----------|
| Stops the program | Can be handled |
| Program crashes | Program continues |
| No control over the error | Can be controlled using `try` and `except` |

---

# Summary

- **Exception Handling** is used to handle errors while the program is running.
- The `try` block contains code that may cause an error.
- The `except` block handles the error.
- The `else` block runs only when there is no error.
- The `finally` block always runs, whether an error occurs or not.
- Exception Handling prevents the program from crashing and provides a better experience for the user.
- It is commonly used in banking systems, login systems, payment systems, file handling, APIs, and almost every real-world Python application.
