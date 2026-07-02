# 🐍 Parameters in Python

---

# 📖 What are Parameters?

A **parameter** is a variable that is written inside the parentheses of a function.

Parameters allow a function to receive information when it is called.

Instead of using fixed values, we can pass different values to the same function.

---

# 🌍 Real-World Example

Imagine you order food online.

The delivery person always asks for your **delivery address**.

The delivery process is the same for every customer.

Only the address changes.

Similarly, a function performs the same task, but the values passed to it can be different.

These values are received through **parameters**.

---

# ❓ Why Do We Need Parameters?

Parameters help us to:

- Pass different values to the same function.
- Avoid creating many similar functions.
- Make functions reusable.
- Make programs flexible.

---

# 📝 Syntax

```python
def function_name(parameter1, parameter2):
    # Code
```

---

# 💻 Example 1 – Greeting Students

Suppose a school wants to greet every student by their name.

```python
def greet(name):
    print("Welcome", name)

greet("Gokul")
greet("Rahul")
greet("Priya")
```

### Output

```
Welcome Gokul
Welcome Rahul
Welcome Priya
```

---

# 💻 Example 2 – Employee Salary

Suppose a company wants to calculate the salary of different employees.

```python
def calculate_salary(basic_salary, bonus):
    total = basic_salary + bonus
    print("Total Salary:", total)

calculate_salary(30000, 5000)
calculate_salary(45000, 8000)
```

### Output

```
Total Salary: 35000
Total Salary: 53000
```

---

# 💻 Example 3 – Student Result

Suppose a school wants to check whether students have passed.

```python
def result(name, mark):
    print("Student Name:", name)

    if mark >= 35:
        print("Result: Pass")
    else:
        print("Result: Fail")

result("Gokul", 82)
result("Rahul", 24)
```

### Output

```
Student Name: Gokul
Result: Pass

Student Name: Rahul
Result: Fail
```

---

# 💻 Example 4 – Shopping Bill

Suppose an online shopping website wants to calculate the total bill.

```python
def calculate_bill(price, quantity):
    total = price * quantity
    print("Total Bill: ₹", total)

calculate_bill(500, 3)
calculate_bill(250, 5)
```

### Output

```
Total Bill: ₹ 1500
Total Bill: ₹ 1250
```

---

# 🌍 Where are Parameters Used?

Parameters are used in:

- 🏦 Banking Applications
- 🛒 Shopping Websites
- 🎓 College Management Systems
- 🏥 Hospital Management Systems
- 📱 Mobile Applications
- 🌐 Websites
- 🤖 AI Applications
- 🔐 Cybersecurity Tools

---

# 📌 Difference Between Parameter and Argument

| Parameter | Argument |
|-----------|----------|
| A variable written in the function definition. | The actual value passed while calling the function. |
| Receives data. | Sends data to the function. |

### Example

```python
def greet(name):
    print("Welcome", name)

greet("Gokul")
```

Here,

- `name` is the **Parameter**
- `"Gokul"` is the **Argument**

---

# 📌 Key Points

- Parameters are variables inside a function definition.
- Parameters receive values from the function call.
- One function can have one or more parameters.
- Parameters make functions reusable.
- Different values can be passed every time the function is called.
