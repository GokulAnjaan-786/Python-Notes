# 🐍 sys.argv in Python

---

# 📖 What is sys.argv?

`sys.argv` is used to receive values from the **command line** when running a Python program.

Instead of asking the user to enter values using `input()`, we can pass the values while running the program.

To use `sys.argv`, we first need to import the **sys** module.

---

# 🌍 Real-World Example

Imagine you are ordering food using a mobile app.

Instead of the app asking you the same questions again and again, you directly select:

- Food Item
- Quantity
- Delivery Address

and place the order.

Similarly, with `sys.argv`, we directly pass values while running the program.

The program receives those values immediately.

---

# ❓ Why Do We Need sys.argv?

We use `sys.argv` when:

- We want to pass values while running the program.
- We do not want to use `input()`.
- We are running programs from the terminal or command prompt.
- We want to automate tasks.

---

# 📝 Syntax

```python
import sys

print(sys.argv)
```

---

# 📌 Understanding sys.argv

Suppose the file name is:

```
program.py
```

You run the program like this:

```bash
python program.py Gokul
```

Python stores the values like this:

| Index | Value |
|-------|--------|
| 0 | program.py |
| 1 | Gokul |

Notice that the file name is always stored at index **0**.

The first value entered by the user starts from index **1**.

---

# 💻 Example 1 – Display Name

### Python Program

```python
import sys

print("File Name:", sys.argv[0])
print("Name:", sys.argv[1])
```

### Run the Program

```bash
python program.py Gokul
```

### Output

```
File Name: program.py
Name: Gokul
```

---

# 💻 Example 2 – Add Two Numbers

### Python Program

```python
import sys

num1 = int(sys.argv[1])
num2 = int(sys.argv[2])

total = num1 + num2

print("Total =", total)
```

### Run the Program

```bash
python program.py 10 20
```

### Output

```
Total = 30
```

---

# 💻 Example 3 – Student Details

### Python Program

```python
import sys

name = sys.argv[1]
department = sys.argv[2]

print("Student Name :", name)
print("Department   :", department)
```

### Run the Program

```bash
python program.py Gokul AIML
```

### Output

```
Student Name : Gokul
Department   : AIML
```

---

# 💻 Example 4 – Employee Salary

### Python Program

```python
import sys

name = sys.argv[1]
salary = int(sys.argv[2])

print("Employee :", name)
print("Salary   :", salary)
```

### Run the Program

```bash
python program.py Rahul 45000
```

### Output

```
Employee : Rahul
Salary   : 45000
```

---

# 🌍 Where is sys.argv Used?

`sys.argv` is commonly used in:

- 🤖 Automation Scripts
- 🔐 Cybersecurity Tools
- 🖥️ Command Line Applications
- 📂 File Processing Programs
- 📊 Data Analysis Scripts
- ☁️ Server Management Scripts
- 🛠️ DevOps Automation

---

# 📌 Difference Between input() and sys.argv

| input() | sys.argv |
|----------|----------|
| Takes input while the program is running. | Takes input while starting the program. |
| User enters values one by one. | All values are passed in one command. |
| Mainly used by beginners. | Commonly used in automation and command-line programs. |

### Example Using input()

```python
name = input("Enter Name: ")

print(name)
```

---

### Example Using sys.argv

```python
import sys

print(sys.argv[1])
```

Run:

```bash
python program.py Gokul
```

---

# 📌 Key Points

- `sys.argv` is available in the **sys** module.
- Always import the **sys** module before using `sys.argv`.
- `sys.argv` stores command-line values as a list.
- `sys.argv[0]` is always the Python file name.
- User values start from `sys.argv[1]`.
- All values received through `sys.argv` are strings.
- Convert numbers using `int()` or `float()` when required.
