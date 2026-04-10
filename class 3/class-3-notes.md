# 🐍 Python Crash Course – Class 3

This class introduces **Lists (data collections)** and **Conditional Statements (decision making)**.
These concepts allow you to store multiple values and control program behavior based on conditions.

---

# 📦 1. Lists (Collection of Values)

```python
ayesha_marks = [90, 80, 70, 50, 75]
print(ayesha_marks)
```

**Quick Points:**

* List → collection of values
* Defined using `[]` (square brackets)
* Values separated by commas

**Detailed Explanation:**
Instead of creating multiple variables for each subject, lists allow you to store all values in a single variable. This makes code cleaner, scalable, and easier to manage—especially when dealing with large datasets.

**Output:**

```text
[90, 80, 70, 50, 75]
```

---

# 🧠 Why Lists are Important

Without lists:

```python
maths = 90
computer = 80
python = 70
```

With lists:

```python
marks = [90, 80, 70]
```

👉 This reduces complexity and improves structure.

---

# 🧾 2. Lists with Strings

```python
subjects = ['Maths', 'Computer', 'Python', 'English', 'Biology']
print(subjects)
```

**Explanation:**
Lists can store strings, numbers, or mixed data. Each item is stored in order.

**Output:**

```text
['Maths', 'Computer', 'Python', 'English', 'Biology']
```

---

# 🔢 3. List Indexing

```python
print(subjects[0])
print(subjects[4])
```

**Quick Points:**

* Index starts from `0`
* Left → Right indexing

**Detailed Explanation:**
Each value in a list has a position called an index. Python starts counting from 0, not 1. This is important and often confusing for beginners.

**Output:**

```text
Maths
Biology
```

---

# 🔁 4. Negative Indexing

```python
print(subjects[-1])
```

**Quick Points:**

* `-1` → last element
* Right → Left indexing

**Detailed Explanation:**
Negative indexing allows you to access elements from the end of the list. This is useful when you don’t know the exact length of the list.

**Output:**

```text
Biology
```

---

# ➕ 5. Adding Data (append)

```python
students = ['Ayan', 'Aliza', 'Dawood']
students.append("Sarfaraz")
print(students)
```

**Quick Points:**

* `append()` → adds value at end

**Detailed Explanation:**
The `append()` method adds a new item to the end of the list. It does not replace existing values—it only extends the list.

**Output:**

```text
['Ayan', 'Aliza', 'Dawood', 'Sarfaraz']
```
## 🔹 insert vs append

👉 Research and practice:

* `append()` → adds at end
* `insert(index, value)` → adds at specific position

Example:

```python
students.insert(1, "Ali")
```

---

---

# ❌ 6. Removing Data (pop)

```python
students.pop()
print(students)
```

**Quick Points:**

* `pop()` → removes last item
* Can also remove by index

**Detailed Explanation:**
The `pop()` function removes elements. By default, it removes the last value, but you can also specify an index.

**Output:**

```text
['Ayan', 'Aliza', 'Dawood']
```

## 🔹 remove vs pop

👉 Difference:

* `remove(value)` → removes by value
* `pop(index)` → removes by index

---

---

## ⚠ Error Example

```python
students.pop(5)
```

**Explanation:**
If the index does not exist, Python throws an error.

**Output:**

```text
IndexError: pop index out of range
```

---

# 📊 7. Multiple Data Types in List

```python
bio_data = ['Ayan', 'Hussain', 50, 5.10, True]
print(bio_data)
```

**Explanation:**
Python lists can store different data types together, unlike many other languages.

**Output:**

```text
['Ayan', 'Hussain', 50, 5.1, True]
```

---


# ⚖️ 8. If-Else (Decision Making)

```python
age = int(input("Enter your age"))

if age > 10 and age < 18:
    print("Yes! you are eligible....")
else:
    print("No! you are not eligible...")
```

**Quick Points:**

* `if` → condition check
* `else` → fallback

**Detailed Explanation:**
If-Else allows your program to make decisions. Based on conditions, different blocks of code execute.

---

# 📊 9. Grading System

```python
marks = int(input("Enter your marks: "))

if marks >= 90:
    print("Grade A+")
elif marks >= 80:
    print("Grade A")
elif marks >= 70:
    print("Grade B")
else:
    print("Grade F")
```

**Explanation:**
`elif` allows multiple conditions. Python checks them one by one and executes the first true condition.

---

# 🔍 10. Number Check Program

```python
number = int(input("Enter a number"))

if number > 0:
    print("Positive number")
elif number < 0:
    print("Negative number")
else:
    print("Zero")
```

---

# 🧠 11. Nested If-Else

```python
logged_in = False
is_teacher = False

if logged_in:
    if is_teacher:
        print("Welcome, Teacher!")
    else:
        print("Welcome, Student")
else:
    print("Please Login")
```

**Explanation:**
Nested if means placing an `if` inside another `if`. This is used for complex decision-making.

---

# 🎯 12. Real-Life Example (Weekend Logic)

```python
is_weekend = True
is_sunday = True

if is_weekend:
    if is_sunday:
        print("Go to Ocean")
    else:
        print("Cricket Day")
else:
    print("Weekdays")
```

---

# 🔐 13. Login System (Important)

```python
correct_username = "admin"
correct_password = "123"

username = input("Enter username: ")
password = input("Enter password: ")

if username == correct_username and password == correct_password:
    print("Login Successful!")
elif username != correct_username:
    print("Wrong username.")
else:
    print("Wrong password.")
```

**Explanation:**
This is a real-world example combining input + conditions + logical operators.

---

# 🔍 14. Checking Value in List

```python
players = ['Amir', 'Watson', 'Starc', 'Ayan']

if 'Ayan' in players:
    print("Start booking flights")
```

**Quick Points:**

* `in` → checks existence

**Detailed Explanation:**
The `in` keyword is used to check whether a value exists inside a list.

---

# 📘 Concepts Covered

* Lists (creation, indexing, operations)
* append() and pop()
* If-Else logic
* Nested conditions
* Logical operators
* Real-world programs

---

# 🚀 Next Step

Move to the next class where you will start building more complex logic and structured programs.

---

# Note

This class marks the shift from basic coding to **logical thinking and problem solving**.
You are now learning how real programs make decisions and manage data.
