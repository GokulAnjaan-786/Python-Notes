# 🐍 Data Types

## 📖 What is a Data Type?
- A data type tells Python what kind of value is stored in a variable, like a number, text, or true/false value.

---

## 🌍 Real-World Example
- Think of a form you fill at a hospital. Some fields need your name (text), some need your age (number), and some need a yes/no answer (true/false).
- Each field expects a specific "type" of information. Python data types work the same way.

---

## ❓ Why Do We Need It?
- Data types help Python understand how to store and process data correctly.
- They prevent errors, like trying to add a number to a piece of text by mistake.
- Real-world software uses data types to validate form inputs, store database records, and perform correct calculations.

---

## 📝 Syntax

```python
variable_name = value   # Python decides the data type automatically
type(variable_name)     # Used to check the data type
```

---

## 💻 Example 1

```python
name = "Anjaan"        # str (text)
age = 20                # int (whole number)
height = 5.9            # float (decimal number)
is_student = True       # bool (True or False)

print(type(name))
print(type(age))
print(type(height))
print(type(is_student))
```

### Output

```text
<class 'str'>
<class 'int'>
<class 'float'>
<class 'bool'>
```

---

## 💻 Example 2

```python
# Type conversion
number_text = "100"
number = int(number_text)
print(number + 50)
```

### Output

```text
150
```

---

## 💻 Example Using User Input

```python
age = input("Enter your age: ")
age = int(age)
print("Next year you will be", age + 1)
```

### Sample Input

```text
19
```

### Output

```text
Next year you will be 20
```

---

## 🌍 Real-World Applications

* Storing prices as `float` in shopping websites.
* Storing usernames and messages as `str` in chat apps.
* Storing true/false flags like `is_logged_in` in login systems.
* Storing quantities like number of items as `int` in inventory systems.
* Storing a list of products as a `list` in an online store.

---

## 📌 Important Points

* Common basic data types: `int`, `float`, `str`, `bool`.
* Common collection data types: `list`, `tuple`, `dict`, `set`.
* Use `type()` to check the data type of any variable.
* Data from `input()` is always taken as `str`, even if the user types a number.
* You can convert between types using `int()`, `float()`, `str()`, `bool()`.

---

## ⚠️ Common Mistakes

### Mistake 1

❌ Wrong

```python
age = input("Enter age: ")
print(age + 5)   # Error: age is a string, not a number
```

✅ Correct

```python
age = int(input("Enter age: "))
print(age + 5)
```

---

### Mistake 2

❌ Wrong

```python
value = "10"
result = value * 2   # This repeats the string, not multiply the number
print(result)
```

✅ Correct

```python
value = int("10")
result = value * 2
print(result)
```

---

## 🎯 Interview Questions

### Question 1
**Q: What are the basic data types in Python?**
The basic data types in Python are `int` (whole numbers), `float` (decimal numbers), `str` (text), and `bool` (True or False).

---

### Question 2
**Q: Why does `input()` always return a string?**
Because Python treats all keyboard input as text by default. If we need a number, we must convert it manually using `int()` or `float()`.

---

### Question 3
**Q: What is type conversion in Python?**
Type conversion is changing a value from one data type to another, for example converting a string "10" into the integer 10 using `int()`.

---

## 🧪 Practice Problem

Write a program that asks the user for their weight in kilograms (as a number) and their name (as text), then prints a message showing both values along with their data types.

---

## 📚 Summary

* A data type defines what kind of value a variable holds.
* Common types: `int`, `float`, `str`, `bool`, `list`, `tuple`, `dict`, `set`.
* Use `type()` to check a variable's data type.
* `input()` always returns data as a string.
* Convert types using `int()`, `float()`, `str()`, `bool()`.
* Choosing the correct data type avoids bugs and errors in a program.
* Data types are the building blocks for storing information correctly.
