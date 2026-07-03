# 🌍 Real-World Project 1 – Student Management System

## 📖 Problem Statement

Suppose a college wants to store the details of a student.

The details include:

- Name
- Age
- Department
- CGPA

A dictionary is the best choice because each piece of information has a unique key.

---

## 💻 Python Program

```python
student = {
    "Name": "Gokul",
    "Age": 20,
    "Department": "AIML",
    "CGPA": 8.65
}

for key, value in student.items():
    print(key, ":", value)
```

### Output

```
Name : Gokul
Age : 20
Department : AIML
CGPA : 8.65
```

---

# 🌍 Real-World Project 2 – Employee Database

## 📖 Problem Statement

A company stores employee information.

Each employee has:

- Employee ID
- Name
- Department
- Salary

---

## 💻 Python Program

```python
employee = {
    "Employee ID": 101,
    "Name": "Rahul",
    "Department": "Developer",
    "Salary": 50000
}

for key, value in employee.items():
    print(key, ":", value)
```

### Output

```
Employee ID : 101
Name : Rahul
Department : Developer
Salary : 50000
```

---

# 🌍 Real-World Project 3 – Banking System

## 📖 Problem Statement

A bank stores customer account details.

Each account contains:

- Account Number
- Account Holder
- Balance

---

## 💻 Python Program

```python
account = {
    "Account Number": 123456789,
    "Account Holder": "Gokul",
    "Balance": 25000
}

print("Account Holder :", account["Account Holder"])
print("Available Balance : ₹", account["Balance"])
```

### Output

```
Account Holder : Gokul
Available Balance : ₹ 25000
```

---

# 🌍 Real-World Project 4 – Hospital Patient Record

## 📖 Problem Statement

A hospital stores patient details.

The details include:

- Patient ID
- Name
- Blood Group
- Disease

---

## 💻 Python Program

```python
patient = {
    "Patient ID": 5001,
    "Name": "Priya",
    "Blood Group": "O+",
    "Disease": "Fever"
}

for key, value in patient.items():
    print(key, ":", value)
```

### Output

```
Patient ID : 5001
Name : Priya
Blood Group : O+
Disease : Fever
```

---

# 🌍 Real-World Project 5 – Product Inventory System

## 📖 Problem Statement

An online shopping website stores product details.

Each product contains:

- Product ID
- Product Name
- Price
- Stock

---

## 💻 Python Program

```python
product = {
    "Product ID": 101,
    "Product Name": "Laptop",
    "Price": 65000,
    "Stock": 25
}

for key, value in product.items():
    print(key, ":", value)
```

### Output

```
Product ID : 101
Product Name : Laptop
Price : 65000
Stock : 25
```

---

# 🌍 Real-World Project 6 – Cybersecurity User Login System

## 📖 Problem Statement

A login system stores usernames and passwords.

The username acts as the key.

The password acts as the value.

---

## 💻 Python Program

```python
users = {
    "gokul": "Python@123",
    "rahul": "Java@456",
    "priya": "AI@789"
}

username = input("Enter Username: ")
password = input("Enter Password: ")

if username in users and users[username] == password:
    print("Login Successful")
else:
    print("Invalid Username or Password")
```

### Sample Input

```
Enter Username: gokul
Enter Password: Python@123
```

### Output

```
Login Successful
```

---

# 🌍 Real-World Project 7 – Student Marks System

## 📖 Problem Statement

A teacher stores student marks.

The student's name is the key.

The marks are the value.

---

## 💻 Python Program

```python
marks = {
    "Gokul": 95,
    "Rahul": 87,
    "Priya": 91
}

student = input("Enter Student Name: ")

if student in marks:
    print("Marks:", marks[student])
else:
    print("Student Not Found")
```

### Sample Input

```
Enter Student Name: Priya
```

### Output

```
Marks: 91
```

---

# 🌍 Where Are Dictionaries Used?

Dictionaries are commonly used in:

- 🎓 Student Management Systems
- 👨‍💼 Employee Databases
- 🏦 Banking Applications
- 🏥 Hospital Management Systems
- 🛒 Online Shopping Websites
- 📱 Mobile Applications
- 🌐 Websites
- 🔐 User Login Systems
- 🤖 Artificial Intelligence Projects
- 📊 Data Analysis

---

# 💡 When Should You Use a Dictionary?

Use a Dictionary when:

- Every value has a unique name (key).
- You want to access data using a key instead of an index.
- You need to update values easily.
- You want to store related information together.

### Examples

- Student Details
- Employee Records
- Bank Account Information
- Product Details
- Patient Records
- User Login Information
