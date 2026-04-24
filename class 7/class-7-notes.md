# 🐍 Python Crash Course – Class 7 (Deep Dive)

"""
This class introduces Functions (reusable logic blocks), parameters & arguments, 
return values, scope (local vs global), and real-world modular programming.

👉 This is where you stop writing messy code and start writing structured, scalable programs.
"""

# ---
# ⚙️ 1. What are Functions?
# Core Idea: A function is a named reusable code block.
# 👉 Instead of writing the same code again and again, you write it once and reuse it.

# Built-in Functions (Already in Python)
print("Hello")
len("world")
input("Write your name: ") # Commented out for script flow: input("Write your name")
int("2")
range(20)
type([1,2,3])

# Output:
# Hello
# <class 'list'>

# 🧠 Deep Understanding:
# 👉 Python already gives you functions like print(), len(), and input().
# 👉 But real programming starts when you create your own functions.

# ---
# 🏗️ 2. Creating Your Own Function
# Syntax:
# def function_name():
#     function code

def greet():
    print("Good Morning!")

# Calling the Function:
greet()
greet()
greet()
greet()
greet()
greet()
greet()

# 🧠 Real Insight:
# 👉 Compare this:
# Without function: print("Good Morning!") written 3 times.
# With function: greet() called 3 times.
# ✔ Cleaner | ✔ Reusable | ✔ Professional

# ---
# 📥 3. Parameters & Arguments
def greet_user(name):
    print(f"Hello!,{name}")

greet_user("Ayan")
greet_user("Misha")
greet_user("Sumeet")
greet_user("Aziz")

# 🧠 Deep Understanding:
# Parameter -> variable inside function (name)
# Argument -> actual value ("Ayan")
# 👉 Think: Function = machine | Parameter = input slot | Argument = value you insert

# Loop + Function (Power Combo)
students = ["Ayan", "Misha", "Sumeet"]
for name in students:
    greet_user(name)

# ---
# 🔢 4. Multiple Parameters
def introduce(name, age, city):
    print(f"{name} is , age is {age},city is {city }")

introduce("ayan", 50, "karachi")
# introduce("ayan", "karachi", 50) # 🧠 Critical Insight: Order matters!

# ---
# 🔁 5. Return Statement (Very Important)
# Without Return:
def add_no_return(a, b):
    print(a + b)

result = add_no_return(10, 5)
print(result) # Output: 15, then None

# With Return:
def add(a, b):
    return a + b

def sub(c, d):
    return c - d

result_add = add(10, 5)
result_subtract = sub(100, 60)
print(result_add)      # 15
print(result_subtract) # 40

# 🧠 Deep Concept:
# 👉 print() -> shows value | 👉 return -> sends value back
# ✔ return is used for logic | ✔ print is used for display

# ---
# 🧠 6. Real Logic Example (Age Check)
def age_check(age):
    if age >= 18:
        return "Adult"
    return "Minor"

# 🧠 Insight: Once return runs -> function ends immediately.

# ---
# ⚙️ 7. Default Parameters
def greet_with_default(name, greeting="Hello"):
    print(f"{greeting}, {name}!")

greet_with_default("Ali", "Good morning")
greet_with_default("Ayan") # Uses "Hello"

# ---
# 🎯 8. Keyword Arguments
introduce(name="Ayan", city="ISB", age=12)
# 🧠 Insight: Keyword arguments ignore order and make code readable.

# ---
# 📊 9. Real Problem – Grade System
def get_grade(score):
    if score >= 90: return "A"
    elif score >= 80: return "B"
    elif score >= 70: return "C"
    elif score >= 60: return "D"
    else: return "F"

students_list = [
    {"name": "Ali", "score": 92},
    {"name": "Sara", "score": 75},
    {"name": "Ahmed", "score": 55}
]

for s in students_list:
    grade = get_grade(s["score"])
    print(f"{s['name']} got grade {grade}")

# ---
# 🔢 10. Multiple Returns
def get_stats(numbers):
    return max(numbers), min(numbers), sum(numbers)

nums = [5, 2, 4, 7, 9, 10, 12, 2, 3]
max_n, min_n, sum_n = get_stats(nums)
print(max_n, min_n, sum_n)

# ---
# 🌍 11. Scope (Local vs Global)
# Global Scope:
language = "python"

def show_scope():
    message = "I am local" # Local Scope
    print(f"Inside: {message}")
    print(f"I am learning {language}")

show_scope()

# ⚠️ Global Keyword
count = 10
def increment():
    global count
    count += 1
    print(f"Incremented count: {count}")

# ---
# 🧾 12. Real Project – Receipt System
def calculate_tax(amount):
    return amount * 0.18

def calculate_discount(amount):
    return 2000

def calculate_total(subtotal, tax, discount):
    return subtotal + tax - discount

def print_receipt(subtotal):
    tax = calculate_tax(subtotal)
    discount = calculate_discount(subtotal)
    total = calculate_total(subtotal, tax, discount)

    print("--- RECEIPT ---")
    print("Subtotal: ", subtotal)
    print("Tax:      ", tax)
    print("Discount: ", discount)
    print("Total:    ", total)

print_receipt(70000)

# 🧠 Deep Insight: Functions calling other functions = modular system.
# ✔ Clean | ✔ Maintainable | ✔ Scalable

