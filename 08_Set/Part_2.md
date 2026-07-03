# 🔧 Common Set Methods in Python

Python provides several built-in methods to work with sets. These methods help us add, remove, combine, and compare unique values.

---

# 1️⃣ add()

## 📖 What is add()?

The `add()` method adds a single new element to a set.

---

## 🌍 Real-World Example

A new student registers for a workshop.

We need to add the student's name to the registration list.

---

## 📝 Syntax

```python
set_name.add(value)
```

---

## 💻 Example

```python
students = {"Gokul", "Rahul", "Priya"}

students.add("Arun")

print(students)
```

### Output

```
{'Gokul', 'Rahul', 'Priya', 'Arun'}
```

---

# 2️⃣ update()

## 📖 What is update()?

The `update()` method adds multiple elements to a set.

---

## 🌍 Real-World Example

Two classes are participating in a workshop.

We combine both student groups into one registration list.

---

## 📝 Syntax

```python
set1.update(set2)
```

---

## 💻 Example

```python
class_a = {"Gokul", "Rahul"}
class_b = {"Priya", "Arun"}

class_a.update(class_b)

print(class_a)
```

### Output

```
{'Gokul', 'Rahul', 'Priya', 'Arun'}
```

---

# 3️⃣ remove()

## 📖 What is remove()?

The `remove()` method removes a specific element from a set.

If the value is not present, Python gives an error.

---

## 🌍 Real-World Example

A student cancels their workshop registration.

---

## 📝 Syntax

```python
set_name.remove(value)
```

---

## 💻 Example

```python
students = {"Gokul", "Rahul", "Priya"}

students.remove("Rahul")

print(students)
```

### Output

```
{'Gokul', 'Priya'}
```

---

# 4️⃣ discard()

## 📖 What is discard()?

The `discard()` method also removes an element.

The difference is that it **does not give an error** if the value is not present.

---

## 🌍 Real-World Example

Suppose you try to remove a student who has already left the workshop.

The program should continue without showing an error.

---

## 📝 Syntax

```python
set_name.discard(value)
```

---

## 💻 Example

```python
students = {"Gokul", "Rahul", "Priya"}

students.discard("Arun")

print(students)
```

### Output

```
{'Gokul', 'Rahul', 'Priya'}
```

---

# 5️⃣ pop()

## 📖 What is pop()?

The `pop()` method removes a random element from the set.

Since sets are unordered, you cannot predict which element will be removed.

---

## 🌍 Real-World Example

Suppose one random participant wins a lucky draw and is removed from the waiting list.

---

## 📝 Syntax

```python
set_name.pop()
```

---

## 💻 Example

```python
students = {"Gokul", "Rahul", "Priya"}

students.pop()

print(students)
```

### Sample Output

```
{'Rahul', 'Priya'}
```

**Note:** The removed element may be different each time.

---

# 6️⃣ clear()

## 📖 What is clear()?

The `clear()` method removes all elements from a set.

---

## 🌍 Real-World Example

After the workshop is completed, the registration list is cleared for the next event.

---

## 📝 Syntax

```python
set_name.clear()
```

---

## 💻 Example

```python
students = {"Gokul", "Rahul", "Priya"}

students.clear()

print(students)
```

### Output

```
set()
```

---

# 7️⃣ copy()

## 📖 What is copy()?

The `copy()` method creates a duplicate copy of a set.

---

## 🌍 Real-World Example

Before updating student records, the school creates a backup copy.

---

## 📝 Syntax

```python
new_set = old_set.copy()
```

---

## 💻 Example

```python
students = {"Gokul", "Rahul", "Priya"}

backup = students.copy()

print(backup)
```

### Output

```
{'Gokul', 'Rahul', 'Priya'}
```

---

# 8️⃣ union()

## 📖 What is union()?

The `union()` method combines two sets and removes duplicate values.

---

## 🌍 Real-World Example

Two colleges combine their participant lists for a hackathon.

---

## 📝 Syntax

```python
set1.union(set2)
```

---

## 💻 Example

```python
college_a = {"Gokul", "Rahul"}
college_b = {"Rahul", "Priya"}

print(college_a.union(college_b))
```

### Output

```
{'Gokul', 'Rahul', 'Priya'}
```

---

# 9️⃣ intersection()

## 📖 What is intersection()?

The `intersection()` method returns only the common elements between two sets.

---

## 🌍 Real-World Example

Find students who are members of both the Coding Club and the AI Club.

---

## 📝 Syntax

```python
set1.intersection(set2)
```

---

## 💻 Example

```python
coding_club = {"Gokul", "Rahul", "Priya"}
ai_club = {"Rahul", "Arun"}

print(coding_club.intersection(ai_club))
```

### Output

```
{'Rahul'}
```

---

# 🔟 difference()

## 📖 What is difference()?

The `difference()` method returns the elements that are present in the first set but not in the second set.

---

## 🌍 Real-World Example

Find students who are only in the Coding Club.

---

## 📝 Syntax

```python
set1.difference(set2)
```

---

## 💻 Example

```python
coding_club = {"Gokul", "Rahul", "Priya"}
ai_club = {"Rahul", "Arun"}

print(coding_club.difference(ai_club))
```

### Output

```
{'Gokul', 'Priya'}
```

---

# 1️⃣1️⃣ symmetric_difference()

## 📖 What is symmetric_difference()?

The `symmetric_difference()` method returns elements that are present in either set, but **not in both**.

---

## 🌍 Real-World Example

Find students who belong to only one club.

---

## 📝 Syntax

```python
set1.symmetric_difference(set2)
```

---

## 💻 Example

```python
coding_club = {"Gokul", "Rahul", "Priya"}
ai_club = {"Rahul", "Arun"}

print(coding_club.symmetric_difference(ai_club))
```

### Output

```
{'Gokul', 'Priya', 'Arun'}
```

---

# 📊 Quick Reference Table

| Method | Purpose |
|---------|---------|
| `add()` | Add one element |
| `update()` | Add multiple elements |
| `remove()` | Remove an element (gives error if not found) |
| `discard()` | Remove an element (no error if not found) |
| `pop()` | Remove a random element |
| `clear()` | Remove all elements |
| `copy()` | Create a duplicate set |
| `union()` | Combine two sets |
| `intersection()` | Find common elements |
| `difference()` | Find different elements |
| `symmetric_difference()` | Find elements present in only one set |

---

# 📌 Key Points

- `add()` adds one element.
- `update()` adds multiple elements.
- `remove()` gives an error if the value is not present.
- `discard()` does not give an error if the value is not present.
- `pop()` removes a random element.
- `clear()` removes all elements.
- `union()` combines two sets.
- `intersection()` finds common values.
- `difference()` finds values that are unique to the first set.
- `symmetric_difference()` finds values that are unique to either set.
