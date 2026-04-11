# 🐍 Python Crash Course – Class 4

This class introduces **Loops (repetition & automation)** and strengthens your understanding of **logic with conditions inside loops**.
These concepts are critical because they allow you to **automate tasks instead of writing repetitive code manually**.

---

## 🔍 1. Checking Value using `in`

```python
players = ['Amir', 'Watson', 'Starc']

if 'Ayan' in players:
    print("start booking your flights.....")
else:
    print("No ....")
```

### Quick Points:

* `in` → checks if value exists
* Used with lists, strings, etc

### Detailed Explanation:

The `in` keyword searches through the list and checks whether a specific value exists or not.

👉 Internally, Python checks each item one by one.

👉 If found → True
👉 If not found → False

👉 Beginner Insight:
Think of it like searching a name in a class list manually. Python is doing the same thing behind the scenes.

### Output:

```text
No ....
```

---

# 🔁 2. Loops (Repetition)

Loops are used when you want to **repeat a task multiple times automatically**.

👉 Instead of writing 100 print statements, you use a loop.

👉 Real-life analogy:
Imagine telling someone to print numbers from 1 to 100. Without loops, you would repeat instructions 100 times. With loops, you give one instruction — and it repeats automatically.

### Types of Loops:

* `for loop` → used when number of iterations is known
* `while loop` → used when condition-based repetition is needed

---

## 🔄 3. For Loop (Basic Syntax)

```python
for i in range(10):
    print(i)
```

### Quick Points:

* `for` → loop keyword
* `i` → iterator (temporary variable)
* `range()` → generates sequence

### Detailed Explanation:

This loop runs 10 times.

👉 `range(10)` generates numbers from **0 to 9**
👉 Each value is stored in `i` one by one

👉 Deep Insight:

* `i` is not special — you can name it anything
* It just holds current value in each iteration

👉 Execution flow:

1. Start loop
2. Assign first value to `i`
3. Run print
4. Move to next value
5. Repeat until range ends

### Output:

```text
0
1
2
3
4
5
6
7
8
9
```

---

## 🧠 EXTRA: Loop Syntax (Must Understand Deeply)

```python
# for iterator in iterable:
#     statement / code logic
```

### Deep Breakdown:

* `iterator` → variable that stores current value
* `iterable` → data source (list, range, string)
* `:` → start of block
* indentation → defines loop body

👉 Non-programmer explanation:
“Take items one by one from a collection and do something with each.”

---

## ⚠️ Heavy Loop Example (Important Concept)

```python
for a in range(100000000):
    print(a)
```

### Explanation:

This will run **100 million times**, which can freeze or crash your system.

👉 Real-world lesson:
Always be careful with large loops — they consume CPU and time.

👉 Beginner mistake:
Thinking “computer fast hai” → but logic matters more than speed.

---

## 📦 4. Looping Through List

```python
numbers = [10,1,5,6,8,24,22,475]

for num in numbers:
    print(num)
```

### Quick Points:

* Loop directly over list
* No need for index

### Detailed Explanation:

Instead of accessing elements using index, Python allows direct iteration.

👉 Behind the scenes:

* First value → 10 → printed
* Second value → 1 → printed
* continues till list ends

👉 This approach:

* Reduces errors
* Improves readability

### Output:

```text
10
1
5
6
8
24
22
475
```

---

## 🧾 5. Loop with Strings (Names Example)

```python
names = ['Ali', 'Ayan','Ahmed','Shayan']

for name in names:
    print(name)
```

👉 Same logic applies — just different data type (strings instead of numbers)

### Output:

```text
Ali
Ayan
Ahmed
Shayan
```

---

## ⛔ 6. break Statement

```python
names = ['Ali', 'Ayan','Ahmed','Shayan']

for name in names:
    print(1)
    break
    print(name)
```

### Quick Points:

* `break` → stops loop immediately

### Detailed Explanation:

As soon as Python encounters `break`, the loop **terminates instantly**.

👉 Important:
Code after `break` inside loop will NEVER run

👉 Real-world analogy:
You’re searching for a person in a list — once found, you stop searching.

### Output:

```text
1
```

---

