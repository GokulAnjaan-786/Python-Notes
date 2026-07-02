# 🐍 Continue

## 📖 What is Continue?
- `continue` is a statement used to skip the rest of the current loop iteration and move directly to the next one.

---

## 🌍 Real-World Example
- Think about checking attendance in class. If a student is absent, the teacher skips marking their performance for that day and moves on to the next student, without stopping the whole process.
- `continue` works the same way — it skips the current step and moves to the next one in the loop.

---

## ❓ Why Do We Need It?
- Sometimes we want to skip certain items in a loop without stopping the whole loop.
- `continue` lets us avoid unwanted cases while still processing the rest of the items.
- Real-world software uses `continue` to skip invalid data, skip blank entries, or skip already-processed items.

---

## 📝 Syntax

```python
for item in sequence:
    if condition:
        continue
    # rest of the loop code (skipped when continue runs)
```

---

## 💻 Example 1

```python
for i in range(1, 6):
    if i == 3:
        continue
    print(i)
```

### Output

```text
1
2
4
5
```

---

## 💻 Example 2

```python
numbers = [10, -5, 20, -8, 30]

for num in numbers:
    if num < 0:
        continue
    print("Positive number:", num)
```

### Output

```text
Positive number: 10
Positive number: 20
Positive number: 30
```

---

## 💻 Example Using User Input

```python
for i in range(1, 6):
    skip = input("Do you want to skip number " + str(i) + "? (yes/no): ")
    if skip == "yes":
        continue
    print("Processing number:", i)
```

### Sample Input

```text
no
yes
no
no
no
```

### Output

```text
Processing number: 1
Processing number: 3
Processing number: 4
Processing number: 5
```

---

## 🌍 Real-World Applications

* Skipping blank or invalid entries while processing a list of user data.
* Skipping already-processed orders in an order management system.
* Ignoring negative numbers while calculating the total of positive sales.
* Skipping weekends while calculating working days in a payroll system.
* Skipping duplicate entries while cleaning up a dataset.

---

## 📌 Important Points

* `continue` skips only the current iteration, not the entire loop.
* The loop continues running normally after skipping the current step.
* `continue` is often combined with `if` to define a skipping condition.
* Unlike `break`, `continue` does not stop the loop — it just moves to the next round.
* Using `continue` can make code cleaner by avoiding deeply nested if-else blocks.

---

## ⚠️ Common Mistakes

### Mistake 1

❌ Wrong

```python
for i in range(5):
    if i == 2:
    continue          # Wrong indentation
    print(i)
```

✅ Correct

```python
for i in range(5):
    if i == 2:
        continue
    print(i)
```

---

### Mistake 2

❌ Wrong

```python
for i in range(5):
    if i == 2:
        continue
        print(i)      # This line never runs because continue skips it
```

✅ Correct

```python
for i in range(5):
    if i == 2:
        continue
    print(i)          # Placed outside the if block, runs for all other values
```

---

## 🎯 Interview Questions

### Question 1
**Q: What does the continue statement do?**
The `continue` statement skips the remaining code in the current loop iteration and moves directly to the next iteration.

---

### Question 2
**Q: What is the difference between break and continue?**
`break` stops the loop completely, while `continue` only skips the current iteration and lets the loop keep running.

---

### Question 3
**Q: Give an example of when continue is useful.**
Continue is useful when processing a list of numbers and we want to skip negative numbers while still processing all the positive ones.

---

## 🧪 Practice Problem

Write a program that loops through numbers from 1 to 20 and prints only the numbers that are NOT divisible by 3, using `continue` to skip the ones that are.

---

## 📚 Summary

* `continue` skips the current iteration and moves to the next one.
* The loop does not stop; it simply moves forward.
* Commonly combined with `if` to define a skip condition.
* Different from `break`, which stops the loop entirely.
* Code placed after `continue` in the same iteration will not execute.
* Useful for skipping unwanted data while processing a collection.
