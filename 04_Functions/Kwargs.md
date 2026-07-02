# 🐍 **kwargs in Python

---

# 📖 What is **kwargs?

`**kwargs` is used when we do not know how many **key-value pairs** will be passed to a function.

Instead of accepting only fixed parameters, `**kwargs` allows a function to receive multiple named values.

All the values are stored as a **dictionary**.

---

# 🌍 Real-World Example

Imagine you are creating an **Employee Registration System**.

Some employees provide:

- Name
- Department
- Salary

Some employees also provide:

- Phone Number
- Email
- Address

Every employee may provide different details.

Instead of creating many parameters, we can use `**kwargs` to receive all the information.

---

# ❓ Why Do We Need **kwargs?

We use `**kwargs` when:

- We do not know how many details will be passed.
- We want to receive multiple key-value pairs.
- We want one function to work with different types of information.

---

# 📝 Syntax

```python
def function_name(**kwargs):
    # Code
```

---

# 💻 Example 1 – Display Student Details

```python
def student_details(**kwargs):
    print(kwargs)

student_details(
    name="Gokul",
    age=20,
    department="AIML"
)
```

### Output

```python
{
    'name': 'Gokul',
    'age': 20,
    'department': 'AIML'
}
```

Notice that all the values are stored inside a **dictionary**.

---

# 💻 Example 2 – Display Employee Details

```python
def employee_details(**kwargs):

    for key, value in kwargs.items():
        print(key, ":", value)

employee_details(
    name="Rahul",
    department="HR",
    salary=45000
)
```

### Output

```
name : Rahul
department : HR
salary : 45000
```

---

# 💻 Example 3 – Mobile Phone Details

```python
def mobile_details(**kwargs):

    for key, value in kwargs.items():
        print(key, ":", value)

mobile_details(
    brand="Samsung",
    model="S25",
    color="Black",
    price=75000
)
```

### Output

```
brand : Samsung
model : S25
color : Black
price : 75000
```

---

# 💻 Example 4 – Online Shopping Order

```python
def order_details(**kwargs):

    print("Order Details")

    for key, value in kwargs.items():
        print(key, ":", value)

order_details(
    customer="Gokul",
    product="Laptop",
    quantity=1,
    amount=65000
)
```

### Output

```
Order Details

customer : Gokul
product : Laptop
quantity : 1
amount : 65000
```

---

# 🌍 Where is **kwargs Used?

`**kwargs` is commonly used in:

- 🛒 Online Shopping Websites
- 🏦 Banking Applications
- 🎓 Student Management Systems
- 🏥 Hospital Management Systems
- 🌐 Web Applications
- 🤖 AI Applications
- 📊 Data Analysis Projects
- 🔐 Cybersecurity Tools

---

# 📌 Difference Between *args and **kwargs

| *args | **kwargs |
|--------|-----------|
| Accepts multiple values | Accepts multiple key-value pairs |
| Stores values as a tuple | Stores values as a dictionary |
| Used when values have no names | Used when values have names |

### Example

```python
def numbers(*args):
    print(args)

numbers(10, 20, 30)
```

### Output

```
(10, 20, 30)
```

---

```python
def student(**kwargs):
    print(kwargs)

student(name="Gokul", age=20)
```

### Output

```python
{'name': 'Gokul', 'age': 20}
```

---

# 📌 Key Points

- `**kwargs` accepts any number of key-value pairs.
- The values are stored as a dictionary.
- You can give any name after `**`, but `kwargs` is the standard name.
- `**kwargs` is useful when different users provide different information.
- It makes functions flexible and reusable.