"""
📘 Concepts Covered:
Functions
Parameters/Arguments
Return vs Print
Default/Keyword Arguments
Multiple Returns
Scope 
Modular Design.

🔥 My Straight Advice:
If you master functions, you think like a developer. 
If you don’t, your code stays messy and unscalable.
"""


# 🐍 Python Crash Course – Class 7 (Deep Dive)

"""
This class introduces Functions (reusable logic blocks), parameters & arguments, 
return values, scope (local vs global), and real-world modular programming.

👉 This is where you stop writing messy code and start writing structured, scalable programs.
"""

# ---
# ⚙️ 1. What are Functions? (The "Recipe" Concept)
# Core Idea: A function is a named reusable code block. 
# Think of it like a recipe: You write the steps once, and cook it whenever you're hungry.

# 👉 Beginner Insight: Every time you see "name()", you are looking at a function. 
# The "()" is the "trigger" that tells Python to run that code.

# Built-in Functions (Already in Python)
print("Hello")           # Displays output
len("world")             # Counts characters/items
input("Your name: ")     # Takes user input
type([1,2,3])            # Identifies data type

# ---
# 🏗️ 2. Creating Your Own Function (Define vs Call)
# Defining (def) is like writing the recipe. 
# Calling is like actually cooking the meal.

def greet():
    print("Good Morning!")

# Calling the Function (The "Trigger")
greet()
greet()

# 🧠 Real Insight:
# Without functions, if you wanted to change "Good Morning" to "Hi", 
# you'd have to edit every line. With a function, you change it in ONE place.

# ---
# 📥 3. Parameters vs Arguments (The "Machine" Analogy)
# Parameter -> The "empty slot" in the machine (name)
# Argument -> The actual item you put into the slot ("Ayan")

def greet_user(name): # 'name' is the Parameter (placeholder)
    print(f"Hello, {name}!")

greet_user("Ayan")    # "Ayan" is the Argument (actual value)
greet_user("Misha")   # "Misha" is the Argument

# ---
# 🔁 4. Return Statement (The "ATM" Concept) - CRITICAL
# 👉 print() is like a TV Screen: You see the result, but you can't grab it.
# 👉 return is like an ATM: It gives you the "cash" (data) to put in your wallet (variable).

# Example WITHOUT Return (You can't use the result later)
def add_simple(a, b):
    print(a + b)

result = add_simple(5, 5) 
# print(result) would show "None" because nothing was handed back.

# Example WITH Return (You can save the result)
def add_logic(a, b):
    return a + b

my_total = add_logic(10, 20)
final_bill = my_total + 100 # We successfully used the data!
print(f"Final Bill: {final_bill}")

# ---
# ⚙️ 5. Default Parameters (The "Safety Net")
# If the user forgets to give an input, the function uses a backup value.

def power_up(player, level=1):
    print(f"{player} is now level {level}")

power_up("Ayan", 10) # Uses 10
power_up("Talha")    # Forgets level, so uses default 1

# ---
# 🎯 6. Keyword Arguments (Order Independence)
def introduce(name, age, city):
    print(f"{name} is {age} years old and lives in {city}")

# Using keywords, the order doesn't matter!
introduce(city="Karachi", age=22, name="Ayan")

# ---
# 🌍 7. Scope (The "Invisible Walls")
# Local Scope: Variables inside a function "die" when the function finishes.
# Global Scope: Variables in the main file live everywhere.

global_var = "I am everywhere"

def scope_test():
    local_var = "I am only inside here"
    print(global_var) # Works!
    print(local_var)  # Works!

scope_test()
# print(local_var) # ERROR: Python can't see inside the function's walls.

# ---
# 📊 8. Real Problem – Modular Grade System
# Breaking a big problem into small, manageable "Lego" pieces.

def get_grade(score):
    if score >= 90: return "A"
    elif score >= 80: return "B"
    else: return "C"

students = [
    {"name": "Ali", "score": 92},
    {"name": "Sara", "score": 75}
]

for s in students:
    grade = get_grade(s["score"])
    print(f"{s['name']} -> Grade: {grade}")

# ---
# 🔢 9. Multiple Returns (Data Bundling)
def get_stats(numbers):
    # Returns 3 values at once as a tuple
    return max(numbers), min(numbers), sum(numbers)

nums = [10, 20, 30]
highest, lowest, total = get_stats(nums)

# ---
# 🧾 10. Real Project – Modular Receipt System
# This shows how real-world professional code is built.

def calculate_tax(amount):
    return amount * 0.18

def calculate_total(subtotal, tax):
    return subtotal + tax

def print_receipt(subtotal):
    tax = calculate_tax(subtotal)
    total = calculate_total(subtotal, tax)
    
    print("--- RECEIPT ---")
    print(f"Subtotal: {subtotal}")
    print(f"Tax:      {tax}")
    print(f"Total:    {total}")

print_receipt(5000)

# 🧠 Deep Insight: 
# If the Tax rate changes, you only update ONE function (calculate_tax).
# This is called "Maintainable Code."

"""
📘 Concepts Covered:
- Define (def) vs Call
- Parameters (slots) vs Arguments (values)
- Return (ATM) vs Print (TV)
- Default Values & Keyword Args
- Scope (Inside vs Outside)
- Modular Design (Small functions connecting together)

🔥 My Straight Advice:
Mastering functions is the difference between a "beginner" and a "developer." 
It allows you to build complex things like your digital agency projects without 
the code falling apart. Keep your functions small, specific, and always use 'return' 
if you need to use that data later!
"""