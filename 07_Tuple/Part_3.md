---

# 🌍 Real-World Project 1 – Student Record System

## 📖 Problem Statement

Suppose a college wants to store the basic details of a student.

The details are:

- Register Number
- Student Name
- Department

These details usually do not change after admission.

So, a tuple is a good choice.

---

## 💻 Python Program

```python
student = (101, "Gokul", "AIML")

print("Register Number :", student[0])
print("Student Name    :", student[1])
print("Department      :", student[2])
```

### Output

```
Register Number : 101
Student Name    : Gokul
Department      : AIML
```

---

# 🌍 Real-World Project 2 – Employee Information System

## 📖 Problem Statement

A company stores employee details.

The Employee ID should never change.

So, a tuple is used.

---

## 💻 Python Program

```python
employee = (1001, "Rahul", "Developer", 50000)

print("Employee ID :", employee[0])
print("Name        :", employee[1])
print("Role        :", employee[2])
print("Salary      :", employee[3])
```

### Output

```
Employee ID : 1001
Name        : Rahul
Role        : Developer
Salary      : 50000
```

---

# 🌍 Real-World Project 3 – GPS Location

## 📖 Problem Statement

Google Maps stores locations using Latitude and Longitude.

These values usually remain fixed for a location.

---

## 💻 Python Program

```python
location = (11.0168, 76.9558)

print("Latitude  :", location[0])
print("Longitude :", location[1])
```

### Output

```
Latitude  : 11.0168
Longitude : 76.9558
```

---

# 🌍 Real-World Project 4 – RGB Color System

## 📖 Problem Statement

Every color on a computer screen is represented using RGB values.

Each color contains:

- Red
- Green
- Blue

These values remain fixed for that color.

---

## 💻 Python Program

```python
red = (255, 0, 0)

print("Red   :", red[0])
print("Green :", red[1])
print("Blue  :", red[2])
```

### Output

```
Red   : 255
Green : 0
Blue  : 0
```

---

# 🌍 Real-World Project 5 – Hospital Patient Record

## 📖 Problem Statement

A hospital stores basic patient information.

The Patient ID should never change.

---

## 💻 Python Program

```python
patient = (5001, "Priya", "O+")

print("Patient ID :", patient[0])
print("Name       :", patient[1])
print("Blood Group:", patient[2])
```

### Output

```
Patient ID : 5001
Name       : Priya
Blood Group: O+
```

---

# 🌍 Real-World Project 6 – Passport Details

## 📖 Problem Statement

Passport details remain fixed after they are issued.

A tuple is a good choice to store them.

---

## 💻 Python Program

```python
passport = (
    "N1234567",
    "Gokul",
    "India"
)

print("Passport Number :", passport[0])
print("Name            :", passport[1])
print("Country         :", passport[2])
```

### Output

```
Passport Number : N1234567
Name            : Gokul
Country         : India
```

---

# 🌍 Real-World Project 7 – Product Details

## 📖 Problem Statement

A product has a fixed Product ID.

The ID should not change.

---

## 💻 Python Program

```python
product = (
    101,
    "Laptop",
    65000
)

print("Product ID   :", product[0])
print("Product Name :", product[1])
print("Price        :", product[2])
```

### Output

```
Product ID   : 101
Product Name : Laptop
Price        : 65000
```

---

# 🌍 Where Are Tuples Used?

Tuples are commonly used in:

- 📍 GPS Coordinates
- 🌈 RGB Color Values
- 🛂 Passport Information
- 🪪 Aadhaar Information
- 🏥 Hospital Patient ID
- 🎓 Student Register Number
- 👨‍💼 Employee ID
- 📦 Product ID
- ✈️ Flight Number
- 🚆 Train Number

These values usually remain fixed, so tuples are the best choice.

---

# 💡 When Should You Use a Tuple?

Use a tuple when:

- The data should not change.
- The values are fixed.
- You want to protect important information.
- You want to prevent accidental updates.
- You want to group related values together.

For example:

- Date of Birth
- Passport Number
- Aadhaar Number
- GPS Coordinates
- RGB Color Values
