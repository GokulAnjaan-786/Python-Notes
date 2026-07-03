# 💻 LeetCode Problem – Two Sum

## 📖 Problem Statement

You are given a list of integers and a target value.

Find the indexes of the two numbers whose sum is equal to the target.

You can assume that there will always be exactly one correct answer.

---

## 📝 Example

### Input

```python
numbers = [2, 7, 11, 15]
target = 9
```

### Output

```python
[0, 1]
```

### Explanation

```
numbers[0] = 2
numbers[1] = 7

2 + 7 = 9
```

So, the answer is:

```
[0, 1]
```

---

# 🌍 Real-World Example

Imagine you are shopping.

You have gift cards with the following values:

```
₹200
₹700
₹1100
₹1500
```

You want to buy a product worth **₹900**.

Which two gift cards can you use?

```
₹200 + ₹700 = ₹900
```

Similarly, the Two Sum problem finds two numbers whose total is equal to the target.

---

# 💻 Python Solution

```python
numbers = [2, 7, 11, 15]
target = 9

seen = {}

for i in range(len(numbers)):

    difference = target - numbers[i]

    if difference in seen:
        print([seen[difference], i])
        break

    seen[numbers[i]] = i
```

### Output

```
[0, 1]
```

---

# 📖 Step-by-Step Explanation

## Step 1

```python
numbers = [2, 7, 11, 15]
```

This is our list.

| Index | Value |
|------:|------:|
| 0 | 2 |
| 1 | 7 |
| 2 | 11 |
| 3 | 15 |

---

## Step 2

```python
target = 9
```

We need two numbers whose sum is **9**.

---

## Step 3

```python
seen = {}
```

Create an empty dictionary.

This dictionary stores:

```
Number : Index
```

Initially,

```
{}
```

---

## Step 4

```python
for i in range(len(numbers)):
```

The loop visits every element.

### First Iteration

```
i = 0
```

Current Number

```
2
```

---

## Step 5

```python
difference = target - numbers[i]
```

```
difference = 9 - 2
```

```
difference = 7
```

Now Python asks,

> "Have I already seen 7?"

---

## Step 6

```python
if difference in seen:
```

Currently,

```
seen = {}
```

There is no 7.

So,

```
False
```

---

## Step 7

```python
seen[numbers[i]] = i
```

Store

```
2 : 0
```

Dictionary becomes

```
{
    2 : 0
}
```

---

## Second Iteration

```
i = 1
```

Current Number

```
7
```

Difference

```
9 - 7 = 2
```

Now Python checks

```
Is 2 inside the dictionary?
```

Answer

```
Yes
```

because

```
{
    2 : 0
}
```

already exists.

---

## Step 8

```python
print([seen[difference], i])
```

```
seen[2]
```

gives

```
0
```

Current index

```
1
```

So,

```
[0,1]
```

is printed.

---

## Step 9

```python
break
```

The answer is found.

The loop stops.

---

# 🧠 Final Dictionary

```
{
    2 : 0
}
```

This means

```
Number 2 is at index 0
```

---

# ⏱️ Time Complexity

```
O(n)
```

Python visits every number only once.

This makes the solution very fast.

---

# 📌 Key Idea

Instead of searching the list again and again,

we store the numbers in a dictionary.

Since dictionary lookup is very fast,

the program becomes efficient.

---

# 👨‍💻 Taking User Input

Instead of using fixed values,

```python
numbers = [2, 7, 11, 15]
target = 9
```

we can take input from the user.

```python
numbers = list(map(int, input("Enter numbers separated by spaces: ").split()))

target = int(input("Enter Target: "))

seen = {}

for i in range(len(numbers)):

    difference = target - numbers[i]

    if difference in seen:
        print("Indexes:", [seen[difference], i])
        break

    seen[numbers[i]] = i
```

### Sample Input

```
Enter numbers separated by spaces:
2 7 11 15

Enter Target:
9
```

### Output

```
Indexes: [0, 1]
```

---

# 🎯 What You Learned

- How to use a dictionary for fast searching.
- How to solve the famous Two Sum problem.
- How to trace the program step by step.
- How to take list input from the user.
- Why dictionaries are useful in coding interviews.
