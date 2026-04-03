# 🐍 Python Crash Course – Class 1

This repository documents my Python learning journey from scratch.
It is structured in a way that both beginners and intermediate learners can understand concepts clearly with examples and outputs.

---

# 📌 0. Getting Started (Setup Guide)

## What is Python?

Python is a high-level programming language known for its simple syntax and readability.

**Quick Points:**

* Easy to learn
* Widely used in industry
* Supports multiple domains (Web, AI, Automation)

**Detailed Explanation:**
Python is designed to be close to human language, which makes it easier for beginners to understand programming logic. It reduces complexity compared to other languages and allows you to focus more on problem-solving rather than syntax.

---

## Required Tools

### 1. Python

* Core engine that runs your code

**Detailed:**
Python is responsible for interpreting and executing your `.py` files. Without it, your system cannot understand Python code.

---

### 2. Visual Studio Code (VS Code)

* Code editor for writing programs

**Detailed:**
VS Code provides a clean interface, syntax highlighting, and built-in terminal which helps in writing and running code efficiently.

---

## Installation Process

**Steps:**

1. Download Python
2. Run `.exe` file
3. ✔ Tick: **Add Python to PATH**
4. Click Install

**What is `.exe`?**

* Executable installer file
* Used to install software on Windows

---

## Verify Installation

```bash id="2f6kgi"
python
```

**Output:**

```id="rg2m35"
Python 3.x.x
>>>
```

**Explanation:**
If you see this, it means Python is successfully installed and ready to use.

---

# 📂 0.1 Files & Extensions

## File Types

| Extension | Use                           |
| --------- | ----------------------------- |
| `.py`     | Run Python code               |
| `.ipynb`  | Notebook (code + explanation) |
| `.md`     | Documentation                 |

---

## Creating a Python File

```bash id="5y6lmp"
class_1.py
```

**Quick Points:**

* No spaces in file name
* Correct extension required

**Detailed:**
Python only recognizes `.py` files as executable scripts. If the extension is wrong (like `.txt`), the file will not run.

---

# ▶ 0.2 Running Python Code

## Method 1: CMD

```bash id="v6x3ye"
python class_1.py
```

**Output Example:**

```id="r8v3lj"
Hello World
```

**Explanation:**
CMD runs the Python interpreter, which reads your file and executes it line by line.

---

## Method 2: VS Code

* Click ▶ Run
* Or press `Ctrl + F5`

---

## ⚠ Common Mistake

```id="c7qznb"
>>>
```

**Explanation:**
This is Python shell. It is used for quick testing, not for running full files.

---

# 🧾 1. First Program – print()

```python id="9b44kt"
print("Hello World!")
```

**Quick Points:**

* `print()` → display output
* String → text inside quotes

**Detailed Explanation:**
The `print()` function sends data to the console (screen). It is one of the most commonly used functions and is essential for debugging and displaying results.

**Output:**

```id="cf4mtz"
Hello World!
```

---

# 🔢 2. Data Types

```python id="9b7l3f"
print(type("2"))
print(type(2))
```

**Quick Points:**

* `type()` → checks data type
* `"2"` → string
* `2` → integer

**Detailed Explanation:**
Python treats text and numbers differently. Even if something looks like a number but is inside quotes, Python will treat it as a string. Understanding this avoids logical mistakes in programs.

**Output:**

```id="yx7nb2"
<class 'str'>
<class 'int'>
```

---

# 🧵 3. Strings

```python id="33u6qn"
print("Ayan Hussain")
```

**Quick Points:**

* Text inside quotes = string

**Detailed Explanation:**
Strings are used to store textual data such as names, messages, and sentences. They are one of the most commonly used data types in Python.

**Output:**

```id="r3v8xw"
Ayan Hussain
```

---

# 📦 4. Variables

```python id="7zpfm7"
name = "waqas"
print("My name is:", name)
```

**Quick Points:**

* Variable = data container
* `=` → assignment operator

**Detailed Explanation:**
Variables allow you to store values and reuse them. Instead of hardcoding values multiple times, you store them once and reference them wherever needed.

