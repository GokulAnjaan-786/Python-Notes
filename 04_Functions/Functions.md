# 🐍 Functions in Python

---

# 📖 What is a Function?

A **function** is a block of code that performs a specific task.

Instead of writing the same code again and again, we write it once inside a function and use it whenever we need it.

Functions make programs **clean**, **easy to understand**, and **easy to reuse**.

---

# 🌍 Real-World Example

Imagine you have a **TV Remote**.

When you press the **Power** button, the TV turns on.

Every time you press the same button, it performs the same task.

You do not open the TV and connect wires every time.

Similarly, in Python, we create a function once and call it whenever we need that task.

---

# ❓ Why Do We Need Functions?

Functions help us to:

- Avoid writing the same code again and again.
- Make programs easy to read.
- Make programs easy to maintain.
- Divide a large program into smaller parts.
- Reuse the same code whenever needed.

---

# 📝 Syntax

```python
def function_name():
    # Code to execute
```

---

# 💻 Example 1 – Welcome Message

Suppose you are creating a learning application. Every time a user opens the application, you want to display a welcome message.

```python
def welcome():
    print("Welcome to Python Programming")

welcome()
```

### Output

```
Welcome to Python Programming
```

---

# 💻 Example 2 – Employee Salary Calculator

Imagine you are developing software for a company.

The company wants to calculate the total salary of an employee.

```python
def calculate_salary(basic_salary, bonus):
    total_salary = basic_salary + bonus
    print("Total Salary:", total_salary)

calculate_salary(30000, 5000)
```

### Output

```
Total Salary: 35000
```

---

# 💻 Example 3 – Student Result System

Suppose a school wants to automatically check whether a student has passed or failed.

```python
def check_result(mark):
    if mark >= 35:
        print("Result: Pass")
    else:
        print("Result: Fail")

check_result(82)
```

### Output

```
Result: Pass
```

---

# 💻 Example 4 – Shopping Bill

Suppose you are developing an online shopping application.

```python
def calculate_bill(price, quantity):
    total = price * quantity
    print("Total Bill: ₹", total)

calculate_bill(250, 4)
```

### Output

```
Total Bill: ₹ 1000
```

---

# 🌍 Where Are Functions Used?

Functions are used in almost every software application.

Some examples are:

- 🏦 Banking Applications
- 🛒 Online Shopping Websites
- 🏥 Hospital Management Systems
- 🎓 College Management Systems
- 📱 Mobile Applications
- 🤖 Artificial Intelligence Projects
- 🔐 Cybersecurity Tools
- 🎮 Games
- 🌐 Websites
- 📊 Data Analysis Projects

---

# 📌 Key Points

- A function is a block of code that performs a specific task.
- Functions are created using the `def` keyword.
- A function runs only when it is called.
- A function can be called multiple times.
- Functions reduce repeated code.
- Functions make programs clean and organized.
- Large programs are divided into smaller functions.
