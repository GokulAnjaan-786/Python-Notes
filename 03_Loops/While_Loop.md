# 🐍 While Loop

## 📖 What is a While Loop?
- A while loop repeats a block of code again and again as long as a given condition remains true.

---

## 🌍 Real-World Example
- Think about filling a water bottle. You keep pouring water while the bottle is not full. The moment it becomes full, you stop pouring.
- A `while` loop works the same way — it keeps running while the condition is true, and stops when it becomes false.

---

## ❓ Why Do We Need It?
- Sometimes we don't know in advance how many times we need to repeat something; we only know the condition to stop.
- While loops are useful when repetition depends on a changing condition, not a fixed count.
- Real-world software uses while loops for things like retrying a failed connection or running a game until the player loses.

---

## 📝 Syntax

```python
while condition:
    # code to repeat while condition is True
```

---

## 💻 Example 1

```python
count = 1

while count <= 5:
    print(count)
    count = count + 1
```

### Output

```text
1
2
3
4
5
```

---

## 💻 Example 2

```python
number = 10

while number > 0:
    print(number)
    number = number - 2
```

### Output

```text
10
8
6
4
2
```

---

## 💻 Example Using User Input

```python
password = ""

while password != "python123":
    password = input("Enter the correct password: ")

print("Access granted!")
```

### Sample Input

```text
wrongpass
python123
```

### Output

```text
Access granted!
```

---

## 🌍 Real-World Applications

* Retrying a network connection until it succeeds.
* Running a game loop until the player runs out of lives.
* Validating user input until the correct format is entered.
* Withdrawing money from an ATM in a loop until balance is zero.
* Monitoring a sensor value until it reaches a safe threshold.

---

## 📌 Important Points

* The condition in a while loop is checked before each repetition.
* If the condition is false from the start, the loop body never runs.
* You must update the condition variable inside the loop, or it may run forever.
* A loop that never stops is called an "infinite loop" — usually a bug unless intentional.
* `while True:` combined with a `break` statement is a common pattern for controlled infinite loops.

---

## ⚠️ Common Mistakes

### Mistake 1

❌ Wrong

```python
count = 1
while count <= 5:
    print(count)
    # Forgot to update count, causing an infinite loop
```

✅ Correct

```python
count = 1
while count <= 5:
    print(count)
    count = count + 1
```

---

### Mistake 2

❌ Wrong

```python
while count <= 5
    print(count)
```

✅ Correct

```python
while count <= 5:
    print(count)
```

---

## 🎯 Interview Questions

### Question 1
**Q: What is the main difference between a for loop and a while loop?**
A for loop is typically used when the number of repetitions is known in advance, while a while loop is used when repetition depends on a condition that may not have a fixed count.

---

### Question 2
**Q: What is an infinite loop, and how can it happen accidentally?**
An infinite loop is a loop that never stops running. It can happen accidentally if the condition variable is never updated inside the loop body.

---

### Question 3
**Q: What does `while True:` mean in Python?**
`while True:` creates a loop that always runs, since the condition is always true. It is usually combined with a `break` statement to stop it under a specific condition.

---

## 🧪 Practice Problem

Write a program using a while loop that keeps asking the user to enter a number until they enter 0, and prints "Goodbye!" once they do.

---

## 📚 Summary

* A while loop repeats code as long as a condition remains true.
* The condition is checked before every repetition of the loop.
* Forgetting to update the condition variable can cause an infinite loop.
* While loops are useful when the number of repetitions is unknown in advance.
* `while True:` with `break` is a common pattern for controlled loops.
* Widely used in real-time systems, retries, and validation checks.
