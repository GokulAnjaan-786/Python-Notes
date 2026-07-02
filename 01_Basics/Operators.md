# 🐍 Operators

## 📖 What is an Operator?
- An operator is a special symbol that performs an action on values, like adding two numbers or comparing them.

---

## 🌍 Real-World Example
- Think of a calculator. When you press `+`, `-`, `*`, or `/`, the calculator performs that operation on the numbers you entered.
- Python operators work exactly the same way, but inside code.

---

## ❓ Why Do We Need It?
- Operators let us perform calculations, compare values, and make decisions in our programs.
- Without operators, we could not do math, check conditions, or combine data.
- Real-world software uses operators for billing calculations, discount logic, login checks, and much more.

---

## 📝 Syntax

```python
result = value1 operator value2
```

---

## 💻 Example 1

```python
# Arithmetic operators
a = 10
b = 3

print(a + b)   # Addition
print(a - b)   # Subtraction
print(a * b)   # Multiplication
print(a / b)   # Division
print(a % b)   # Modulus (remainder)
print(a ** b)  # Exponent (power)
```

### Output

```text
13
7
30
3.3333333333333335
1
1000
```

---

## 💻 Example 2

```python
# Comparison operators
x = 5
y = 8

print(x == y)   # Equal to
print(x != y)   # Not equal to
print(x > y)    # Greater than
print(x < y)    # Less than
```

### Output

```text
False
True
False
True
```

---

## 💻 Example Using User Input

```python
num1 = int(input("Enter first number: "))
num2 = int(input("Enter second number: "))
print("Sum:", num1 + num2)
print("Is num1 greater than num2?", num1 > num2)
```

### Sample Input

```text
15
7
```

### Output

```text
Sum: 22
Is num1 greater than num2? True
```

---

## 🌍 Real-World Applications

* Calculating total bill amount in a shopping cart using arithmetic operators.
* Checking login credentials using comparison operators (`==`).
* Applying discount logic using logical operators (`and`, `or`).
* Checking if a number is even or odd using the modulus operator (`%`).
* Comparing scores to decide pass or fail in an exam result system.

---

## 📌 Important Points

* Arithmetic operators: `+`, `-`, `*`, `/`, `%`, `**`, `//`.
* Comparison operators: `==`, `!=`, `>`, `<`, `>=`, `<=`.
* Logical operators: `and`, `or`, `not`.
* Assignment operators: `=`, `+=`, `-=`, `*=`, `/=`.
* `/` always gives a float result, while `//` gives an integer (floor) result.

---

## ⚠️ Common Mistakes

### Mistake 1

❌ Wrong

```python
if x = 5:      # Using = instead of == for comparison
    print("Equal")
```

✅ Correct

```python
if x == 5:
    print("Equal")
```

---

### Mistake 2

❌ Wrong

```python
print(10 / 3)    # Thinking this gives an integer result
```

✅ Correct

```python
print(10 // 3)   # Use floor division for a whole number result
```

---

## 🎯 Interview Questions

### Question 1
**Q: What is the difference between `/` and `//` in Python?**
`/` performs normal division and always returns a float, while `//` performs floor division and returns the whole number part only.

---

### Question 2
**Q: What is the difference between `=` and `==`?**
`=` is used to assign a value to a variable, while `==` is used to compare two values for equality.

---

### Question 3
**Q: What does the modulus operator `%` do?**
The modulus operator returns the remainder after dividing one number by another, for example `10 % 3` gives `1`.

---

## 🧪 Practice Problem

Write a program that takes two numbers from the user and prints whether the first number is greater than, less than, or equal to the second number.

---

## 📚 Summary

* Operators perform actions like math, comparison, and logic on values.
* Arithmetic operators handle basic math operations.
* Comparison operators compare two values and return `True` or `False`.
* Logical operators combine multiple conditions.
* `/` gives a float, `//` gives a floor (whole number) result.
* `=` assigns a value, `==` compares two values.
* Operators are essential for calculations and decision-making in programs.
