# 🐍 Variables

## 📖 What is a Variable?
- A variable is a name we give to a place in the computer's memory where we store a value.
- Think of it like a labeled box. You put something inside the box, and you can use the label to find it later.

---

## 🌍 Real-World Example
- Imagine you have a box labeled "Pocket Money". You keep ₹500 inside it.
- Whenever you want to know how much pocket money you have, you just check the box labeled "Pocket Money".
- In Python, `pocket_money = 500` does the same thing. `pocket_money` is the label, and `500` is the value inside.

---

## ❓ Why Do We Need It?
- Variables let us store data so we can use it again and again without typing it every time.
- They make our code readable, because we use meaningful names instead of raw numbers or text.
- Real-world software uses variables everywhere — storing usernames, prices, scores, settings, and much more.

---

## 📝 Syntax

```python
variable_name = value
```

---

## 💻 Example 1

```python
name = "Anjaan"
age = 20
print(name)
print(age)
```

### Output

```text
Anjaan
20
```

---

## 💻 Example 2

```python
# Reassigning a variable
score = 10
print(score)

score = 25
print(score)
```

### Output

```text
10
25
```

---

## 💻 Example Using User Input

```python
city = input("Enter your city name: ")
print("You live in", city)
```

### Sample Input

```text
Coimbatore
```

### Output

```text
You live in Coimbatore
```

---

## 🌍 Real-World Applications

* Storing user details like name, email, and age in a login system.
* Keeping track of a shopping cart total in an e-commerce app.
* Storing game scores that update as the player plays.
* Holding sensor readings in an IoT device.
* Storing configuration settings like screen brightness or volume level.

---

## 📌 Important Points

* A variable name cannot start with a number (e.g. `1name` is invalid).
* Variable names are case-sensitive (`Age` and `age` are different variables).
* You do not need to declare the type of a variable in Python; it is decided automatically.
* Use meaningful names like `total_price` instead of unclear names like `x`.
* You can change the value of a variable anytime; this is called reassignment.

---

## ⚠️ Common Mistakes

### Mistake 1

❌ Wrong

```python
1name = "Anjaan"
```

✅ Correct

```python
name1 = "Anjaan"
```

---

### Mistake 2

❌ Wrong

```python
my variable = 10
```

✅ Correct

```python
my_variable = 10
```

---

## 🎯 Interview Questions

### Question 1
**Q: What is a variable in Python?**
A variable is a name used to refer to a value stored in memory. It acts like a label attached to data so we can use and change that data easily.

---

### Question 2
**Q: Do we need to declare a data type while creating a variable in Python?**
No. Python is a dynamically typed language, which means it automatically figures out the data type based on the value assigned.

---

### Question 3
**Q: Can we change the value of a variable after creating it?**
Yes. Variables in Python are mutable in the sense that you can reassign a new value to them at any time using the `=` sign.

---

## 🧪 Practice Problem

Create a program that stores your name, favorite programming language, and years of learning experience in three separate variables, and then prints them in a single sentence like:
"My name is ___, I love coding in ___, and I have been learning for ___ years."

---

## 📚 Summary

* A variable is a name that stores a value in memory.
* Python does not require you to mention the data type while creating a variable.
* Variable names are case-sensitive.
* Variable names cannot start with a number or contain spaces.
* Variables can be reassigned to new values anytime.
* Use meaningful variable names for readable code.
* Variables are the foundation of almost every Python program.
