# 🐍 For Loop

## 📖 What is a For Loop?
- A for loop is used to repeat a block of code a fixed number of times or for each item in a sequence, like a list or a range of numbers.

---

## 🌍 Real-World Example
- Think about a teacher calling out roll numbers one by one from a class list. She goes through each name, one at a time, until the list is finished.
- A `for` loop does exactly this — it goes through each item in a sequence, one by one.

---

## ❓ Why Do We Need It?
- Loops let us avoid writing the same code again and again for repeated tasks.
- They make it easy to process each item in a collection, like a list of students or products.
- Real-world software uses for loops to process orders, send bulk emails, and display lists of items.

---

## 📝 Syntax

```python
for item in sequence:
    # code to repeat for each item
```

---

## 💻 Example 1

```python
for i in range(5):
    print(i)
```

### Output

```text
0
1
2
3
4
```

---

## 💻 Example 2

```python
fruits = ["apple", "banana", "mango"]

for fruit in fruits:
    print("I like", fruit)
```

### Output

```text
I like apple
I like banana
I like mango
```

---

## 💻 Example Using User Input

```python
n = int(input("Enter a number: "))

for i in range(1, n + 1):
    print(i, "x 2 =", i * 2)
```

### Sample Input

```text
3
```

### Output

```text
1 x 2 = 2
2 x 2 = 4
3 x 2 = 6
```

---

## 🌍 Real-World Applications

* Sending a confirmation email to every customer in an order list.
* Displaying every product in a shopping website's catalog page.
* Calculating the total marks of a student by going through each subject's score.
* Printing a multiplication table for a given number.
* Processing every row in a spreadsheet or database table.

---

## 📌 Important Points

* `range(n)` generates numbers from `0` to `n-1`.
* `range(start, stop)` generates numbers from `start` to `stop-1`.
* `range(start, stop, step)` lets you skip numbers using the step value.
* A for loop can iterate over strings, lists, tuples, dictionaries, and sets.
* The loop variable (like `i` or `fruit`) takes a new value in each round of the loop.

---

## ⚠️ Common Mistakes

### Mistake 1

❌ Wrong

```python
for i in range(5)     # Missing colon
    print(i)
```

✅ Correct

```python
for i in range(5):
    print(i)
```

---

### Mistake 2

❌ Wrong

```python
for i in range(1, 5):
    print(i)
print("Total numbers printed: 5")   # Wrong assumption, range(1,5) prints only 4 numbers
```

✅ Correct

```python
for i in range(1, 6):
    print(i)
print("Total numbers printed: 5")
```

---

## 🎯 Interview Questions

### Question 1
**Q: What is the difference between range(5) and range(1, 5)?**
`range(5)` generates numbers from 0 to 4 (5 numbers), while `range(1, 5)` generates numbers from 1 to 4 (4 numbers), since the stop value is always excluded.

---

### Question 2
**Q: Can a for loop iterate over a string?**
Yes, a for loop can go through each character of a string one by one, since a string is a sequence of characters.

---

### Question 3
**Q: What is the use of the step value in range()?**
The step value determines how much to increase (or decrease) each number in the sequence, for example `range(0, 10, 2)` prints even numbers from 0 to 8.

---

## 🧪 Practice Problem

Write a program that takes a number from the user and prints its multiplication table from 1 to 10 using a for loop.

---

## 📚 Summary

* A for loop repeats a block of code for each item in a sequence.
* `range()` is commonly used to generate a sequence of numbers.
* For loops can iterate over lists, strings, tuples, dictionaries, and sets.
* The stop value in `range()` is always excluded from the sequence.
* Step values in `range()` allow skipping numbers.
* For loops are essential for processing collections of data efficiently.
