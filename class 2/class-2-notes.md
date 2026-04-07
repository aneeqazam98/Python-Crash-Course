# 🐍 Python Crash Course – Class 2

This class focuses on **user input, type conversion, operators, and basic logic building**.
These concepts are essential because they allow your program to **interact with users and make decisions**.

---

# 📥 1. Taking Input from User

```python
name = input("Enter Your Name: ")
print(type(name))

age = input("Enter Your Age: ")
print(type(age))

print(name, age)
```

**Quick Points:**

* `input()` → takes user input
* Always returns **string (str)**

**Detailed Explanation:**
The `input()` function allows the user to enter data during program execution. However, Python **always treats input as a string**, even if the user enters numbers. That’s why type conversion is needed later.

**Output:**

```text
<class 'str'>
<class 'str'>
ayan 15
```

---

# 🔄 2. Type Conversion (Casting)

```python
num = "3"
print("Type before conversion:", type(num))

num2 = int(num)
print("Type after conversion:", type(num2))
```

**Quick Points:**

* `int()` → converts string to integer
* Used when input is numeric

**Detailed Explanation:**
Type conversion is used when you need to change data from one type to another. Since `input()` gives string data, you must convert it into `int` or `float` to perform calculations.

**Output:**

```text
Type before conversion:  <class 'str'>
Type after conversion:  <class 'int'>
```

---

## ❌ Invalid Conversion Example

```python
num = "Hello"
num2 = int(num)
```

**Explanation:**
Not all strings can be converted into numbers. Only numeric strings like `"100"` can be converted. Otherwise, Python throws an error.

**Output:**

```text
ValueError: invalid literal for int() with base 10: 'Hello'
```

---

# 🔢 3. Float Conversion

```python
weight = "60.55"
print(type(weight))

weight = float(weight)
print(type(weight))
print(weight)
```

**Quick Points:**

* `float()` → converts decimal string into float

**Detailed Explanation:**
When dealing with decimal values (like weight, height, price), you should use `float()` instead of `int()`.

**Output:**

```text
<class 'str'>
<class 'float'>
60.55
```

---

# ➕ 4. Mixed Data Calculation

```python
maths = 70
physics = 80
python = "90"

total = maths + physics + int(python)
print(total)
```

**Explanation:**
You cannot directly add string and integer values. The string must first be converted into an integer before performing arithmetic operations.

**Output:**

```text
240
```

---

# ➗ 5. Arithmetic Operators

```python
a = int(input("Enter first value: "))
b = int(input("Enter Second value: "))

print(a + b)
print(a - b)
print(a * b)
print(a / b)
print(a // b)
print(a % b)
print(a ** b)
```

**Quick Points:**

* `+` → addition
* `-` → subtraction
* `*` → multiplication
* `/` → division (float)
* `//` → floor division
* `%` → remainder
* `**` → power

**Detailed Explanation:**
Arithmetic operators are used to perform mathematical operations. Each operator behaves differently, especially `/` (always float) and `//` (removes decimal part).

**Output Example:**

```text
13
7
30
3.3333333333333335
3
1
1000
```

---

# ⚡ 6. Using F-Strings with Input

```python
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))

print(f"Add      : {num1 + num2}")
print(f"Subtract : {num1 - num2}")
print(f"Multiply : {num1 * num2}")
print(f"Divide   : {num1 / num2}")
```

**Explanation:**
F-strings make output clean and readable by directly embedding expressions inside `{}`.

**Output Example:**

```text
Add      : 15.0
Subtract : 5.0
Multiply : 50.0
Divide   : 2.0
```

---

# ⚖️ 7. Comparison Operators

```python
print(10 == 5)
print(10 > 5)
print(10 < 5)
print(10 >= 10)
print(10 <= 9)
```

**Quick Points:**

* `==` → equal
* `!=` → not equal
* `>` `<` → greater/less
* `>=` `<=` → inclusive comparison

**Detailed Explanation:**
Comparison operators compare two values and always return a boolean (`True` or `False`). These are essential for decision-making in programs.

**Output:**

```text
False
True
False
True
False
```

---

# 🧠 8. Logical Operators

```python
age = 20
score = 85

print(age >= 18 and score >= 80)
print(age >= 18 and score >= 90)
print(age < 18 or score >= 80)
print(not True)
```

**Quick Points:**

* `and` → both conditions must be True
* `or` → at least one True
* `not` → reverses result

**Detailed Explanation:**
Logical operators combine multiple conditions. They are widely used in real-world scenarios like validations, login systems, and filtering conditions.

**Output:**

```text
True
False
True
False
```

---

# 🎯 9. Real-Life Example (Age Check)

```python
age = int(input("Enter your age: "))
print(age >= 10 and age <= 18)
```

**Explanation:**
This checks whether the age lies within a specific range. Both conditions must be true for the final result to be true.

---

# 🧮 10. Age Calculation Program

```python
age_years = int(input("Enter your age in years: "))

age_days = age_years * 365
age_hours = age_days * 24
age_minutes = age_hours * 60

print(f"{age_days} days")
print(f"{age_hours} hours")
print(f"{age_minutes} minutes")
```

**Explanation:**
This program converts age into different units using simple arithmetic operations. It demonstrates how calculations can be chained together.

---

# 🔁 11. Assignment Operators

```python
count = 0

count = count + 1
print(count)

count += 1
print(count)

count -= 1
print(count)
```

**Quick Points:**

* `+=` → increase value
* `-=` → decrease value

**Detailed Explanation:**
Assignment operators provide a shorter and cleaner way to update variables. Instead of writing long expressions, you can use shorthand operators.

**Output:**

```text
1
2
3
2
```

---

# 📘 Concepts Covered

* input() function
* Type conversion (int, float)
* Arithmetic operators
* Comparison operators
* Logical operators
* F-strings with input
* Real-world condition checks
* Assignment operators

---

# 🚀 Next Step

Move to Class 3 and start combining logic with conditions to build real programs.

---

# Note

This class is where programming actually begins.
You are no longer just printing — you are **taking input, processing it, and making decisions**.
