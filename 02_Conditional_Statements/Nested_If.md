# 🐍 Nested If

## 📖 What is a Nested If?
- A nested if is an `if` statement placed inside another `if` (or `else`) statement. It lets us check a condition only after another condition is already true.

---

## 🌍 Real-World Example
- Think about entering a movie theater. First, you check if you have a ticket. If yes, then you check if you are old enough for the movie's age rating.
- The second check only happens after the first one is passed — that's exactly how nested if works.

---

## ❓ Why Do We Need It?
- Some real-life decisions depend on more than one condition, checked in stages.
- Nested if lets us build detailed decision trees where later checks depend on earlier results.
- Real-world software uses nested if for multi-step validations like login + permission checks, or age + ticket type checks.

---

## 📝 Syntax

```python
if condition1:
    if condition2:
        # code if both condition1 and condition2 are True
```

---

## 💻 Example 1

```python
age = 25
has_ticket = True

if has_ticket:
    if age >= 18:
        print("Welcome, enjoy the movie!")
    else:
        print("Sorry, you are too young for this movie.")
else:
    print("Please buy a ticket first.")
```

### Output

```text
Welcome, enjoy the movie!
```

---

## 💻 Example 2

```python
number = 15

if number > 0:
    if number % 2 == 0:
        print("Positive even number")
    else:
        print("Positive odd number")
else:
    print("Negative number")
```

### Output

```text
Positive odd number
```

---

## 💻 Example Using User Input

```python
username = input("Enter username: ")
password = input("Enter password: ")

if username == "admin":
    if password == "admin123":
        print("Login successful!")
    else:
        print("Incorrect password.")
else:
    print("Username not found.")
```

### Sample Input

```text
admin
wrongpass
```

### Output

```text
Incorrect password.
```

---

## 🌍 Real-World Applications

* Two-step login systems that check username first, then password.
* Ticket booking systems that check ticket availability and then age restrictions.
* Bank withdrawal systems that check account status and then balance.
* Online exam portals that check login and then check if the exam time is active.
* E-commerce sites that check stock availability and then check payment success.

---

## 📌 Important Points

* Nested if means an if statement written inside another if or else block.
* Each level of nesting must be indented one step further than the previous.
* Too much nesting can make code hard to read; try to keep it simple.
* Nested if is useful when a decision truly depends on multiple stages of checking.
* You can combine nested if with elif for even more detailed decision-making.

---

## ⚠️ Common Mistakes

### Mistake 1

❌ Wrong

```python
if has_ticket:
if age >= 18:            # Missing proper indentation
    print("Welcome")
```

✅ Correct

```python
if has_ticket:
    if age >= 18:
        print("Welcome")
```

---

### Mistake 2

❌ Wrong

```python
if age >= 18 and has_ticket:
    if True:              # Unnecessary nesting, condition already combined
        print("Welcome")
```

✅ Correct

```python
if age >= 18 and has_ticket:
    print("Welcome")
```

---

## 🎯 Interview Questions

### Question 1
**Q: What is a nested if statement?**
A nested if is an if statement placed inside another if or else block, used to check a second condition only after the first one is satisfied.

---

### Question 2
**Q: When should we use nested if instead of the `and` operator?**
Nested if is preferred when we need to perform different actions based on the outer condition (like showing different messages), while `and` is used when we only need a single combined true/false check.

---

### Question 3
**Q: What is a disadvantage of using too much nested if?**
Too many nested if statements make the code harder to read and maintain; it's often better to simplify logic using `elif` or logical operators.

---

## 🧪 Practice Problem

Write a program that asks the user to enter their age and whether they have a valid ID (yes/no). Use nested if statements to check if they are allowed to enter a nightclub (must be 18+ and have a valid ID).

---

## 📚 Summary

* A nested if is an if statement written inside another if or else block.
* It allows checking a second condition only after the first is true.
* Proper indentation is very important in nested if statements.
* Useful for multi-stage decisions like login and permission checks.
* Avoid excessive nesting to keep code readable.
* Can be combined with elif and logical operators for cleaner logic.
