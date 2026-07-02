# 🐍 *args in Python

---

# 📖 What is *args?

`*args` is used when we do not know how many arguments will be passed to a function.

Instead of creating separate parameters, `*args` allows a function to accept any number of values.

All the values are stored as a **tuple**.

---

# 🌍 Real-World Example

Imagine you are organizing a birthday party.

Some days, **5 friends** come.

Some days, **10 friends** come.

Some days, **20 friends** come.

You don't know how many friends will come.

Similarly, in Python, when we don't know how many values will be passed to a function, we use `*args`.

---

# ❓ Why Do We Need *args?

We use `*args` when:

- We don't know how many values will be passed.
- We want one function to work with different numbers of inputs.
- We want to avoid creating many functions with different numbers of parameters.

---

# 📝 Syntax

```python
def function_name(*args):
    # Code
```

---

# 💻 Example 1 – Display Student Names

Suppose a teacher wants to display the names of students attending a workshop.

Some days there may be 3 students.

Some days there may be 8 students.

```python
def students(*args):
    print(args)

students("Gokul", "Rahul", "Arun")
```

### Output

```
('Gokul', 'Rahul', 'Arun')
```

Notice that all the values are stored inside a **tuple**.

---

# 💻 Example 2 – Print All Employee Names

```python
def employees(*args):

    for employee in args:
        print(employee)

employees("Ravi", "Kumar", "Priya", "Anu")
```

### Output

```
Ravi
Kumar
Priya
Anu
```

---

# 💻 Example 3 – Calculate Total Marks

Suppose a student has marks in different subjects.

Instead of fixing the number of subjects, we can use `*args`.

```python
def total_marks(*marks):

    total = sum(marks)

    print("Total Marks:", total)

total_marks(85, 90, 88)
```

### Output

```
Total Marks: 263
```

---

# 💻 Example 4 – Shopping Bill

Suppose a customer buys different products.

```python
def shopping_bill(*prices):

    total = sum(prices)

    print("Total Bill: ₹", total)

shopping_bill(500, 200, 150, 100)
```

### Output

```
Total Bill: ₹ 950
```

---

# 🌍 Where is *args Used?

`*args` is commonly used in:

- 🛒 Shopping Applications
- 🏦 Banking Applications
- 🎓 Student Management Systems
- 📊 Data Analysis
- 🤖 Artificial Intelligence Projects
- 🌐 Web Applications
- 🔐 Cybersecurity Tools

---

# 📌 Difference Between Normal Parameters and *args

| Normal Parameters | *args |
|-------------------|--------|
| Fixed number of values | Any number of values |
| Number of parameters must be known | Number of parameters is not required |
| Stores individual values | Stores all values as a tuple |

---

### Example

```python
def add(a, b):
    print(a + b)

add(10, 20)
```

Here, the function accepts only **2 values**.

---

```python
def add(*numbers):
    print(sum(numbers))

add(10, 20)
add(10, 20, 30)
add(10, 20, 30, 40)
```

### Output

```
30
60
100
```

The same function works for any number of values.

---

# 📌 Key Points

- `*args` allows a function to accept multiple values.
- The values are stored as a tuple.
- You can give any name after `*`, but `args` is the standard name.
- `*args` makes functions more flexible.
- It is useful when the number of inputs is unknown.
