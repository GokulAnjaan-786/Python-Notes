# 🐍 If Else Statement

## 📖 What is an If Else Statement?
- An if-else statement lets a program choose between two paths: one path runs if the condition is true, and another path runs if it's false.

---

## 🌍 Real-World Example
- Think about an umbrella. If it's raining, you take an umbrella. Else (if it's not raining), you don't take one.
- In Python, `if-else` handles exactly this kind of two-choice decision.

---

## ❓ Why Do We Need It?
- Many real-life decisions have two outcomes: yes/no, pass/fail, allow/deny.
- Without `else`, we can only handle the "true" case, but not provide an alternative action.
- Real-world software uses `if-else` for things like login success/failure, payment approval/rejection, and more.

---

## 📝 Syntax

```python
if condition:
    # code if condition is True
else:
    # code if condition is False
```

---

## 💻 Example 1

```python
age = 15

if age >= 18:
    print("You are eligible to vote.")
else:
    print("You are not eligible to vote yet.")
```

### Output

```text
You are not eligible to vote yet.
```

---

## 💻 Example 2

```python
number = 7

if number % 2 == 0:
    print("Even number")
else:
    print("Odd number")
```

### Output

```text
Odd number
```

---

## 💻 Example Using User Input

```python
password = input("Enter password: ")

if password == "python123":
    print("Login successful!")
else:
    print("Incorrect password. Try again.")
```

### Sample Input

```text
wrongpass
```

### Output

```text
Incorrect password. Try again.
```

---

## 🌍 Real-World Applications

* Checking login credentials and showing success or failure messages.
* Deciding pass/fail status based on exam marks.
* Approving or declining a loan application based on eligibility.
* Showing "in stock" or "out of stock" messages in an online store.
* Sending "delivered" or "pending" status in a delivery tracking app.

---

## 📌 Important Points

* `else` does not need its own condition; it automatically runs when the `if` condition is false.
* Only one block, either `if` or `else`, will execute — never both.
* Both `if` and `else` blocks must be properly indented.
* `else` must always come after an `if` (or `elif`) block; it cannot be used alone.
* Combining `if-else` gives your program exactly two possible outcomes.

---

## ⚠️ Common Mistakes

### Mistake 1

❌ Wrong

```python
if age >= 18:
    print("Eligible")
else
    print("Not eligible")
```

✅ Correct

```python
if age >= 18:
    print("Eligible")
else:
    print("Not eligible")
```

---

### Mistake 2

❌ Wrong

```python
else:
    print("Not eligible")   # else used without if before it
```

✅ Correct

```python
if age >= 18:
    print("Eligible")
else:
    print("Not eligible")
```

---

## 🎯 Interview Questions

### Question 1
**Q: What is the purpose of the else block?**
The `else` block runs a set of code when the `if` condition is false, providing an alternative path for the program.

---

### Question 2
**Q: Can we use else without an if statement?**
No. `else` must always be paired with an `if` (or `elif`) statement; it cannot exist on its own.

---

### Question 3
**Q: Can both if and else blocks run at the same time?**
No. Only one of the two blocks will ever execute, depending on whether the condition is true or false.

---

## 🧪 Practice Problem

Write a program that asks the user to enter a number and checks whether it is positive or negative, printing an appropriate message using if-else.

---

## 📚 Summary

* `if-else` provides two possible paths: one for true, one for false.
* Only one block executes at a time, never both.
* `else` has no condition of its own.
* `else` must always follow an `if` or `elif` statement.
* It is widely used for two-outcome decisions like pass/fail or success/failure.
* Understanding `if-else` is essential before moving to more complex conditions like `elif`.