**Output:**

```id="2y5r2c"
My name is: waqas
```

---

# 🔢 5. Numbers & Boolean

```python id="sc5jz9"
age = 50
height = 5.7
is_student = True
```

**Quick Points:**

* `int` → whole numbers
* `float` → decimals
* `bool` → True / False

**Detailed Explanation:**
Different data types are used depending on the kind of data. For example, age is stored as an integer, height as a float, and logical conditions as boolean values.

---

# 🔍 6. Checking Data Type

```python id="z3zj53"
print(type(age))
```

**Output:**

```id="jlwm5o"
<class 'int'>
```

**Explanation:**
This helps verify the type of data stored in a variable, which is useful when debugging or handling dynamic data.

---

# 🔁 7. Overwriting Variables

```python id="8o8nvv"
planet = "Mars"
planet = "Earth"
print(planet)
```

**Quick Points:**

* Latest value replaces old one

**Detailed Explanation:**
Python does not store multiple values in a variable unless explicitly programmed. The most recent assignment always overrides the previous value.

**Output:**

```id="0m9x6n"
Earth
```

---

# ↩ 8. New Line (\n)

```python id="glzv2k"
print("Karachi\nLahore")
```

**Quick Points:**

* `\n` → line break

**Detailed Explanation:**
`\n` is a special escape character that tells Python to move to the next line. It is useful for formatting output.

**Output:**

```id="sl0nzn"
Karachi
Lahore
```

---

# ⚙ 9. print(), sep, end

## Default Behavior

```python id="4ehm48"
print("A", "B", "C")
```

**Output:**

```id="5c0mka"
A B C
```

**Explanation:**
By default:

* `sep = " "` → space between values
* `end = "\n"` → new line after print

---

## sep (Separator)

```python id="mj1n6k"
print("A", "B", "C", sep="-")
```

**Quick Points:**

* Controls space between values

**Detailed Explanation:**
The `sep` parameter allows you to define what should appear between multiple values instead of the default space. This is useful for formatting outputs like dates or lists.

**Output:**

```id="rzcz3h"
A-B-C
```

---

## end (Ending)

```python id="7tdffx"
print("Hello", end=" ")
print("World")
```

**Quick Points:**

* Controls line ending

**Detailed Explanation:**
Normally, `print()` moves to a new line after execution. By changing `end`, you can keep output on the same line or customize the ending.

**Output:**

```id="3f3q2h"
Hello World
```

---

# 🔗 10. String Concatenation

```python id="0m9az1"
first = "Ayan"
last = "Hussain"

print(first + " " + last)
```

**Quick Points:**

* `+` → joins strings

**Detailed Explanation:**
Concatenation combines multiple strings into one. It is commonly used when building full names, sentences, or dynamic messages.

**Output:**

```id="3wdr0z"
Ayan Hussain
```

---

# ⚡ 11. F-Strings (Formatted Strings)

```python id="vtij0b"
name = "Aneeq"
age = 20

print(f"My name is {name} and I am {age}")
```

**Quick Points:**

* `f` → formatted string
* `{}` → insert variables

**Detailed Explanation:**
F-strings allow you to embed variables directly inside a string. This makes the code cleaner and easier to read compared to older formatting methods.

**Output:**

```id="m6zcs9"
My name is Aneeq and I am 20
```

---

## Advanced Example

```python id="8ztnj7"
print(f"Next year age: {age + 1}")
```

**Explanation:**
Python evaluates expressions inside `{}` before printing, which allows dynamic calculations within strings.

**Output:**

```id="gsc1xq"
Next year age: 21
```

---

# 📘 Final Concepts Covered

* print() function
* Variables and assignment
* Data types (str, int, float, bool)
* type() function
* \n (new line)
* sep and end
* String concatenation
* F-strings

---

# 🚀 Next Step

Move to Class 2 and start practicing small programs to strengthen your understanding.

---

# Note

This repository is focused on building strong fundamentals.
The goal is not just to write code, but to clearly understand how and why it works.


