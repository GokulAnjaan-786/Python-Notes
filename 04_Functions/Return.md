# 🐍 Return Statement in Python

---

# 📖 What is a Return Statement?

The **return** statement is used to send a value back from a function.

When a function finishes its work, it can return the result to the place where it was called.

Unlike `print()`, the `return` statement allows us to store the result in a variable and use it later.

---

# 🌍 Real-World Example

Imagine you withdraw money from an ATM.

You request ₹5,000.

The ATM processes your request and gives you the money.

Similarly, a function processes the input and **returns** the result.

---

# ❓ Why Do We Need Return?

The `return` statement helps us to:

- Send a result back from a function.
- Store the returned value in a variable.
- Use the result later in the program.
- Avoid calculating the same thing again.

---

# 📝 Syntax

```python
def function_name():
    return value
```

---

# 💻 Example 1 – Add Two Numbers

Suppose you want to add two numbers and use the answer later.

```python
def add(a, b):
    return a + b

result = add(10, 20)

print(result)
```

### Output

```
30
```

---

# 💻 Example 2 – Employee Salary Calculator

Suppose a company wants to calculate an employee's salary.

```python
def calculate_salary(basic_salary, bonus):
    total_salary = basic_salary + bonus
    return total_salary

salary = calculate_salary(35000, 5000)

print("Total Salary:", salary)
```

### Output

```
Total Salary: 40000
```

---

# 💻 Example 3 – Student Result

Suppose a school wants to check whether a student has passed.

```python
def check_result(mark):

    if mark >= 35:
        return "Pass"

    return "Fail"

result = check_result(80)

print(result)
```

### Output

```
Pass
```

---

# 💻 Example 4 – Online Shopping Discount

Suppose an online shopping website gives a ₹500 discount.

```python
def final_price(price):
    return price - 500

amount = final_price(5000)

print("Final Amount: ₹", amount)
```

### Output

```
Final Amount: ₹ 4500
```

---

# 📌 Difference Between print() and return

| print() | return |
|----------|---------|
| Displays the output on the screen. | Sends the value back from the function. |
| Cannot store the result. | The result can be stored in a variable. |
| Mainly used for displaying information. | Mainly used when another part of the program needs the result. |

---

### Example

```python
def add(a, b):
    print(a + b)

result = add(10, 20)

print(result)
```

### Output

```
30
None
```

Why?

The function printed the answer, but it did not return anything.

---

### Using return

```python
def add(a, b):
    return a + b

result = add(10, 20)

print(result)
```

### Output

```
30
```

---

# 🌍 Where is Return Used?

The `return` statement is used in:

- 🏦 Banking Applications
- 🛒 Online Shopping Websites
- 📱 Mobile Applications
- 🌐 Websites
- 🤖 Artificial Intelligence Projects
- 🎓 Student Management Systems
- 🏥 Hospital Management Systems
- 🔐 Cybersecurity Tools

---

# 📌 Key Points

- The `return` statement sends a value back from a function.
- A function can return numbers, strings, lists, dictionaries, and many other data types.
- The returned value can be stored in a variable.
- `return` ends the execution of the function immediately.
- Use `return` when another part of the program needs the result.
