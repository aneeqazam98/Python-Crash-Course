# 🐍 Python Crash Course – Class 6

This class focuses on **Dictionaries (key-value data structure)**, **dictionary methods**, **looping with dictionaries**, **real-world problem solving**, **tuples**, and **string case methods**.

👉 This is where data handling becomes structured and closer to real-world applications.

---

## 📦 1. Lists vs Dictionaries (Core Understanding)

```python
marks = [100,90,80,76,57]
subjects = ["maths","Sci","python"]
print(marks[2])
```

**Output:**

```text
80
```

**Detailed Explanation:**

👉 Lists store values using **index positions**

👉 Problem:
You don’t know what 80 represents (Maths? Science?)

👉 This is where dictionaries solve the problem.

👉 **Beginner Insight (Very Important):**
Lists = position-based
Dictionaries = meaning-based

👉 Real world example:

List:

```python
[100, 90, 80]
```

Dictionary:

```python
{"maths":100, "science":90, "python":80}
```

👉 Which one is clearer? Obviously dictionary.

---

## 🧠 2. Dictionaries (Key-Value Concept)

```python
student = {
    "name":"ayan",
    "age": 50,
    "marks": 100,
    "email": "ayanhussain@gmail.com"
}
print(student)
```

**Output:**

```text
{'name': 'ayan', 'age': 50, 'marks': 100, 'email': 'ayanhussain@gmail.com'}
```

**Quick Points:**

* Uses `{}` (curly brackets)
* Stores data as key → value pairs
* More structured than lists

**Deep Explanation:**

👉 A dictionary works like a **real-world record system**

Think of it like:

* Student Form
* Database Row
* JSON Object (used in APIs)

👉 Structure:

```python
key : value
```

👉 Rules:

* Keys must be unique
* Values can be anything (list, string, int, boolean)

👉 **Beginner Insight:**
Dictionary = “label + value”

---

## 🔍 3. Accessing Data

```python
print(student["email"])
```

**Output:**

```text
ayanhussain@gmail.com
```

👉 Access using key instead of index

👉 **Think like this:**
Instead of saying “give me position 2”
You say → “give me email”

---

## ⚠️ KeyError Concept

```python
print(student["roll_no"])
```

**Output:**

```text
KeyError: 'roll_no'
```

**Explanation:**

👉 If key doesn’t exist → program crashes

👉 **Beginner Mistake:**
Assuming key exists without checking

👉 **Safe mindset:**
Always verify key or use `.get()`

---

## ✏️ 4. Updating & Adding Data

```python
student["passed"] = False
```

👉 Updates if key exists
👉 Adds if key does not exist

```python
student["id"] = 'ABC-123'
```

👉 New key added

👉 **Beginner Insight:**
Dictionary is dynamic — it grows as needed

---

## 📦 Nested Data (Very Important)

```python
student["grades"].append(66)
```

👉 Dictionary can contain:

* Lists
* Booleans
* Strings
* Numbers

👉 **Real-world Insight:**
Data is never flat — it’s always nested

Example:

```python
student = {
    "name": "ayan",
    "grades": [80,90,70]
}
```

👉 You can now manipulate inner data

---

## ❌ 5. Deleting Data

```python
del student['id']
```

👉 Removes key-value pair completely

👉 **Use Case:**
Removing unnecessary data

---

## 🔍 6. Checking Key with `in`

```python
if 'email' in student:
    print(student["email"])
else:
    print("Does not exixt")
```

👉 Prevents errors

👉 **Best Practice:**
Never directly access unknown keys

---

## 📏 7. Length of Dictionary

```python
print(len(student))
```

👉 Counts total keys

👉 **Beginner Insight:**
len() works on lists, strings, dictionaries

---

# ⚙️ 8. Dictionary Methods (Very Important)

---

## 🔹 get()

```python
print(student.get('name'))
print(student.get('names'))
print(student.get("names",'N/A'))
```

**Output:**

```text
ayan
None
N/A
```

👉 Safer than `[]`

👉 **Key Difference:**

| Method | If key missing |
| ------ | -------------- |
| []     | Error          |
| get()  | Safe           |

👉 **Best Practice:**
Use `get()` in real applications

---

## 🔹 keys()

```python
print(student.keys())
```

👉 Returns all keys

👉 Used when you only need labels

