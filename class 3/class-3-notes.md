# 🐍 Python Crash Course – Class 3

This class introduces Lists (data collections) and Conditional Statements (decision making).
These concepts allow you to store structured data and control program flow based on logic, which is the foundation of real-world programming.

---

## 📦 1. Lists (Collection of Values)

```python
ayesha_marks = [90, 80, 70, 50, 75]
print(ayesha_marks)
```

### Quick Points:

* List → collection of values
* Defined using [] (square brackets)
* Values separated by commas

### Detailed Explanation:

A list is used when you need to store multiple related values in a single variable. Instead of creating separate variables for each subject or student, lists allow grouping data logically.

Think of a list as a container or box that holds multiple items in order.

👉 This becomes extremely powerful when:

* You have large data (e.g., 100 students)
* You need to loop or process data later (coming in next classes)

### Output:

```text
[90, 80, 70, 50, 75]
```

---

## 🧠 Why Lists are Important

### Without lists:

```python
maths = 90
computer = 80
python = 70
```

### With lists:

```python
marks = [90, 80, 70]
```

### Deeper Insight:

Without lists, your code becomes:

* Hard to manage
* Repetitive
* Not scalable

With lists:

* You write less code
* You can process data easily
* You can automate logic later

👉 Lists are the first step toward data handling.

---

## 🧾 2. Lists with Strings

```python
subjects = ['Maths', 'Computer', 'Python', 'English', 'Biology']
print(subjects)
```

### Detailed Explanation:

Lists are flexible — they can store:

* Strings
* Numbers
* Boolean values
* Even mixed data

Each value is stored in sequence, and Python remembers the order.

### Output:

```text
['Maths', 'Computer', 'Python', 'English', 'Biology']
```

---

## 🔢 3. List Indexing

```python
print(subjects[0])
print(subjects[4])
```

### Quick Points:

* Index starts from 0
* Left → Right indexing

### Detailed Explanation:

Every item in a list has a position called an index.
Python uses zero-based indexing, meaning:

| Value    | Index |
| -------- | ----- |
| Maths    | 0     |
| Computer | 1     |
| Python   | 2     |
| English  | 3     |
| Biology  | 4     |

👉 Formula mindset:
Total items = n → last index = n - 1

### Output:

```text
Maths
Biology
```

---

## 🔁 4. Negative Indexing

```python
print(subjects[-1])
```

### Quick Points:

* -1 → last element
* Access from right side

### Detailed Explanation:

Negative indexing is useful when:

* You don’t know list length
* You want last/latest data

Example:

-1 → last item
-2 → second last

### Output:

```text
Biology
```

---

## ➕ 5. Adding Data (append)

```python
students = ['Ayan', 'Aliza', 'Dawood']
students.append("Sarfaraz")
print(students)
```

### Quick Points:

* append() → adds value at end

### Detailed Explanation:

append() modifies the original list (in-place).
It does NOT create a new list — it updates the existing one.

👉 Important mindset:

Lists are mutable (changeable)

### Output:

```text
['Ayan', 'Aliza', 'Dawood', 'Sarfaraz']
```

---

### 🔹 insert vs append (Homework – Must Understand)

#### append():

```python
students.append("Ali")
```

➡ Always adds at end

#### insert():

```python
students.insert(1, "Ali")
```

➡ Adds at specific position

### Deep Insight:

* Use append() → when order doesn’t matter
* Use insert() → when position matters

---

## ❌ 6. Removing Data (pop)

```python
students.pop()
print(students)
```

### Quick Points:

* pop() → removes last item
* Can remove by index

### Detailed Explanation:

pop() removes and returns the value.
This is important — you can store it:

```python
removed = students.pop()
```

👉 Useful in real systems like:

* Undo operations
* Removing last entry

### Output:

```text
['Ayan', 'Aliza', 'Dawood']
```

---

### 🔹 remove vs pop (Homework – Must Understand)

#### remove():

```python
students.remove("Ayan")
```

➡ Removes by value

#### pop():

```python
students.pop(0)
```

➡ Removes by index

### Key Difference:

| Function | Works On |
| -------- | -------- |
| remove() | value    |
| pop()    | index    |

---

## ⚠ Error Example

```python
students.pop(5)
```

### Explanation:

If index doesn’t exist → program crashes.

👉 Beginner mistake:
Always ensure index is valid before accessing/removing.

### Output:

```text
IndexError: pop index out of range
```

---

## 📊 7. Multiple Data Types in List

```python
bio_data = ['Ayan', 'Hussain', 50, 5.10, True]
print(bio_data)
```

### Detailed Explanation:

Python lists are dynamic — they allow multiple data types in one list.

👉 But in real-world systems:

Try to keep data consistent for clarity

### Output:

```text
['Ayan', 'Hussain', 50, 5.1, True]
```

---

## ⚖️ 8. If-Else (Decision Making)

```python
age = int(input("Enter your age"))

if age > 10 and age < 18:
    print("Yes! you are eligible....")
else:
    print("No! you are not eligible...")
```

### Quick Points:

* if → condition check
* else → fallback

### Detailed Explanation:

If-Else controls program flow.
Your program becomes dynamic — it reacts based on input.

👉 Without conditions → static program
👉 With conditions → intelligent program

---

## 📊 9. Grading System

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

### Detailed Explanation:

Python checks conditions top to bottom.
Once one condition is true → rest are ignored.

👉 Important rule:
Order of conditions matters.

---

## 🔍 10. Number Check Program

```python
number = int(input("Enter a number"))

if number > 0:
    print("Positive number")
elif number < 0:
    print("Negative number")
else:
    print("Zero")
```

### Explanation:

This is a classic logic-building exercise.
It trains your brain to think in conditions.

---

## 🧠 11. Nested If-Else

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

### Detailed Explanation:

Nested conditions are used when:
👉 One condition depends on another

Real-world example:

* First check login
* Then check role

---

## 🎯 12. Real-Life Example (Weekend Logic)

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

### Explanation:

This models real-life decisions using logic layers.

---

## 🔐 13. Login System (Important)

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

### Detailed Explanation:

This combines:

* Input
* Comparison
* Logical operators

👉 This is your first real-world system simulation

---

## 🔍 14. Checking Value in List

```python
players = ['Amir', 'Watson', 'Starc', 'Ayan']

if 'Ayan' in players:
    print("Start booking flights")
```

### Quick Points:

* in → checks existence

### Detailed Explanation:

The in keyword scans the list and checks if a value exists.

👉 Used in:

* Search systems
* Validation
* Filters

---

## 📘 Concepts Covered

* Lists (creation, indexing, operations)
* append(), insert(), pop(), remove()
* If-Else logic
* Nested conditions
* Logical operators
* Real-world logic building

---

## 🚀 Next Step

Next class → you’ll start combining:

* Lists + Loops
* Logic + Automation

That’s where real power begins.

---

## Note

This class is a turning point.
You’re no longer just writing code — you’re learning how to structure data and control logic like a programmer.

---

## 🔥 My Straight Advice

If you master this class:

* You’re ahead of 70% beginners
* You can already build basic apps

If you don’t:

* Everything ahead will feel confusing

👉 So revise this twice.
