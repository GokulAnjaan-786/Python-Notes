# 🌍 Real-World Project 1 – Student Registration System

## 📖 Problem Statement

Suppose a college is conducting a Python workshop.

Many students accidentally register more than once.

The college wants only one registration for each student.

A **Set** is the best choice because it automatically removes duplicate names.

---

## 💻 Python Program

```python
students = {
    "Gokul",
    "Rahul",
    "Priya",
    "Gokul",
    "Arun",
    "Rahul"
}

print("Registered Students:")

for student in students:
    print(student)
```

### Sample Output

```
Registered Students:
Gokul
Rahul
Priya
Arun
```

Notice that duplicate names are removed automatically.

---

# 🌍 Real-World Project 2 – Website Unique Visitors

## 📖 Problem Statement

A website wants to know how many unique visitors visited today.

The same person may visit many times.

The website should count only unique visitors.

---

## 💻 Python Program

```python
visitors = {
    "192.168.1.10",
    "192.168.1.15",
    "192.168.1.10",
    "192.168.1.25"
}

print("Unique Visitors:", len(visitors))
```

### Output

```
Unique Visitors: 3
```

---

# 🌍 Real-World Project 3 – Email Subscriber List

## 📖 Problem Statement

A company is collecting email addresses.

Some customers subscribe multiple times.

Duplicate email addresses should not be stored.

---

## 💻 Python Program

```python
emails = {
    "gokul@gmail.com",
    "rahul@gmail.com",
    "gokul@gmail.com",
    "priya@gmail.com"
}

print(emails)
```

### Sample Output

```
{
'gokul@gmail.com',
'rahul@gmail.com',
'priya@gmail.com'
}
```

---

# 🌍 Real-World Project 4 – Cybersecurity Blacklisted IP Addresses

## 📖 Problem Statement

A firewall stores blacklisted IP addresses.

If the same IP address is blocked again, it should not be stored twice.

---

## 💻 Python Program

```python
blacklist = {
    "192.168.1.5",
    "192.168.1.10",
    "192.168.1.5",
    "192.168.1.25"
}

print("Blocked IP Addresses:")

for ip in blacklist:
    print(ip)
```

### Sample Output

```
Blocked IP Addresses:

192.168.1.5
192.168.1.10
192.168.1.25
```

---

# 🌍 Real-World Project 5 – Shopping Categories

## 📖 Problem Statement

An online shopping website stores product categories.

Duplicate categories should not appear.

---

## 💻 Python Program

```python
categories = {
    "Electronics",
    "Books",
    "Clothing",
    "Electronics",
    "Shoes"
}

print(categories)
```

### Sample Output

```
{
'Electronics',
'Books',
'Clothing',
'Shoes'
}
```

---

# 🌍 Real-World Project 6 – Blood Group Records

## 📖 Problem Statement

A hospital wants to know which blood groups are available.

Duplicate blood groups are not required.

---

## 💻 Python Program

```python
blood_groups = {
    "A+",
    "B+",
    "O+",
    "A+",
    "AB+"
}

print("Available Blood Groups:")

for group in blood_groups:
    print(group)
```

### Sample Output

```
Available Blood Groups:

A+
B+
O+
AB+
```

---

# 🌍 Real-World Project 7 – College Club Members

## 📖 Problem Statement

Find students who are members of both the Coding Club and the AI Club.

---

## 💻 Python Program

```python
coding_club = {
    "Gokul",
    "Rahul",
    "Priya"
}

ai_club = {
    "Rahul",
    "Arun",
    "Priya"
}

common_students = coding_club.intersection(ai_club)

print(common_students)
```

### Output

```
{'Rahul', 'Priya'}
```

---

# 🌍 Where Are Sets Used?

Sets are commonly used in:

- 🎓 Student Registration Systems
- 🌐 Website Visitor Tracking
- 📧 Email Subscription Systems
- 🔐 Cybersecurity Applications
- 🏥 Hospital Management Systems
- 🛒 Online Shopping Websites
- 📊 Data Analysis
- 🤖 Artificial Intelligence Projects
- 🎮 Gaming Applications
- 📱 Mobile Applications

---

# 💡 When Should You Use a Set?

Use a Set when:

- You want only unique values.
- Duplicate values should be removed automatically.
- You want to compare two groups of data.
- You need fast searching.
- You need mathematical set operations such as Union and Intersection.

### Examples

- Student Registration Numbers
- Email Addresses
- Mobile Numbers
- Blacklisted IP Addresses
- Website Visitors
- Product Categories