---

## 🔹 values()

```python
print(student.values())
```

👉 Returns all values

---

## 🔹 items()

```python
print(student.items())
```

👉 Returns key-value pairs

👉 Most powerful for looping

---

## 🔹 update()

```python
student.update({'name': 'hussain',
 'age': 49,
 'marks': 99})
```

👉 Updates multiple values at once

👉 Cleaner than multiple assignments

---

# 🔁 9. Looping Over Dictionary

---

## Loop Keys

```python
for key in student.keys():
    print(key)
```

👉 Useful when only keys matter

---

## Loop Values

```python
for value in student.values():
    print(value)
```

👉 Useful when only values matter

---

## Loop Both (Most Important)

```python
for key,value in student.items():
    print(key, " -> ", value)
```

👉 **Beginner Insight:**
This is how real programs read structured data

---

# 🎯 10. Problem Solving (List of Dictionaries)

```python
students = [
    {"name":"ayan","grade":"A"},
    {"name":"affan","grade":"B"},
    {"name":"aziz","grade":"C"},
    {"name":"aftab","grade":"A"},
    {"name":"sarfaraz","grade":"E"},
    {"name":"hanzala","grade":"F"}
]

for student in students:
    print(f'Student Name is: {student["name"]} and grade is {student["grade"]}')
```

👉 Structure:

List → contains multiple dictionaries

👉 Real-world analogy:

* Database table
* Each row = dictionary

---

# 📊 11. Average Calculation (Important Logic)

```python
students ={
    "Ali":[80,90,70],
    "Ayan":[100,50,20],
    "Aftab":[60,57,66]
}

for name, marks in students.items():
    avg = sum(marks) / len(marks)
    print(name, "average marks =", avg)
```

👉 Combines:

* Loop
* Dictionary
* Math

👉 **Deep Insight:**
This is how analytics systems work

---

# 🛒 12. Filtering Data (Real Use Case)

```python
products ={
    "apple":80,
    "mango":200,
    "banana": 50,
    "oranges":180
}

expensive_products = {}

max_price = 100
for fruit,price in products.items():
    if price > max_price:
        expensive_products[fruit] = price
print(expensive_products)
```

👉 Output:

```text
{'mango': 200, 'oranges': 180}
```

👉 **Concept:**
Filtering

👉 **Real Use Cases:**

* Expensive products
* High-value customers
* Fraud detection

---

# 🔒 13. Tuples (Immutable Data)

```python
fruits = ("apple","mango","grapes")
fruits[0] = 'dates'
```

**Output:**

```text
TypeError: 'tuple' object does not support item assignment
```

**Explanation:**

👉 Tuples cannot be changed

👉 **Beginner Insight:**

| Type  | Mutable |
| ----- | ------- |
| List  | Yes     |
| Tuple | No      |

👉 Use tuples when data must remain constant

---

# 🔤 14. String Case Methods

```python
name = "Ayan hussain"
print(name.upper())
```

👉 Output:

```text
AYAN HUSSAIN
```

---

```python
print(name.lower())
```

👉 Output:

```text
ayan hussain
```

---

```python
print(name.title())
```

👉 Output:

```text
Ayan Hussain
```

---

```python
print(name.capitalize())
```

👉 Output:

```text
Ayan hussain
```

👉 **Real Use Cases:**

* Formatting user input
* Cleaning data
* Display formatting

---

# ⭐ 15. Mini Project – Contact Book

👉 Build a contact book using:

* dictionary
* input()
* while loop

### Features:

1. Add contact (name, phone, city)
2. Search contact
3. Show all contacts
4. Exit program

---

## 🧠 How It Should Work (Beginner Breakdown)

👉 Step-by-step thinking:

1. Start program
2. Show menu
3. Take user input
4. Perform action
5. Repeat until exit

👉 This builds:

* Logic thinking
* Real program flow
* User interaction

---

# 📘 Concepts Covered

* Dictionaries (core structure)
* Key-value logic
* Dictionary methods
* Looping dictionaries
* Data processing
* Filtering logic
* Tuples (immutability)
* String methods

---

# 🔥 My Straight Advice

If you master dictionaries:

* You can handle real-world data
* You can build actual projects

If you don’t:

* You’ll stay stuck in basic coding

👉 This is a critical turning point — don’t take it lightly.
