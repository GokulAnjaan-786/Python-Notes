# 🐍 Elif Statement

## 📖 What is an Elif Statement?
- `elif` stands for "else if". It lets us check multiple conditions one after another, instead of just two outcomes.

---

## 🌍 Real-World Example
- Think about grading a school exam. If marks are above 90, grade is A. Else if marks are above 75, grade is B. Else if marks are above 50, grade is C. Otherwise, grade is F.
- `elif` in Python allows this kind of multi-level checking.

---

## ❓ Why Do We Need It?
- Real-life decisions often have more than two outcomes, not just true/false.
- Without `elif`, we would need many separate `if` statements, which is messy and inefficient.
- Real-world software uses `elif` for grading systems, pricing tiers, traffic light logic, and much more.

---

## 📝 Syntax

```python
if condition1:
    # code if condition1 is True
elif condition2:
    # code if condition2 is True
elif condition3:
    # code if condition3 is True
else:
    # code if none of the above are True
```

---

## 💻 Example 1

```python
marks = 82

if marks >= 90:
    print("Grade: A")
elif marks >= 75:
    print("Grade: B")
elif marks >= 50:
    print("Grade: C")
else:
    print("Grade: F")
```

### Output

```text
Grade: B
```

---

## 💻 Example 2

```python
day = 3

if day == 1:
    print("Monday")
elif day == 2:
    print("Tuesday")
elif day == 3:
    print("Wednesday")
else:
    print("Invalid day number")
```

### Output

```text
Wednesday
```

---

## 💻 Example Using User Input

```python
temperature = int(input("Enter temperature in Celsius: "))

if temperature > 35:
    print("It's very hot!")
elif temperature > 20:
    print("It's pleasant weather.")
else:
    print("It's cold outside.")
```

### Sample Input

```text
25
```

### Output

```text
It's pleasant weather.
```

---

## 🌍 Real-World Applications

* Grading systems in schools and colleges (A, B, C, F).
* Pricing tiers based on subscription plans (Basic, Standard, Premium).
* Traffic light simulation (Red, Yellow, Green).
* Shipping cost calculation based on order weight ranges.
* Movie ticket pricing based on age groups (child, adult, senior citizen).

---

## 📌 Important Points

* `elif` is checked only if the previous `if` (or `elif`) condition was false.
* You can use as many `elif` blocks as needed.
* Python checks conditions from top to bottom and stops at the first true condition.
* `else` at the end is optional but useful for handling all remaining cases.
* Using `elif` is more efficient than writing multiple separate `if` statements.

---

## ⚠️ Common Mistakes

### Mistake 1

❌ Wrong

```python
if marks >= 90:
    print("Grade: A")
if marks >= 75:            # Using if instead of elif
    print("Grade: B")
```

✅ Correct

```python
if marks >= 90:
    print("Grade: A")
elif marks >= 75:
    print("Grade: B")
```

---

### Mistake 2

❌ Wrong

```python
if day == 1:
    print("Monday")
elif day = 2:              # Using = instead of ==
    print("Tuesday")
```

✅ Correct

```python
if day == 1:
    print("Monday")
elif day == 2:
    print("Tuesday")
```

---

## 🎯 Interview Questions

### Question 1
**Q: What is the purpose of elif in Python?**
`elif` allows checking multiple conditions in sequence, running the code block for the first condition that is true.

---

### Question 2
**Q: What is the difference between using multiple if statements and if-elif?**
Multiple `if` statements check every condition independently, even after one is true. `elif` stops checking further conditions once one is found true, making it more efficient.

---

### Question 3
**Q: Is else mandatory when using elif?**
No, `else` is optional. You can use `if-elif` without an `else`, but adding `else` helps handle any remaining unmatched cases.

---

## 🧪 Practice Problem

Write a program that takes a person's age as input and prints "Child" if age is below 13, "Teenager" if age is between 13 and 19, "Adult" if age is between 20 and 59, and "Senior Citizen" if age is 60 or above.

---

## 📚 Summary

* `elif` means "else if" and allows checking multiple conditions.
* Conditions are checked top to bottom, and the first true one runs.
* You can use multiple `elif` blocks in a single if-elif-else chain.
* `else` at the end catches all remaining cases.
* `elif` is more efficient than using several separate `if` statements.
* Widely used in grading systems, pricing logic, and multi-outcome decisions.
