---

# 🔧 Common List Methods in Python

Python provides many built-in methods to work with lists. These methods help us add, remove, search, and arrange data easily.

---

# 1️⃣ append()

## 📖 What is append()?

The `append()` method adds a new element to the **end** of a list.

---

## 🌍 Real-World Example

Imagine a teacher wants to add a new student's name to the attendance list.

Instead of creating a new list, the teacher simply adds the student's name at the end.

---

## 📝 Syntax

```python
list_name.append(value)
```

---

## 💻 Example

```python
students = ["Gokul", "Rahul", "Priya"]

students.append("Arun")

print(students)
```

### Output

```
['Gokul', 'Rahul', 'Priya', 'Arun']
```

---

# 2️⃣ extend()

## 📖 What is extend()?

The `extend()` method adds all the elements of another list to the current list.

---

## 🌍 Real-World Example

Suppose two classes are going on a college tour.

Instead of creating a new attendance list, both class lists are combined into one.

---

## 📝 Syntax

```python
list1.extend(list2)
```

---

## 💻 Example

```python
class_a = ["Gokul", "Rahul"]
class_b = ["Priya", "Arun"]

class_a.extend(class_b)

print(class_a)
```

### Output

```
['Gokul', 'Rahul', 'Priya', 'Arun']
```

---

# 3️⃣ insert()

## 📖 What is insert()?

The `insert()` method adds an element at a specific position.

---

## 🌍 Real-World Example

A student joins the class late and needs to be placed at roll number 2.

---

## 📝 Syntax

```python
list_name.insert(index, value)
```

---

## 💻 Example

```python
students = ["Gokul", "Rahul", "Priya"]

students.insert(1, "Arun")

print(students)
```

### Output

```
['Gokul', 'Arun', 'Rahul', 'Priya']
```

---

# 4️⃣ remove()

## 📖 What is remove()?

The `remove()` method removes a specific value from the list.

---

## 🌍 Real-World Example

A student leaves the class, so the teacher removes the student's name from the attendance list.

---

## 📝 Syntax

```python
list_name.remove(value)
```

---

## 💻 Example

```python
students = ["Gokul", "Rahul", "Priya"]

students.remove("Rahul")

print(students)
```

### Output

```
['Gokul', 'Priya']
```

---

# 5️⃣ pop()

## 📖 What is pop()?

The `pop()` method removes an element using its index.

If no index is given, it removes the last element.

---

## 🌍 Real-World Example

Imagine removing the last product from a shopping cart.

---

## 📝 Syntax

```python
list_name.pop()
```

or

```python
list_name.pop(index)
```

---

## 💻 Example

```python
students = ["Gokul", "Rahul", "Priya"]

students.pop()

print(students)
```

### Output

```
['Gokul', 'Rahul']
```

---

## 💻 Example

```python
students = ["Gokul", "Rahul", "Priya"]

students.pop(1)

print(students)
```

### Output

```
['Gokul', 'Priya']
```

---

# 6️⃣ clear()

## 📖 What is clear()?

The `clear()` method removes all elements from the list.

---

## 🌍 Real-World Example

At the end of the academic year, the attendance list is cleared for the next batch of students.

---

## 📝 Syntax

```python
list_name.clear()
```

---

## 💻 Example

```python
students = ["Gokul", "Rahul", "Priya"]

students.clear()

print(students)
```

### Output

```
[]
```

---

# 7️⃣ index()

## 📖 What is index()?

The `index()` method returns the position of an element.

---

## 🌍 Real-World Example

Finding the roll number of a student in the attendance list.

---

## 📝 Syntax

```python
list_name.index(value)
```

---

## 💻 Example

```python
students = ["Gokul", "Rahul", "Priya"]

print(students.index("Rahul"))
```

### Output

```
1
```

---

# 8️⃣ count()

## 📖 What is count()?

The `count()` method counts how many times an element appears in the list.

---

## 🌍 Real-World Example

Counting how many students selected Python as their favorite programming language.

---

## 📝 Syntax

```python
list_name.count(value)
```

---

## 💻 Example

```python
numbers = [10, 20, 10, 30, 10]

print(numbers.count(10))
```

### Output

```
3
```

---

# 9️⃣ sort()

## 📖 What is sort()?

The `sort()` method arranges the list in ascending order.

---

## 🌍 Real-World Example

Sorting students' marks from lowest to highest.

---

## 📝 Syntax

```python
list_name.sort()
```

---

## 💻 Example

```python
marks = [75, 45, 90, 60]

marks.sort()

print(marks)
```

### Output

```
[45, 60, 75, 90]
```

---

# 🔟 reverse()

## 📖 What is reverse()?

The `reverse()` method reverses the order of the list.

---

## 🌍 Real-World Example

Displaying the latest messages first in a chat application.

---

## 📝 Syntax

```python
list_name.reverse()
```

---

## 💻 Example

```python
numbers = [1, 2, 3, 4, 5]

numbers.reverse()

print(numbers)
```

### Output

```
[5, 4, 3, 2, 1]
```

---

# 1️⃣1️⃣ copy()

## 📖 What is copy()?

The `copy()` method creates a duplicate copy of a list.

---

## 🌍 Real-World Example

Creating a backup of student records before making changes.

---

## 📝 Syntax

```python
new_list = old_list.copy()
```

---

## 💻 Example

```python
students = ["Gokul", "Rahul", "Priya"]

backup = students.copy()

print(backup)
```

### Output

```
['Gokul', 'Rahul', 'Priya']
```

---

# 📊 Quick Reference Table

| Method | Purpose |
|---------|---------|
| `append()` | Add one element at the end |
| `extend()` | Add another list |
| `insert()` | Add at a specific position |
| `remove()` | Remove a value |
| `pop()` | Remove using index |
| `clear()` | Remove all elements |
| `index()` | Find the position of a value |
| `count()` | Count occurrences |
| `sort()` | Arrange in ascending order |
| `reverse()` | Reverse the list |
| `copy()` | Create a duplicate list |

---

# 📌 Key Points

- Lists are mutable, so they can be changed.
- `append()` adds one element.
- `extend()` adds multiple elements from another list.
- `insert()` adds an element at a specific position.
- `remove()` removes a value.
- `pop()` removes an element using its index.
- `sort()` arranges elements in ascending order.
- `reverse()` changes the order of elements.
- `copy()` creates another list with the same elements.
