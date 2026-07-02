# 🐍 If Statement

## 📖 What is an If Statement?
- An if statement lets a program make a decision. It runs a block of code only when a certain condition is true.

---

## 🌍 Real-World Example
- Think about crossing the road. If the traffic light is red, you stop. If it's not red, you don't stop.
- In Python, `if` checks a condition and runs code only when that condition is true.

---

## ❓ Why Do We Need It?
- Programs need to make decisions based on different situations, just like humans do in daily life.
- Without `if`, every program would run the same way every time, with no flexibility.
- Real-world software uses `if` for login checks, discount rules, age verification, and much more.

---

## 📝 Syntax

```python
if condition:
    # code to run if condition is True
```

---

## 💻 Example 1

```python
age = 20

if age >= 18:
    print("You are eligible to vote.")
```

### Output

```text
You are eligible to vote.
```

---

## 💻 Example 2

```python
temperature = 40

if temperature > 35:
    print("It's a hot day, drink plenty of water!")
```

### Output

```text
It's a hot day, drink plenty of water!
```

---

## 💻 Example Using User Input

```python
marks = int(input("Enter your marks: "))

if marks >= 90:
    print("Excellent! You scored a distinction.")
```

### Sample Input

```text
95
```

### Output

```text
Excellent! You scored a distinction.
```

---

## 🌍 Real-World Applications

* Checking if a user is old enough to register on a website.
* Applying a discount if the cart total is above a certain amount.
* Showing a warning message if the battery level is low.
* Allowing login only if the password matches.
* Sending an alert if the temperature crosses a safety limit.

---

## 📌 Important Points

* The condition inside `if` must return `True` or `False`.
* Indentation (spacing) is very important in Python; the code inside `if` must be indented.
* You can use comparison and logical operators inside the condition.
* If the condition is `False`, the code inside `if` simply does not run.
* `if` is often combined with `else` and `elif` for more choices (covered in the next topics).

---

## ⚠️ Common Mistakes

### Mistake 1

❌ Wrong

```python
if age >= 18
    print("Eligible to vote")
```

✅ Correct

```python
if age >= 18:
    print("Eligible to vote")
```

---

### Mistake 2

❌ Wrong

```python
if age >= 18:
print("Eligible to vote")   # Missing indentation
```

✅ Correct

```python
if age >= 18:
    print("Eligible to vote")
```

---

## 🎯 Interview Questions

### Question 1
**Q: What is the purpose of an if statement?**
It allows a program to execute a block of code only when a specific condition is true, enabling decision-making.

---

### Question 2
**Q: Why is indentation important in Python if statements?**
Python uses indentation to define which code belongs inside the `if` block. Incorrect indentation causes errors or wrong behavior.

---

### Question 3
**Q: What happens if the condition in an if statement is False?**
The code block inside the `if` statement is simply skipped, and the program continues with the next line after it.

---

## 🧪 Practice Problem

Write a program that asks the user to enter their bank account balance, and if the balance is below ₹1000, print a message warning them about low balance.

---

## 📚 Summary

* An `if` statement runs code only when a condition is true.
* The condition must evaluate to `True` or `False`.
* Indentation defines what code belongs inside the `if` block.
* If the condition is `False`, the block is skipped entirely.
* `if` statements are the foundation of decision-making in Python.
* They are widely used in real-world applications for validations and rules.
