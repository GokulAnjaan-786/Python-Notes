---

# 🔧 Common String Functions in Python

Python provides many built-in functions to work with strings. These functions make it easy to modify, search, and analyze text.

---

# 1️⃣ upper()

## 📖 Definition

The `upper()` function converts all characters in a string to uppercase.

### 🌍 Real-World Example

When filling an online form, some websites automatically convert your name to uppercase.

### 💻 Example

```python
name = "gokul"

print(name.upper())
```

### Output

```
GOKUL
```

---

# 2️⃣ lower()

## 📖 Definition

The `lower()` function converts all characters in a string to lowercase.

### 🌍 Real-World Example

Email addresses are usually stored in lowercase.

### 💻 Example

```python
email = "GOKUL@GMAIL.COM"

print(email.lower())
```

### Output

```
gokul@gmail.com
```

---

# 3️⃣ capitalize()

## 📖 Definition

The `capitalize()` function converts the first letter into uppercase and the remaining letters into lowercase.

### 💻 Example

```python
name = "gOKUL"

print(name.capitalize())
```

### Output

```
Gokul
```

---

# 4️⃣ title()

## 📖 Definition

The `title()` function converts the first letter of every word into uppercase.

### 🌍 Real-World Example

Useful for formatting names and book titles.

### 💻 Example

```python
sentence = "welcome to python"

print(sentence.title())
```

### Output

```
Welcome To Python
```

---

# 5️⃣ strip()

## 📖 Definition

The `strip()` function removes spaces from the beginning and end of a string.

### 🌍 Real-World Example

Useful when users accidentally type extra spaces while entering their username or email.

### 💻 Example

```python
name = "   Gokul   "

print(name.strip())
```

### Output

```
Gokul
```

---

# 6️⃣ replace()

## 📖 Definition

The `replace()` function replaces one value with another.

### 🌍 Real-World Example

Correcting spelling mistakes in a sentence.

### 💻 Example

```python
sentence = "I love Java"

print(sentence.replace("Java", "Python"))
```

### Output

```
I love Python
```

---

# 7️⃣ split()

## 📖 Definition

The `split()` function converts a string into a list.

### 🌍 Real-World Example

Splitting a full name into first name and last name.

### 💻 Example

```python
sentence = "Python is easy"

print(sentence.split())
```

### Output

```python
['Python', 'is', 'easy']
```

---

# 8️⃣ join()

## 📖 Definition

The `join()` function joins list elements into a single string.

### 💻 Example

```python
words = ["Python", "is", "easy"]

print(" ".join(words))
```

### Output

```
Python is easy
```

---

# 9️⃣ find()

## 📖 Definition

The `find()` function returns the position of the first occurrence of a character or word.

If it is not found, it returns **-1**.

### 💻 Example

```python
name = "Python"

print(name.find("t"))
```

### Output

```
2
```

---

# 🔟 count()

## 📖 Definition

The `count()` function counts how many times a value appears in a string.

### 💻 Example

```python
text = "banana"

print(text.count("a"))
```

### Output

```
3
```

---

# 1️⃣1️⃣ startswith()

## 📖 Definition

Checks whether the string starts with the given value.

### 💻 Example

```python
website = "https://google.com"

print(website.startswith("https"))
```

### Output

```
True
```

---

# 1️⃣2️⃣ endswith()

## 📖 Definition

Checks whether the string ends with the given value.

### 💻 Example

```python
file = "notes.pdf"

print(file.endswith(".pdf"))
```

### Output

```
True
```

---

# 1️⃣3️⃣ isalpha()

## 📖 Definition

Returns **True** if all characters are alphabets.

### 💻 Example

```python
name = "Python"

print(name.isalpha())
```

### Output

```
True
```

---

# 1️⃣4️⃣ isdigit()

## 📖 Definition

Returns **True** if all characters are numbers.

### 💻 Example

```python
number = "2026"

print(number.isdigit())
```

### Output

```
True
```

---

# 1️⃣5️⃣ isalnum()

## 📖 Definition

Returns **True** if the string contains only letters and numbers.

### 💻 Example

```python
text = "Python123"

print(text.isalnum())
```

### Output

```
True
```

---

# 📊 Most Common String Functions

| Function | Purpose |
|----------|---------|
| `upper()` | Converts to uppercase |
| `lower()` | Converts to lowercase |
| `capitalize()` | First letter uppercase |
| `title()` | First letter of every word uppercase |
| `strip()` | Removes extra spaces |
| `replace()` | Replaces text |
| `split()` | Converts string to list |
| `join()` | Converts list to string |
| `find()` | Finds the position of text |
| `count()` | Counts occurrences |
| `startswith()` | Checks starting text |
| `endswith()` | Checks ending text |
| `isalpha()` | Checks only letters |
| `isdigit()` | Checks only numbers |
| `isalnum()` | Checks letters and numbers |

---

# 📌 Important Points

- Strings are immutable, which means they cannot be changed directly.
- Most string functions return a new string.
- String functions are very useful in login systems, search boxes, form validation, and text processing.
- Always remember that Python is case-sensitive.
- `find()` returns **-1** if the value is not found.

---