## 🌍 7. Another Example (Planets)

```python
planets = ['earth','mars','sasid']

for planet in planets:
    print(planet)
```

👉 Simple iteration — same pattern everywhere

### Output:

```text
earth
mars
sasid
```

---

## 🔢 8. range() Variations

### 1️⃣ Single Parameter

```python
for i in range(7):
    print(i)
```

👉 Starts from 0 by default

👉 Internal sequence:
0 → 1 → 2 → 3 → 4 → 5 → 6

### Output:

```text
0
1
2
3
4
5
6
```

---

### 2️⃣ Two Parameters (start, stop)

```python
for i in range(10,20):
    print(i)
```

### Key Rule:

* Start → included
* Stop → excluded

👉 Important mindset:
Python stops BEFORE the stop value

### Output:

```text
10
11
12
13
14
15
16
17
18
19
```

---

### 3️⃣ Inclusive Range Trick

```python
for i in range(10,21):
    print(i)
```

👉 To include 20, we use 21

👉 This is a very common beginner confusion

### Output:

```text
10
11
12
13
14
15
16
17
18
19
20
```

---

## ✖️ 9. Table Example (F-String + Loop)

```python
for i in range(0, 11):
    print(f"2 x {i} = {2 * i}")
```

### Detailed Explanation:

This is a practical example combining:

* Loop
* F-string
* Calculation

👉 Each iteration:

* `i` changes
* Expression recalculates
* Output updates dynamically

👉 This is how programs generate dynamic reports.

### Output:

```text
2 x 0 = 0
2 x 1 = 2
2 x 2 = 4
2 x 3 = 6
2 x 4 = 8
2 x 5 = 10
2 x 6 = 12
2 x 7 = 14
2 x 8 = 16
2 x 9 = 18
2 x 10 = 20
```

---

## ⚙️ 10. Loop with Condition (Even/Odd Separation)

```python
numbers = [1,2,3,4,5,6,7,8,9,10]

even_numbers = []
odd_numbers = []

for num in numbers:
    if num % 2 == 0:
        even_numbers.append(num)
    else:
        odd_numbers.append(num)

print(even_numbers)
print(odd_numbers)
```

### Quick Points:

* `%` → modulo operator
* Even → divisible by 2
* Odd → not divisible by 2

### Detailed Explanation:

This is a **real programming logic example**.

👉 Step-by-step:

1. Loop through each number
2. Check condition
3. Store in separate lists

👉 Deep Insight:

* `%` gives remainder
* If remainder = 0 → even
* Else → odd

👉 This is how data is filtered in real systems.

### Output:

```text
[2, 4, 6, 8, 10]
[1, 3, 5, 7, 9]
```

---

## 🧠 EXTRA: Even Numbers Only (Filtered Output)

```python
# loop with inside if condition 
# print (even) numbers 

numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

even_numbers = []

for num in numbers:
    if num % 2 == 0:
        even_numbers.append(num)

print(even_numbers)
```

### Detailed Explanation:

👉 This is called a **filtering pattern**

Step-by-step:

* Loop runs for each number
* Condition checks if number is even
* If true → added to list
* If false → ignored

👉 Key Learning:
You don’t always need `else`
Sometimes you only care about one condition

👉 Real-world use:

* Filter active users
* Filter passing students
* Filter valid transactions

### Output:

```text
[2, 4, 6, 8, 10]
```

---

# 📘 Concepts Covered

* `in` keyword
* Loops (for loop basics)
* range() function
* Looping through lists
* break statement
* F-strings with loops
* Conditional logic inside loops
* Data filtering (even/odd separation)

---

# 🚀 Next Step

Next class → you’ll move into:

* While loops
* Nested loops
* More complex problem solving

👉 This is where automation becomes powerful.

---

# Note

This class is where you shift from **writing code → automating code**.

Loops are one of the most powerful tools in programming.
If you understand this deeply, you can solve 80% beginner problems easily.

---

# 🔥 My Straight Advice

If you master loops:

* You can automate repetitive tasks
* You can handle large data
* You can write efficient code

If you don’t:

* You’ll keep writing repetitive, inefficient code

👉 Practice loops daily — this is non-negotiable.
